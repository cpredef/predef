## Feature Macros ##

Rather than checking for specific compilers directly in the code, consider using the compiler macros to set feature macros, and then use these feature macros in your code.

```c
#if defined(PREDEF_COMPILER_MSC)
# define HAVE_WINDOWS_H 1
#endif

#if defined(HAVE_WINDOWS_H)
# include <windows.h>
#endif
```

An example of this can be found in [Boost.Config](http://www.boost.org/doc/libs/1_47_0/libs/config/doc/html/index.html).
