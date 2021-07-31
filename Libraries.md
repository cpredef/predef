Please send updates/corrections to [predef-contribute](mailto:predef-contribute@lists.sourceforge.net).

## Standard C Libraries ##

### [Bionic libc](http://en.wikipedia.org/wiki/Bionic_%28software%29) ###

The following macro is defined in the `<sys/cdefs.h>` header file. It may be best to include it via the `<sys/types.h>` header file, which is required by [POSIX](http://pubs.opengroup.org/onlinepubs/009695299/basedefs/sys/types.h.html).

Type|Macro
---|---
Idenfication|`__BIONIC__`

### [GNU glibc](http://en.wikipedia.org/wiki/Glibc) ###

The following macros have to be included from the `<features.h>` header file.

Type|Macro|Description
---|---|---
Version|`__GNU_LIBRARY__`<br/>`__GNU_LIBRARY_MINOR__`|Until version 5
Version|`__GLIBC__`<br/>`__GLIBC_MINOR__`|From version 6

Notice that the `<features.h>` header file does not exist on all platforms, so it cannot be included without further ado. However, since it is included by other GNU glibc header files, a better way to obtain the above-mentioned macros is to include the `<limits.h>` header file (see e.g. paragraph 4/6 in ISO/IEC 9899:1999).

### [klibc](http://en.wikipedia.org/wiki/Klibc) ###

Type|Macro|Format|Description
---|---|---|---
Identification|`__KLIBC__`| |Zero is a valid value
Version|`__KLIBC__`| |Version
Version|`__KLIBC_MINOR__`| |Revision
Version|`__KLIBC_PATCHLEVEL__`| |Patch
Version|`__KLIBC_VERSION__`|0xVVRRPPPP|VV = Version<br/>RR = Revision<br/>PPPP = Patch

### [uClibc](http://en.wikipedia.org/wiki/Uclibc) ###

The following macros have to be included from the `<features.h>` header file.

Type|Macro|Description
---|---|---
Identification|`__UCLIBC__`|
Version|`__UCLIBC_MAJOR__`|Version
Version|`__UCLIBC_MINOR__`|Revision
Version|`__UCLIBC_SUBLEVEL__`|Patch

### VMS libc ###

Type|Macro|Format|Description
---|---|---|---
Identification|`__CRTL_VER`| |
Version|`__CRTL_VER`|VVRREPPTT|VV = Version<br/>RR = Revision<br/>E = Edit number<br/>PP = Patch (01 = A, ... 26 = Z)<br/>TT = Type (22 = official)

Notice that I am not sure about the format of `__CRTL_VER`, but it seems to follow that of `__VMS_VER`.

### z/OS libc ###

Type|Macro|Format|Description
---|---|---|---
Identification|`__LIBREL__`| |Host
Identification|`__TARGET_LIB__`| |Target
Version|`__LIBREL__`|0xNVRRPPPP|N = Product (0 = C/370, 1 = MVS, 2 = OS/390, 4 = z/OS)<br/>V = Version<br/>RR = Revision<br/>PPPP = Patch<br/><br/>Defined for z/OS XL C/C++
Version|`__TARGET_LIB__`|As above|

##### Example #####

Library|`__LIBREL__`
---|---
OS/390 2.10|0x220A0000
z/OS 1.1|0x41010000
z/OS 1.6|0x41060000

## Standard C++ Libraries ##

### [Dinkumware](http://en.wikipedia.org/wiki/Dinkumware) ###

Type|Macro|Format|Description
---|---|---|---
Identification|`_CPPLIB_VER`| |Defined for Dinkumware 2.0 and later
Version|`_CPPLIB_VER`|VVRR|VV = Version<br/>RR = Revision

##### Example #####

Dinkumware|Visual C++|`_CPPLIB_VER`
---|---|---
3.06||306
3.08||308
4.05|2005|405
5.03|2008|503
5.05|2008 SP1|505
5.20|2010|520
5.40|2012|540
6.10|2013|610

### [GNU libstdc++](http://gcc.gnu.org/libstdc++/) ###

One of the standard header files must be included before any of the following macros are defined.

Type|Macro|Format|Description
---|---|---|---
Version|`__GLIBCPP__`|YYYYMMDD|YYYY = Year<br/>MM = Month<br/>DD = Day<br/><br/>From GCC 3.0.0 until GCC 3.4.0
Version|`__GLIBCXX__`|YYYYMMDD|YYYY = Year<br/>MM = Month<br/>DD = Day<br/><br/>From GCC 3.4.0

##### Example #####

GCC|`__GLIBCPP__`|`__GLIBCXX__`
---|---|---
3.0.0|20010615|
3.1.0|20020514|
3.2.0|20020814|
3.3.0|20030513|
3.4.0| |20040419

### Intel C++ Run-Time Libraries ###

Type|Macro
---|---
Identification|`__INTEL_CXXLIB_ICC`

### [libc++](http://libcxx.llvm.org/) ###

One of the standard header files must be included before any of the following macros are defined.

Type|Macro|Format|Description
---|---|---|---
Version|`_LIBCPP_VERSION`|VRRR|V = Version<br>RRR = Revision
Version|`_LIBCPP_ABI_VERSION`|V|V = ABI Version

## Other Libraries ##

### [Microsoft Foundation Classes](http://en.wikipedia.org/wiki/Microsoft_Foundation_Classes) ###

Type|Macro|Format|Description
---|---|---|---
Identification|`_MFC_VER`| |
Version|`_MFC_VER`|0xVVRR|VV = Version<br/>RR = Revision

##### Example #####

MFC|`_MFC_VER`
---|---
4.21|0x0421
6.0|0x0600
7.0|0x0700
