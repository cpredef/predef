Please send updates/corrections to [predef-contribute](mailto:predef-contribute@lists.sourceforge.net).

## [ACC](http://en.wikipedia.org/wiki/ACC_%28programming_language%29) ##

Type|Macro
---|---
Identification|`_ACC_`

## [Altium MicroBlaze C](http://en.wikipedia.org/wiki/Altium) ##

Type|Macro|Format|Description
---|---|---|---
Identification|`__CMB__`| |
Version|`__VERSION__`|VRRR|V=Version<br/>RRR=Revision
Version|`__REVISION__`|P|P=Patch
Version|`__BUILD__`|VRRRPPP|Build number

##### Example #####

Altium MicroBlaze C|`__VERSION__`|`__REVISION__`|`__BUILD__`
---|---|---|---
1.0r2|1000|2|
1.22.2| | |1022001

## [Altium C-to-Hardware](http://en.wikipedia.org/wiki/Altium) ##

Type|Macro|Format|Description
---|---|---|---
Identification|`__CHC__`| |
Version|`__VERSION__`|VRRR|V=Version<br/>RRR=Revision
Version|`__REVISION__`|P|P=Patch<br/>Beta releases set this to -1
Version|`__BUILD__`|VRRRPPP|Build number

##### Example #####

Altium C-to-Hardware|`__VERSION__`|`__REVISION__`|`__BUILD__`
---|---|---|---
2.1r1|2001|1|
1.22.2| | |1022001

## [Amsterdam Compiler Kit](http://en.wikipedia.org/wiki/Amsterdam_Compiler_Kit) ##

Type|Macro
---|---
Identification|`__ACK__`

## [ARM Compiler](http://www.arm.com/products/tools/software-tools/rvds/arm-compiler.php) ##

Type|Macro|Format|Description
---|---|---|---
Identification|`__CC_ARM`| |
Version|`__ARMCC_VERSION`|VRPBBB|V = Version<br/>R = Revision<br/>P = Patch<br/>BBB = Build

Notice that the `__ARMCC_VERSION` macro is also used as version indicator for Norcroft C, but that the format is different.

##### Example #####

Realview C|`__ARMCC_VERSION`
---|---
3.0|300503

## [Aztec C](http://en.wikipedia.org/wiki/Aztec_C) ##

Type|Macro|Format|Description
---|---|---|---
Identification|`AZTEC_C`<br/>`__AZTEC_C__`| |
Version|`__VERSION`|VRR|V = Version<br/>RR = Revision

##### Example #####

Aztec C|`__VERSION`
---|---
5.20|520

## [Borland C++](http://en.wikipedia.org/wiki/C_plus_plus_builder) ##

Type|Macro|Format
---|---|---
Identification|`__BORLANDC__`|
Version|`__BORLANDC__`|?
Identification|`__CODEGEARC__`|
Version|`__CODEGEARC__`|From C++ Builder 2006

##### Example #####

Borland C++|C++ Builder|`__BORLANDC__`|`__CODEGEARC__`
---|---|---|---
2.0| |0x200|
3.0| |0x400|
3.1| |0x410|
4.0| |0x452|
5.0| |0x500|
5.02|1.0|0x520|
|3.0|0x530|
|4.0|0x540|
5.5|5.0|0x550|
5.51| |0x551|
5.6.4| |0x562|
|2006|0x570|0x570
|2007|0x590|0x590
|2009|0x613|0x613
|2010|0x621|0x621
|XE|0x630|0x630
|XE2|0x640|0x640
|XE3|0x650|0x650
|XE4|0x660|0x660

## [CC65](http://en.wikipedia.org/wiki/Cc65) ##

Type|Macro|Format|Description
---|---|---|---
Identification|`__CC65__`| |
Version|`__CC65__`|0xVRP|V = Version<br/>R = Revision<br/>P = Patch

##### Example #####

Version|`__CC65__`
---|---
2.10.1|0x2A1

## [Clang](http://en.wikipedia.org/wiki/Clang) ##

Type|Macro|Format|Description
---|---|---|---
Identification|`__clang__`||
Version|`__clang_major__`|V|V = Major version
Version|`__clang_minor__`|R|R = Minor version
Version|`__clang_patchlevel__`|P|P = Patch level
Version|`__clang_version__`|V.R.P (tags/RELEASE_VRP/final)|V = Major version<br/>R = Minor version<br/>P = Patch level

Notice that clang also defines the GNU C version macros, but you should use the clang [feature checking macros](http://clang.llvm.org/docs/LanguageExtensions.html#feature_check) to detect the availability of various features.

The values of the `__clang_major__`, `__clang_minor__`, and `__clang_patchlevel__` macros are not consistent across distributions of the Clang compiler. For example, the Clang 3.1 distribution available at http://clang.llvm.org defines `__clang_major__` and `__clang_minor__` as `3` and `1` respectively. The version of Clang distributed with Apple XCode 4.4 is branded as "Apple Clang 4.0" and derives from the open source Clang 3.1 distribution, but defines these macros with the values `4` and `0` respectively. Apple's Clang distribution can be identified by the presence of the `__apple_build_version__` macro.

The meaning of the `__clang__` and related macros has changed subtly over the years, from identifying the Clang compiler to identifying compilers that use the Clang infrastructure. For example, IBM XL C/C++ also defines these macros. [IBM XL C/C++ for Linux](https://www.ibm.com/support/knowledgecenter/en/SSXVZZ_16.1.1/com.ibm.xlcpp1611.lelinux.doc/compiler_ref/xlmacros.html?sc=SSXVZZ_latest) defines them starting from version 13.1.1. [IBM XL C/C++ for AIX](https://www.ibm.com/support/knowledgecenter/en/SSGH3R_16.1.0/com.ibm.xlcpp161.aix.doc/compiler_ref/xlmacros.html?sc=SSGH3R_latest) defines them starting from version 16.1.

## [Comeau C++](http://en.wikipedia.org/wiki/Comeau_C/C%2B%2B) ##

Type|Macro|Format|Description
---|---|---|---
Identification|`__COMO__`|
Version|`__COMO_VERSION__`|VRR|V = Version<br/>RR = Revision

##### Example #####

Comeau C++|`__COMO_VERSION__`
---|---
2.3|230

## [Compaq C/C++](http://www.openvms.compaq.com/openvms/brochures/deccplus/) ##

Type|Macro|Format|Description
---|---|---|---
Identification|`__DECC`| |C compiler
Version|`__DECC_VER`|VVRRTPPPP|VV = Version<br/>RR = Revision<br/>T = Type (9 = official)<br/>PPPP = Patch
Identification|`__DECCXX`| |C++ compiler
Version|`__DECCXX_VER`|As __DECC_VER|
Identification|`__VAXC`| |Obsolete
Identification|`VAXC`| |Obsolete

##### Example #####

Compaq C/C++|`__DECC_VER`
---|---
6.0-001|60090001

## [Convex C](http://en.wikipedia.org/wiki/Convex_Computer) ##

Type|Macro
---|---
Identification|`__convexc__`

## [CompCert](http://en.wikipedia.org/wiki/CompCert) ##

Type|Macro
---|---
Identification|`__COMPCERT__`

## [Coverity C/C++ Static Analyzer](http://www.coverity.com/) ##

Type|Macro
---|---
Identification|`__COVERITY__`

## Cray C ##

Type|Macro|Description
---|---|---
Identification|`_CRAYC`|
Version|`_RELEASE`|Version
Version|`_RELEASE_MINOR`|Revision

## [Diab C/C++](http://www.windriver.com/products/development_suite/wind_river_compiler/) ##

Type|Macro|Format|Description
---|---|---|---
Identification|`__DCC__`|1|
Version|`__VERSION_NUMBER__`|VRPP|V = Version<br/>R = Revision<br/>PP = Patch

##### Example #####

Diab C/C++|`__VERSION_NUMBER__`
---|---
4.4g|4426

## [DICE C](http://en.wikipedia.org/wiki/DICE_%28compiler%29) ##

Type|Macro
---|---
Identification|`_DICE`

## [Digital Mars](http://en.wikipedia.org/wiki/Digital_Mars) ##

Type|Macro|Format|Description
---|---|---|---
Identification|`__DMC__`| |
Version|`__DMC__`|0xVRP|V = Version<br/>R = Revision<br/>P = Patch

##### Example #####

Digital Mars|`__DMC__`
---|---
7.0|0x700
7.2|0x720
8.0|0x800

## [Dignus Systems/C++](http://www.dignus.com/dcxx/) ##

Type|Macro|Format|Description
---|---|---|---
Identification|`__SYSC__`| |
Version|`__SYSC_VER__`|VRRPP|V = Version<br/>RR = Revision<br/>PP = Patch

##### Example #####

Systems/C|`__SYSC_VER__`
---|---
1.80.32|18032

## [DJGPP](http://en.wikipedia.org/wiki/Djgpp) ##

Type|Macro|Description
---|---|---
Identification|`__DJGPP__`|
Version|`__DJGPP__`|Version
Version|`__DJGPP_MINOR__`|Revision
Identification|`__GO32__`|Defined by DJGPP 1.x

##### Example #####

DJGPP|`__DJGPP__`|`__DJGPP_MINOR__`
---|---|---
2.01|2|1

## [EDG C++ Frontend](http://en.wikipedia.org/wiki/Edison_Design_Group) ##

Type|Macro|Format|Description
---|---|---|---
Identification|`__EDG__`| |
Version|`__EDG_VERSION__`|VRR|V = Version<br/>RR = Revision

##### Example #####

EDG C++|`__EDG_VERSION__`
---|---
2.30|230
2.45|245

## [EKOPath](http://en.wikipedia.org/wiki/PathScale) ##

Type|Macro|Description
---|---|---
Identification|`__PATHCC__`|
Version|`__PATHCC__`|Version
Version|`__PATHCC_MINOR__`|Revision
Version|`__PATHCC_PATCHLEVEL__`|Patch

##### Example #####

EKOPath|`__PATHCC__`|`__PATHCC_MINOR__`|`__PATHCC_PATCHLEVEL__`
---|---|---|---
2.0|2|0|0

## Fujitsu C++ ##

Type|Macro
---|---
Identification|`__FCC_VERSION`

## [GCC C/C++](http://en.wikipedia.org/wiki/GNU_Compiler_Collection) ##

Type|Macro|Description
---|---|---
Identification|`__GNUC__`|
Version|`__GNUC__`|Version
Version|`__GNUC_MINOR__`|Revision
Version|`__GNUC_PATCHLEVEL__`|Patch (introduced in version 3.0)

Notice that the meaning of the `__GNUC__` macro has changed subtly over the years, from identifying the GNU C/C++ compiler to identifying any compiler that implements the GNU compiler extensions (see the [Feature request - a macro defined for GCC](http://gcc.gnu.org/ml/gcc/2008-07/threads.html#00025) discussion for further information). For example, the Intel C++ on Linux also defines these macros from version 8.1 (see the [Intel C++ Compiler 8.1 for Linux Release Notes](ftp://download.intel.com/support/performancetools/c/linux/sb/clin81_relnotes.pdf) and [Intel Compilers for Linux: Compatibility with GNU Compilers](http://software.intel.com/en-us/articles/intel-compilers-for-linux-compatibility-with-gnu-compilers).)

##### Example #####

GNU C/C++|`__GNUC__`|`__GNUC_MINOR__`|`__GNUC_PATCHLEVEL__`
---|---|---|---
2.7.x|2|7|N/A
3.0.2|3|0|2

### Alternative Version ###

If you prefer a single version macro, you can define the following yourself.

:::c
#if defined(__GNUC__)
# if defined(__GNUC_PATCHLEVEL__)
# define __GNUC_VERSION__ (__GNUC__ * 10000 \
+ __GNUC_MINOR__ * 100 \
+ __GNUC_PATCHLEVEL__)
# else
# define __GNUC_VERSION__ (__GNUC__ * 10000 \
+ __GNUC_MINOR__ * 100)
# endif
#endif

The format of this new macro is:

Type|Macro|Format|Description
---|---|---|---
Version|`__GNUC_VERSION__`|VVRRPP|VV = Version<br/>RR = Revision<br/>PP = Patch

##### Example of Alternative Version #####

GNU C/C++|`__GNUC_VERSION__`
---|---
2.7.x|20700
3.0.2|30002

## [Green Hill C/C++](http://en.wikipedia.org/wiki/Green_Hills_Software) ##

Type|Macro|Format|Description
---|---|---|---
Identification|`__ghs__`| |
Version|`__GHS_VERSION_NUMBER__`|VRP|V = Version<br/>R = Revision<br/>P = Patch
Version|`__GHS_REVISION_DATE__`|[Epoch time](http://en.wikipedia.org/wiki/Epoch_time)|

##### Example #####

Green Hill C/C++|`__GHS_VERSION_NUMBER__`
---|---
4.2.1|421

## HP ANSI C ##

Type|Macro
---|---
Identification|`__HP_cc`

## [HP aC++](http://en.wikipedia.org/wiki/HP_aC%2B%2B) ##

Type|Macro|Format|Description
---|---|---|---
Identification|`__HP_aCC`| |
Version|`__HP_aCC`|1|From version A.01.15 (and A.03.13)
Version|`__HP_aCC`|VVRRPP|VV = Version<br/>RR = Revision<br/>PP = Patch<br/><br/>From version A.01.21 (and A.03.25)

##### Example #####

HP aCC|`__HP_aCC`
---|---
A.01.21|12100

### IAR C/C++ ###

Type|Macro|Format|Description
---|---|---|---
Identification|`__IAR_SYSTEMS_ICC__`| |
Version|`__VER__`|VRR|V = Version<br/>RR = Revision

##### Example #####

IAR C/C++|`__VER__`
---|---
3.34|334

##[IBM XL C/C++ (Clang-based versions)](https://www.ibm.com/us-en/marketplace/ibm-c-and-c-plus-plus-compiler-family)##
The entry on XL C/C++ has been split into three for clarity. This entry covers the following versions:
[IBM XL C/C++ for Linux](https://www.ibm.com/support/knowledgecenter/en/SSXVZZ_16.1.1/com.ibm.xlcpp1611.lelinux.doc/compiler_ref/xlmacros.html?sc=SSXVZZ_latest) for little endian distributions version 13.1.1 and later
[IBM XL C/C++ for AIX](https://www.ibm.com/support/knowledgecenter/en/SSGH3R_16.1.0/com.ibm.xlcpp161.aix.doc/compiler_ref/xlmacros.html?sc=SSGH3R_latest) version 16.1 and later (Clang-based compiler invocation only, see next section for legacy compiler invocation)
Clang-based versions of IBM XL C/C++ define the Clang macros listed in the Clang section.
Specify -qxlcompatmacros to also define the legacy macros listed in IBM XL C/C++ (legacy versions). This is useful when you migrate programs from IBM XL C/C++ (legacy versions) to IBM XL C/C++ (Clang-based versions).

Type|Macro|Format|Description
---|---|---|---
Identification|`__ibmxl__`| |C and C++ compiler
|`__clang__`||
Version|`__ibmxl_vrm__`|0xVVRRMM00|VV = Version<br/>RR = Release<br/>MM = Modification
|`__ibmxl_version__`|V|V = Version
|`__ibmxl_release__`|R|R = Release
|`__ibmxl_modification__`|M|M = Modification
|`__ibmxl_ptf_fix_level__`|F|F = Fix Pack

##### Example #####
IBM XL C/C++|`__ibmxl_vrm__`
---|---
13.1.6.1|0x0D010600
16.1.0.0|0x10010000

## [IBM XL C/C++ (legacy versions)](https://www.ibm.com/us-en/marketplace/ibm-c-and-c-plus-plus-compiler-family) ##

The entry on XL C/C++ has been split into three for clarity. This entry covers the following versions:
[IBM XL C/C++ for Linux](https://www.ibm.com/support/knowledgecenter/en/SSXVZZ_13.1.0/com.ibm.xlcpp131.linux.doc/compiler_ref/xlmacros.html) for big endian distributions
[IBM XL C/C++ for AIX](https://www.ibm.com/support/knowledgecenter/en/SSGH3R_16.1.0/com.ibm.xlcpp161.aix.doc/compiler_ref/xlmacros.html?sc=SSGH3R_latest) (Note: starting in version 16.1, IBM XL C/C++ for AIX also offers a Clang-based compiler invocation, see the Clang-based versions section above for that compiler invocation)

Clang-based versions of IBM XL C/C++ will also define the legacy macros listed in this section when -qxlcompatmacros is specified.

Type|Macro|Format|Description
---|---|---|---
Identification|`__xlC__`| |C and C++ compiler
Version|`__IBMC__`| 0xVVRRMM|C compiler<br/><br/>VV = Version<br/>RR = Release<br/>MM = Modification
|`__IBMCPP__`| 0xVVRRMM|C++ compiler<br/><br/>VV = Version<br/>RR = Release<br/>MM = Modification
|`__xlc__`|0xVVRRMMFF|C compiler<br/><br/>VV = Version<br/>RR = Release<br/>MM = Modification<br/>FF = Fix Pack
|`__xlC__`|0xVVRR|C and C++ compiler<br/><br/>VV = Version<br/>RR = Release
|`__xlC_ver__`|0x0000MMFF|MM = Modification<br/>FF = Fix Pack

##### Example #####

IBM XL C/C++|`__IBMCPP__`|`__xlC__`|`__xlC_ver__`
---|---|---|---
13.1.3.5|0x0D0103|0x0D01|0x00000305
12.1.0.4|0x0C0100|0x0C01|0x00000004

## [IBM z/OS XL C/C++](https://www.ibm.com/us-en/marketplace/xl-cpp-compiler-zos) ##

The entry on XL C/C++ has been split into three for clarity. This entry covers the [XL C/C++ compiler for mainframes (e.g. z/OS)](https://www.ibm.com/support/knowledgecenter/en/SSLTBW_latest/com.ibm.zos.v2r3.cbclx01/xlmacros.htm).

Type|Macro|Format|Description
---|---|---|---
Identification|`__IBMC__`| |C compiler
|`__IBMCPP__`| |C++ compiler
Version|`__IBMC__`<br/>`__IBMCPP__`|NVRRM|N = Product (0 = C/370, 1 = MVS, 2 = OS/390, 4 = z/OS)<br/>V = Version<br/>RR = Revision<br/>M = Modification
|`__COMPILER_VER__`|0xNVRRMMFF|N = Product (see above)<br/>V = Version<br/>RR = Revision<br/>MM = Modification<br/>FF = Fix Pack

Notice that XL C/C++ also defines `__IBMC__` and `__IBMCPP__` macros, but with a different syntax. You can use `__xlC__` (only defined for XL C/C++) or `__COMPILER_VER__` (only defined for z/OS XL C/C++) to distinguish between the two. Alternatively, the macro identifying z/OS (`__MVS__`) can be used to distinguish between them.

:::c
#if defined(__IBMC__) || defined(__IBMCPP__)
# if defined(__COMPILER_VER__)
/* z/OS XL C/C++ so __IBMC__ is defined as NVRRM */
# else
/* z/OS XL C/C++ so __IBMC__ is defined as VRM */
# endif
#endif

##### Example #####

IBM z/OS XL C/C++|`__IBMC__`|`__COMPILER_VER__`
---|---|---
2.3|42030|0x42030000

## [ImageCraft C](http://www.imagecraft.com/) ##

Type|Macro
---|---
Identification|`__IMAGECRAFT__`

## [Intel C/C++](http://en.wikipedia.org/wiki/Intel_C%2B%2B) ##

Type|Macro|Format|Description
---|---|---|---
Identification|`__INTEL_COMPILER`| |
Identification|`__ICC`| |Obsolete
Identification|`__ECC`| |Obsolete
Identification|`__ICL`| |
Version|`__INTEL_COMPILER`|VRP|V = Version<br/>R = Revision<br/>P = Patch
Version|`__INTEL_COMPILER_BUILD_DATE`|YYYYMMDD|YYYY = Year<br/>MM = Month<br/>DD = Day

##### Example #####

Intel C/C++|`__INTEL_COMPILER`|`__INTEL_COMPILER_BUILD_DATE`
---|---|---
5.0|500|
6.0|600|
8.0|800|
9.0|900|20060222

## KAI C++ ##

Type|Macro|Format|Description
---|---|---|---
Identification|`__KCC`| |
Version|`__KCC_VERSION`|0xVRPP|V = Version<br/>R = Revision<br/>PP = Patch (a = 01, b = 02, ...)

##### Example #####

KAI C++|`__KCC_VERSION`
---|---
4.0d|4004

## [KEIL CARM](http://www.keil.com/arm/carm.asp) ##

Type|Macro|Format|Description
---|---|---|---
Identification|`__CA__`| |
Identification|`__KEIL__`| |
Version|`__CA__`|VRR|V = Version<br/>RR = Revision

##### Example #####

Keil CARM|`__CA__`
---|---
1.01|101

## [KEIL C166](http://www.keil.com/c166/c166.asp) ##

Type|Macro|Format|Description
---|---|---|---
Identification|`__C166__`| |
Version|`__C166__`|VRR|V = Version<br>RR = Revision

##### Example #####

Keil C166|`__C166__`
---|---
5.01|501

## [KEIL C51](http://www.keil.com/c51/c51.asp) ##

Type|Macro|Format|Description
---|---|---|---
Identification|`__C51__`| |
Identification|`__CX51__`| |
Version|`__C51__`|VRR|V = Version<br/>RR = Revision

##### Example #####

Keil C51|`__C51__`
---|---
7.01|701

## [LCC](http://en.wikipedia.org/wiki/Local_C_compiler) ##

Type|Macro
---|---
Identification|`__LCC__`

## [LLVM](http://en.wikipedia.org/wiki/LLVM) ##

Type|Macro
---|---
Identification|`__llvm__`

The Clang compiler has an expectation that it operates in conjunction with the LLVM compiler, so the Clang compiler defines `__llvm__` too. IBM XL C/C++ (Clang-based versions) use Clang infrastructure, so IBM XL C/C++ for Linux versions 13.1.1 to 16.1 also define `__llvm__`. Starting from version 16.1.1, [IBM XL C/C++ for Linux](https://www.ibm.com/support/knowledgecenter/en/SSXVZZ_16.1.1/com.ibm.xlcpp1611.lelinux.doc/compiler_ref/xlmacros.html?sc=SSXVZZ_latest) no longer defines `__llvm__`.

## MetaWare High C/C++ ##

Type|Macro
---|---
Identification|`__HIGHC__`

## [Metrowerks CodeWarrior](http://en.wikipedia.org/wiki/CodeWarrior) ##

Type|Macro|Format|Description
---|---|---|---
Identification|`__MWERKS__`| |
Identification|`__CWCC__`| |From 4.2.0
Version|`__MWERKS__`|1|Until CodeWarrior 7
Version|`__MWERKS__`|0xVRPP|V = Version<br/>R = Revision<br/>PP = Patch<br/><br/>From CodeWarrior 7
Version|`__CWCC__`|0xVRPP|V = Version<br/>R = Revision<br/>PP = Patch<br/><br/>From 4.2.0

##### Example #####

Metrowerks C/C++|`__MWERKS__`|`__CWCC__`
---|---|---
2.0|0x2000|
2.2|0x2200|
4.2.0|0x4200|0x4200

## [Microsoft Visual C++](http://en.wikipedia.org/wiki/Visual_studio) ##

Type|Macro|Format|Description
---|---|---|---
Identification|`_MSC_VER`| |
Version|`_MSC_VER`|VVRR|VV = Version<br/>RR = Revision
Version|`_MSC_FULL_VER`|VVRRPPPP|VV = Version<br/>RR = Revision<br/>PPPP = Patch<br/><br/>From Visual C++ 6.0 Processor Pack
Version|`_MSC_FULL_VER`|VVRRPPPPP|VV = Version<br/>RR = Revision<br/>PPPPP = Patch<br/><br/>From Visual C++ 8.0
Version|`_MSC_BUILD`|B|B = Build number<br/><br/>From Visual C++ 9.0

##### Example #####

Visual C++ [1](http://msdn.microsoft.com/en-us/library/b0084kay.aspx) [2](http://social.msdn.microsoft.com/Forums/en-US/vcgeneral/thread/c3f1ba1f-c59d-46a3-a028-bcfabe9fbe2c/)|`_MSC_VER`|`_MSC_FULL_VER`
---|---|---
1.0|800|
3.0|900|
4.0|1000|
4.2|1020|
5.0|1100|
6.0|1200|
6.0 SP6|1200|12008804
7.0|1300|13009466
7.1 (2003)|1310|13103077
8.0 (2005)|1400|140050727
9.0 (2008)|1500|150021022
9.0 SP1|1500|150030729
10.0 (2010)|1600|160030319
10.0 (2010) SP1|1600|160040219
11.0 (2012)|1700|170050727
12.0 (2013)|1800|180021005
14.0 (2015)|1900|190023026
14.0 (2015 Update 1)|1900|190023506
14.0 (2015 Update 2)|1900|190023918
14.0 (2015 Update 3)|1900|190024210
15.0 (2017)|1910|191025017

## [Microtec C/C++](http://www.mentor.com/microtec/) ##

Type|Macro
---|---
Identification|`_MRI`

## [Microway NDP C](http://en.wikipedia.org/wiki/Microway) ##

Type|Macro
---|---
Identification|`__NDPC__`<br/>`__NDPX__`

## [MinGW](http://www.mingw.org/) and [MinGW-w64](http://mingw-w64.sourceforge.net/) ##

MinGW (formerly known as MinGW32) is a toolchain for creating 32 Bit Windows executables. The MinGW-w64 projects offers toolchains for creating 32 Bit and 64 Bit Windows executables. The following table shows which macros are defined by each toolchain:

Type|Macro|Description|MinGW32|MinGW-w64 32 Bit|MinGW-w64 64 Bit
---|---|---|---|---|---
Identification|`__MINGW32__`| | defined | defined | defined
Version|`__MINGW32_MAJOR_VERSION`|Version| defined | defined | defined
Version|`__MINGW32_MINOR_VERSION`|Revision| defined | defined | defined
Identification|`__MINGW64__`| | - | - | defined
Version|`__MINGW64_VERSION_MAJOR`|Version| - | defined | defined
Version|`__MINGW64_VERSION_MINOR`|Revision| - | defined | defined

Notice that `__MINGW32_MAJOR_VERSION`, `__MINGW32_MINOR_VERSION`, `__MINGW64_VERSION_MAJOR`, and `__MINGW64_VERSION_MINOR`
are only defined if appropriate headers are included. Appropriate headers are
`<stdlib.h>`, `<stdio.h>`, `<windows.h>`, `<windef.h>`, and probably more.

##### Examples #####

`__MINGW32_MAJOR_VERSION`|`__MINGW32_MINOR_VERSION`|`__MINGW64_VERSION_MAJOR`|`__MINGW64_VERSION_MINOR`|Description
---|---|---|---|---
2|4| | | MinGW32 2.4
3|20| | | MinGW32 3.20
3|11|2|0| MinGW-w64 2.0

## [MIPSpro](http://en.wikipedia.org/wiki/MIPSpro) ##

Type|Macro|Format|Description
---|---|---|---
Identification|`__sgi`| |
Identification|`sgi`| |
Version|`_COMPILER_VERSION`|VRP|V = Version<br/>R = Revision<br/>P = Patch<br/><br/>Until ?
Version|`_SGI_COMPILER_VERSION`|VRP|V = Version<br/>R = Revision<br/>P = Patch<br/><br/>From ?

##### Example #####

MIPSpro|`_COMPILER_VERSION`|`_SGI_COMPILER_VERSION`
---|---|---
6.0.2|602|
7.2.1|721|
7.4.4| |744

## [Miracle C](http://www.c-compiler.com/) ##

Type|Macro
---|---
Identification|`MIRACLE`

## [MPW C++](http://en.wikipedia.org/wiki/Macintosh_Programmer%27s_Workshop) ##

Type|Macro|Format|Description
---|---|---|---
Identification|`__MRC__`| |
Identification|`MPW_C`| |
Identification|`MPW_CPLUS`| |
Version|`__MRC__`|0xVVRR|VV = Version<br/>RR = Revision

##### Example #####

MPW C++|`__MRC__`
---|---
5.0|0x500

## [Norcroft C](http://www.codemist.co.uk/ncc/index.html) ##

Type|Macro|Format|Description
---|---|---|---
Identification|`__CC_NORCROFT`| |
Version|`__ARMCC_VERSION`|V.R|V = Version<br/>R = Revision

Notice that `__ARMCC_VERSION` is assigned a floating-point number, so it cannot be used by the preprocessor to compare versions.

##### Example #####

Norcroft C|`__ARMCC_VERSION`
---|---
4.69|4.69
4.90|4.90

## [NWCC](http://nwcc.sourceforge.net/) ##

Type|Macro
---|---
Identification|`__NWCC__`

## [Open64](http://en.wikipedia.org/wiki/Open64) ##

Type|Macro|Format|Description
---|---|---|---
Identification|`__OPEN64__`||Contains the full version as a string
Identification|`__OPENCC__`||
Version|`__OPENCC__`|V|V = Version
Version|`__OPENCC_MINOR__`|R|R = Revision
Version|`__OPENCC_PATCHLEVEL__`|P.B|P = Patch<br/>B = Build

Notice that `__OPENCC_PATCHLEVEL__` can be a floating-point number (e.g. `5.2` for Open64 version 4.2.5.2) so it cannot be used by the preprocessor to compare patch-levels.

## [Oracle Pro*C Precompiler](http://en.wikipedia.org/wiki/Pro*C) ##

Type|Macro
---|---
Identification|`ORA_PROC`

## [Oracle Solaris Studio](http://en.wikipedia.org/wiki/Oracle_Solaris_Studio) ##

Type|Macro|Format|Description
---|---|---|---
Identification|`__SUNPRO_C`| |C compiler
Version|`__SUNPRO_C`|0xVRP|V = Version<br/>R = Revision<br/>P = Patch<br/><br/>Until version 5.9
Version|`__SUNPRO_C`|0xVRRP|V = Version<br/>RR = Revision<br/>P = Patch<br/><br/>From later releases
Identification|`__SUNPRO_CC`| |C++ compiler
Version|`__SUNPRO_CC`|As `__SUNPRO_C`|

##### Example #####

Compiler version|Solaris Studio|`__SUNPRO_C`
---|---|---
4.2|4.2|0x420
5.0|5.0|0x500
5.2|6.1|0x520
5.3|6.2|0x530
5.4|7|0x540
5.5|8|0x550
5.6|9|0x560
5.7|10|0x570
5.8|11|0x580
5.9|12|0x590
5.10|12.1|0x5100
5.11|12.2|0x5110
5.12|12.3|0x5120

The name of Oracle Solaris Studio has changed over the years (e.g. Sun Studio, Sun Workshop, Forte Developer) but we do not make this distinction in the table above.

## Pacific C ##

Type|Macro
---|---
Identification|`__PACIFIC__`

## Palm C/C++ ##

Type|Macro|Format|Description
---|---|--|---
Identification|`_PACC_VER`| |
Version|`_PACC_VER`|0xVRRPPBBB|V = Version<br/>RR = Revision<br/>PP = Patch<br/>BBB = Build

##### Example #####

Palm C/C++|`_PACC_VER`
---|---
1.0.0.13|0x1000000D

## [Pelles C](http://en.wikipedia.org/wiki/Pelles_C) ##

Type|Macro|Format|Description
---|---|---|---
Identification|`__POCC__`| |
Version|`__POCC__`|VRR|V = Version<br/>RR = Revision

##### Example #####

Pelles C|`__POCC__`
---|---
3.00|300

## [Portland Group C/C++](http://en.wikipedia.org/wiki/The_Portland_Group) ##

Type|Macro|Description
---|---|---
Identification|`__PGI`|
Version|`__PGIC__`|Version
Version|`__PGIC_MINOR__`|Revision
Version|`__PGIC_PATCHLEVEL__`|Patch

##### Example #####

PGI C/C++|`__PGIC__`|`__PGIC_MINOR__`|`__PGIC_PATCHLEVEL__`
---|---|---|---
7.0.1|7|0|1
11.9|11|9|0

## Renesas C/C++ ##

Type|Macro|Format|Description
---|---|---|---
Identification|`__RENESAS__`| |
Identification|`__HITACHI__`| |
Version|`__RENESAS_VERSION__`|0xVVRR|V = Version<br/>R = Revision<br/>P = Patch
Version|`__RENESAS_VERSION__`|0xVVRRPP00|From ?
Version|`__HITACHI_VERSION__`|0xVVRR|As above

##### Example #####

Renesas C/C++|`__HITACHI_VERSION__`|`__RENESAS_VERSION__`
---|---|---
5.1C|0x0501|
8.0|0x8000|0x8000
1.00.00| |0x01000000

## [SAS/C](http://www.sas.com/products/sasc/) ##

Type|Macro|Format|Description
---|---|---|---
Identification|`SASC`| |
Identification|`__SASC`| |
Identification|`__SASC__`| |
Version|`__VERSION__`| |Until ?
Version|`__REVISION__`| |Until ?
Version|`__SASC__`|VRR|V = Version<br/>RR = Revision<br/><br/>From ?

##### Example #####

SAS/C|`__SASC__`|`__VERSION__`|`__REVISION__`
---|---|---|---
5.10| |5|10
6.50|650| |

## [SCO OpenServer](http://en.wikipedia.org/wiki/SCO_OpenServer) ##

Type|Macro
---|---
Identification|`_SCO_DS`

## [Small Device C Compiler](http://en.wikipedia.org/wiki/Small_Device_C_Compiler) ##

Type|Macro|Format|Description
---|---|---|---
Identification|`SDCC`| |
Version|`SDCC`|VRP|V = Version<br/>R = Revision<br/>P = Patch

##### Example #####

SDCC Version|`SDCC` Macro
---|---
2.5.6|256

## [SN Compiler](http://en.wikipedia.org/wiki/SN_Systems) ##

Type|Macro
---|---
Identification|`__SNC__`

## [Stratus VOS C](http://en.wikipedia.org/wiki/Stratus_VOS) ##

Type|Macro|Description
---|---|---
Identification|`__VOSC__`|
Version|`__VOSC__`|0 = K&R compiler<br/>1 = ANSI C compiler

## Symantec C++ ##

Type|Macro|Format|Description
---|---|---|---
Identification|`__SC__`| |
Version|`__SC__`|0xVVRR|VV = Version<br/>RR = Revision

## [TenDRA C/C++](http://en.wikipedia.org/wiki/TenDRA_Compiler) ##

Type|Macro
---|---
Identification|`__TenDRA__`

## Texas Instruments C/C++ Compiler ##

Type|Macro|Format|Description
---|---|---|---
Identification|`__TI_COMPILER_VERSION__`| |
Identification|`_TMS320C6X`| |All C6000 compilers
Version|`__TI_COMPILER_VERSION__`|VVVRRRPPP|VVV = Version<br/>RRR = Revision<br/>PPP = Patch

##### Example #####

TI C/C++|`__TI_COMPILER_VERSION__`
---|---
4.9.1|4009001
7.3.1|7003001

## [THINK C](http://en.wikipedia.org/wiki/THINK_C) ##

Type|Macro|Description
---|---|---
Version|`THINKC3`|Version 3.x
Version|`THINKC4`|Version 4.x

## [Tiny C](http://en.wikipedia.org/wiki/Tiny_C_Compiler) ##

Type|Macro
---|---
Identification|`__TINYC__`

## [Turbo C/C++](http://en.wikipedia.org/wiki/Turbo_C) ##

Type|Macro|Format|Description
---|---|---|---
Identification|`__TURBOC__`| |
Version|`__TURBOC__`|0xVVRR|VV = Version<br/>RR = Revision<br/><br/>This pattern does not apply to the values between 0x295 and 0x400.

##### Example #####

Turbo C|Turbo C++|`__TURBOC__`
---|---|---
2.01| |0x201
|1.00|0x295
|1.01|0x296
|2.00|0x297

## Ultimate C/C++ ##

Type|Macro|Description
---|---|---
Identification|`_UCC`|
Version|`_MAJOR_REV` = V<br/>`_MINOR_REV` = R|V = Version<br/>R = Revision

##### Example #####

Ultimate C/C++|`_MAJOR_REV`|`_MINOR_REV`
---|---|---
2.1|2|1

## [USL C](http://en.wikipedia.org/wiki/Unix_System_Laboratories) ##

Type|Macro|Format|Description
---|---|---|---
Identification|`__USLC__`| |
Version|`__SCO_VERSION__`|VRRYYYYMM|V = Version<br/>RR = Revision<br/>YYYY = Year<br/>MM = Month

##### Example #####

USL C|`__SCO_VERSION__`|Description
---|---|---
3.2|302199801|
3.4|304200805|UnixWare 7.1.4 UDK C++ (CC)
4.2|402200805|UnixWare 7.1.4 UDK C (cc)

## [VBCC](http://en.wikipedia.org/wiki/Vbcc) ##

Type|Macro
---|---
Identification|`__VBCC__`

## [Watcom C++](http://en.wikipedia.org/wiki/Watcom) ##

Type|Macro|Format|Description
---|---|---|---
Identification|`__WATCOMC__`| |
Version|`__WATCOMC__`|VVRR|VV = Version<br/>RR = Revision

Notice that Watcom C++ became Open Watcom C++ after version 11.0, and the official version numbering (but not the version macro) was restated at version 1.0.

##### Example #####

Watcom C++|Open Watcom C++|`__WATCOMC__`
---|---|---
10.5| |1050
11.0| |1100
|1.0|1200
|1.7|1270

## [Zortech C++](http://en.wikipedia.org/wiki/Zortech) ##

Type|Macro|Format|Description
---|---|---|---
Identification|`__ZTC__`| |
Version|`__ZTC__`|0xVRP|V = Version<br/>R = Revision<br/>P = Patch
