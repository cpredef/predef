## Version Normalization ##

The pre-defined macros specify version numbering in different ways, which makes it annoying to check for specific compiler versions. In this case you can normalize the version number of the different compilers. For example:

:::c
/* Version is 0xVVRRPPPP */
#define PREDEF_VERSION(v,r,p) (((v) << 24) + ((r) << 16) + (p))

/* Normalize GCC version */
#if defined(__GNUC__)
# if defined(__GNUC_PATCHLEVEL__)
# define PREDEF_COMPILER_GNUC PREDEF_VERSION(__GNUC__, __GNUC_MINOR__, __GNUC_PATCHLEVEL__)
# else
# define PREDEF_COMPILER_GNUC PREDEF_VERSION(__GNUC__, __GNUC_MINOR__, 0)
# endif
#endif

/* Normalize Visual Studio version */
#if defined(_MSC_FULL_VER)
# define PREDEF_COMPILER_MSC PREDEF_VERSION(_MSC_FULL_VER / 1000000, (_MSC_FULL_VER % 1000000) / 10000, _MSC_FULL_VER % 10000)
#else
# if defined(_MSC_VER)
# define PREDEF_COMPILER_MSC CDETECT_MKVER(_MSC_VER / 100, _MSC_VER % 100, 0)
# endif
#endif

This can then be used like this:

:::c
#if defined(PREDEF_COMPILER_GNUC) && (PREDEF_COMPILER_GNUC >= PREDEF_VERSION(4, 6, 0))
/* GNU C/C++ compiler version 4.6.0 or newer */
#endif
