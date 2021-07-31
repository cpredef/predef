Please send updates/corrections to [predef-contribute](mailto:predef-contribute@lists.sourceforge.net).

## Language Standards ##

Language standards requires the existence of pre-defined macros.

Name | Macro | Standard
---|---|---
C89|`__STDC__`|ANSI X3.159-1989
C90|`__STDC__`|ISO/IEC 9899:1990
C94|`__STDC_VERSION__` = 199409L|ISO/IEC 9899-1:1994
[C99](http://www.open-std.org/jtc1/sc22/wg14/)|`__STDC_VERSION__` = 199901L|ISO/IEC 9899:1999
[C11](http://en.wikipedia.org/wiki/C11_%28C_standard_revision%29)|`__STDC_VERSION__` = 201112L|ISO/IEC 9899:2011
[C18](https://en.wikipedia.org/wiki/C18_%28C_standard_revision%29)|`__STDC_VERSION__` = 201710L|ISO/IEC 9899:2018
[C++98](http://www.open-std.org/jtc1/sc22/wg21/)|`__cplusplus` = 199711L|ISO/IEC 14882:1998
[C++11](http://en.wikipedia.org/wiki/C%2B%2B11)|`__cplusplus` = 201103L|ISO/IEC 14882:2011
[C++14](http://en.wikipedia.org/wiki/C%2B%2B14)|`__cplusplus` = 201402L|ISO/IEC 14882:2014
[C++17](http://en.wikipedia.org/wiki/C%2B%2B17)|`__cplusplus` = 201703L|ISO/IEC 14882:2017
[C++/CLI](http://www.ecma-international.org/publications/standards/Ecma-372.htm)|`__cplusplus_cli` = 200406L|ECMA-372
[DSP-C](http://www.dsp-c.org)| |ISO/IEC JTC1/SC22 WG14/N854
[EC++](http://www.caravan.net/ec2plus/)|`__embedded_cplusplus`|Embedded C++

##### Example: C Standards #####

```c
#if defined(__STDC__)
# define PREDEF_STANDARD_C_1989
# if defined(__STDC_VERSION__)
# if (__STDC_VERSION__ >= 199409L)
# define PREDEF_STANDARD_C_1994
# endif
# if (__STDC_VERSION__ >= 199901L)
# define PREDEF_STANDARD_C_1999
# endif
# endif
#endif
```

Notice that not all compliant compilers provides the correct pre-defined macros. For example, Microsoft Visual C++ does not define `__STDC__`, or Sun Workshop 4.2 supports C94 without setting `__STDC_VERSION__` to the proper value. Extra checks for such compilers must be added.

Notice that some compilers, such as the [HP aC++](http://h21007.www2.hp.com/portal/site/dspp/menuitem.863c3e4cbcdc3f3515b49c108973a801?ciid=4b080055abe021100055abe02110275d6e10RCRD), use the value 199707L to indicate the C++98 standard. This value was used in an earlier proposal of the C++98 standard.

##### Example: Pre-C89 #####

In continuation of the above example, pre-C89 compilers do not recognize certain keywords. Let the preprocessor remove those keywords for those compilers.

```c
#if !defined(PREDEF_STANDARD_C_1989) && !defined(__cplusplus)
# define const
# define volatile
#endif
```

## Unix Standards ##

There are several related Unix standards, such as [POSIX](http://en.wikipedia.org/wiki/POSIX), [X/Open](http://en.wikipedia.org/wiki/X/Open), and [LSB](http://en.wikipedia.org/wiki/Linux_Standard_Base).

Unix standards require the existence macros in the `<unistd.h>` header file.

Name | Macro | Standard
---|---|---
POSIX.1-1988|`_POSIX_VERSION` = 198808L|
POSIX.1-1990|`_POSIX_VERSION` = 199009L|ISO/IEC 9945-1:1990
POSIX.2|`_POSIX2_C_VERSION` = 199209L|ISO/IEC 9945-2:1993
POSIX.1b-1993|`_POSIX_VERSION` = 199309L|IEEE 1003.1b-1993
POSIX.1-1996|`_POSIX_VERSION` = 199506L|IEEE 1003.1-1996
POSIX.1-2001|`_POSIX_VERSION` = 200112L|IEEE 1003.1-2001
[POSIX.1-2008](http://pubs.opengroup.org/onlinepubs/9699919799/)|`_POSIX_VERSION` = 200809L|IEEE 1003.1-2008
XPG3|`_XOPEN_VERSION` = 3|X/Open Portability Guide 3 (1989)
XPG4|`_XOPEN_VERSION` = 4|X/Open Portability Guide 4 (1992)
SUS|`_XOPEN_VERSION` = 4 `&&` `_XOPEN_UNIX`|X/Open Single UNIX Specification (UNIX95)
[SUSv2](http://www.opengroup.org/onlinepubs/7908799/toc.htm)|`_XOPEN_VERSION` = 500|X/Open Single UNIX Specification, Version 2 (UNIX98)
[SUSv3](http://www.opengroup.org/onlinepubs/007904975/nfindex.html)|`_XOPEN_VERSION` = 600|Open Group Single UNIX Specification, Version 3 (UNIX03)
[SUSv4](http://pubs.opengroup.org/onlinepubs/9699919799/)|`_XOPEN_VERSION` = 700|Open Group Single UNIX Specification, Version 4
LSB|`__LSB_VERSION__` = VR|Linux Standards Base<br/><br/>V = Version<br/>R = Revision

##### Example: Unix Standards #####

The following examples assumes the definition of these macros.

```c
#if defined(unix) || defined(__unix__) || defined(__unix)
# define PREDEF_PLATFORM_UNIX
#endif
#if defined(PREDEF_PLATFORM_UNIX)
# include <unistd.h>
# if defined(_XOPEN_VERSION)
# if (_XOPEN_VERSION >= 3)
# define PREDEF_STANDARD_XOPEN_1989
# endif
# if (_XOPEN_VERSION >= 4)
# define PREDEF_STANDARD_XOPEN_1992
# endif
# if (_XOPEN_VERSION >= 4) && defined(_XOPEN_UNIX)
# define PREDEF_STANDARD_XOPEN_1995
# endif
# if (_XOPEN_VERSION >= 500)
# define PREDEF_STANDARD_XOPEN_1998
# endif
# if (_XOPEN_VERSION >= 600)
# define PREDEF_STANDARD_XOPEN_2003
# endif
# if (_XOPEN_VERSION >= 700)
# define PREDEF_STANDARD_XOPEN_2008
# endif
# endif
#endif
```

Notice that not all compliant compilers provides the correct pre-defined macros. For example, IBM xlC supports Unix without setting any of the `__unix__` macros. Extra checks for such compilers must be added.
