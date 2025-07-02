Please send updates/corrections to [predef-contribute](mailto:predef-contribute@lists.sourceforge.net) or through pull requests on GitHub.

## [AIX](http://en.wikipedia.org/wiki/AIX_operating_system) ##

Type|Macro|Description
---|---|---
Identification|`_AIX`|
Version|`_AIX'VR'`|V = Version<br/>R = Revision
Identification|`__TOS_AIX__`|Defined by xlC

##### Example #####

If `_AIX` is defined, then the following macros can be used to determine the version. Notice that the macros indicates the mentioned version or higher. For example, if `_AIX43` is defined, then `_AIX41` will also be defined.

AIX Version|Macro
--|---
3.2.x|`_AIX3`<br/>`_AIX32`
4.1|`_AIX41`
4.3|`_AIX43`

## [Android](http://en.wikipedia.org/wiki/Android_%28operating_system%29) ##

Type|Macro|Format|Description
---|---|---|--
Identification|`__ANDROID__`| |
Version|`__ANDROID_API__`|V|V = API Version<br/><br/>Must be included from `<android/api-level.h>`

Notice that Android uses Linux kernel, and that the Linux macros also are defined for Android.

##### Example #####

Android Version|`__ANDROID_API__`
---|---
1.0|1
1.1|2
1.5|3
1.6|4
2.0|5
2.0.1|6
2.1|7
2.2|8
2.3|9
2.3.3|10
3.0|11

## [Amdahl UTS](http://en.wikipedia.org/wiki/UTS_%28Mainframe_UNIX%29) ##

Type|Macro
---|---
Identification|`UTS`

## [AmigaOS](http://en.wikipedia.org/wiki/AmigaOS) ##

Type|Macro|Description
---|---|---
Identification|`AMIGA`|
Identification|`__amigaos__`|Defined by GNU C

## [Apollo AEGIS](http://en.wikipedia.org/wiki/Domain/OS) ##

Type|Macro
--|---
Identification|`aegis`

## [Apollo Domain/OS](http://en.wikipedia.org/wiki/Domain/OS) ##

Type|Macro
---|---
Identification|`apollo`

## [AROS](https://en.wikipedia.org/wiki/AROS_Research_Operating_System) ##

Originally *Amiga Research Operating System*, later renamed to *AROS Research Operating System*.

Type|Macro
---|---
Identification|`__AROS__`

## [Bada](http://en.wikipedia.org/wiki/Bada_%28operating_system%29) ##

Based on Nucleus OS.

## [BeOS](http://en.wikipedia.org/wiki/BeOS) ##

Type|Macro|Format|Description
---|---|---|---
Identification|`__BEOS__`| |
Version|`B_BEOS_VERSION`|0xVVRR|VV = Version<br/>RR = Revision<br/><br/>Must be included from [`<BeBuild.h>`](https://git.haiku-os.org/haiku/tree/headers/os/BeBuild.h)

## [Blue Gene](http://en.wikipedia.org/wiki/Bluegene) ##

Type|Macro|Description
---|---|---
Identification|`__bg__`|All Blue Gene systems<br/><br/>Defined by XL C/C++ and GNU C
Version|`__bgq__`|Blue Gene/Q<br/><br/>Defined for XL C/C++ and GNU C
Identification|`__THW_BLUEGENE__`|All Blue Gene systems<br/><br/>Defined by XL C/C++
Version|`__TOS_BGQ__`|Blue Gene/Q<br/><br/>Defined by XL C/C++

## [BSD Environment](http://en.wikipedia.org/wiki/Bsd) ##

Type|Macro|Format|Description
---|---|---|---
Identification|`__FreeBSD__`<br/>`__NetBSD__`<br/>`__OpenBSD__`<br/>`__bsdi__`<br/>`__DragonFly__`<br/>`__MidnightBSD__`| |
Version|`BSD`|YYYYMM|YYYY = Year<br/>MM = Month<br/><br/>Must be included from `<sys/param.h>`
Version|`BSD4_2`<br/>`BSD4_3`<br/>`BSD4_4`| |Must be included from `<sys/param.h>`
Identification|`_SYSTYPE_BSD`| |Defined by DEC C

##### Example #####

Version|`BSD`|Macro
---|---|--
4.3 Net2|199103|
4.4|199306|`BSD4_4`
4.4BSD-Lite2|199506|

## [BSD/OS](http://en.wikipedia.org/wiki/BSD/OS) ##

Type|Macro
---|---
Identification|`__bsdi__`

## [ConvexOS](http://en.wikipedia.org/wiki/Convex_Computer) ##

Type|Macro
---|---
Identification|`__convex__`

## [CP/M](http://en.wikipedia.org/wiki/CP/M) ##

Type|Macro|Format|Description
---|---|---|---
Identification|`__CPM`||Defined by Z88DK
Identification|`CPM`||Defined by Z88DK

## [Cygwin Environment](http://en.wikipedia.org/wiki/Cygwin) ##

Type|Macro
---|---
Identification|`__CYGWIN__`

## [DG/UX](http://en.wikipedia.org/wiki/Data_General) ##

Type|Macro
---|---
Identification|`DGUX`
Identification|`__DGUX__`
Identification|`__dgux__`

## [DragonFly](http://en.wikipedia.org/wiki/DragonFly_BSD) ##

Type|Macro
---|---
Identification|`__DragonFly__`

## [DYNIX/ptx](http://en.wikipedia.org/wiki/Dynix) ##

Type|Macro
---|---
Identification|`_SEQUENT_`
Identification|`sequent`

## [eCos](http://en.wikipedia.org/wiki/ECos) ##

Type|Macro
---|---
Identification|`__ECOS`

## [Emscripten](https://en.wikipedia.org/wiki/Emscripten) ##

Type|Macro|Format|Description
---|---|---|---
Identification|`EMSCRIPTEN`| |From Emscripten 1.0.1a until Emscripten 1.30.6
Identification|`__EMSCRIPTEN__`| |From Emscripten 1.3.7
Version|`__EMSCRIPTEN_major__`|V|V = Major version<br/><br/>From Emscripten 1.21.4<br/><br/>Must be included from `<emscripten/version.h>`
Version|`__EMSCRIPTEN_minor__`|R|R = Minor version<br/><br/>From Emscripten 1.21.4<br/><br/>Must be included from `<emscripten/version.h>`
Version|`__EMSCRIPTEN_tiny__`|P|P = Patch level<br/><br/>From Emscripten 1.21.4<br/><br/>Must be included from `<emscripten/version.h>`

For more information see [Detecting Emscripten in Preprocessor](https://emscripten.org/docs/compiling/Building-Projects.html#detecting-emscripten-in-preprocessor)

##### Example #####

Version|`__EMSCRIPTEN_major__`|`__EMSCRIPTEN_minor__`|`__EMSCRIPTEN_tiny__`
---|---|---|---
3.1.41|3|1|41
3.1.41-git|3|1|41

## [EMX Environment](http://en.wikipedia.org/wiki/EMX_%28programming_environment%29) ##

Type|Macro
---|---
Identification|`__EMX__`

## [FreeBSD](http://en.wikipedia.org/wiki/FreeBSD) ##

Type|Macro|Format|Description
---|---|---|---
Identification|`__FreeBSD__`| |
Identification|`__FreeBSD_kernel__`| |From FreeBSD 8.3, 9.1, and 10.0.[1](http://svnweb.freebsd.org/base/head/sys/sys/param.h?view=markup)
Version|`BSD`| |
Version|`__FreeBSD__`|V|V = Version
Version|`__FreeBSD_version`|?|Must be included from `<sys/param.h>`

##### Example #####

FreeBSD|`__FreeBSD__`|`__FreeBSD_version`
---|---|---
1.x|1|
2.0-RELEASE|2|119411
2.2-RELEASE|2|220000
3.0-RELEASE|3|300005
4.0-RELEASE|4|400017
4.5-RELEASE|4|450000

For more information see the [FreeBSD porters handbook](https://docs.freebsd.org/en/books/porters-handbook/versions/).

## [Fuchsia](https://en.wikipedia.org/wiki/Fuchsia_(operating_system)) ##

Type|Macro|Format|Description
----|-----|------|-----------
Identification|`__Fuchsia__`|| [1](https://github.com/llvm/llvm-project/blob/5f8cefebd900bbbd96961162ed9b80056e2ab95f/clang/lib/Basic/Targets/OSTargets.h#L928-L937)
Version|`__Fuchsia_API_level__`|V|V = API level [1](https://fuchsia.dev/fuchsia-src/contribute/governance/rfcs/0002_platform_versioning)

## GNU aka [GNU/Hurd](http://en.wikipedia.org/wiki/GNU/Hurd) ##

The official name of this operating system is GNU. Hurd is the kernel in the GNU operating system. It is often listed as GNU/Hurd since there is also GNU/Linux and GNU/kFreeBSD, which are most of the GNU operating system with the Linux and FreeBSD kernels respectively.

Type|Macro
---|---
Identification|`__GNU__` [1](http://gcc.gnu.org/viewcvs/trunk/gcc/config/gnu.h?view=markup)
Identification|`__gnu_hurd__` [1](http://gcc.gnu.org/viewcvs/trunk/gcc/config/gnu.h?view=markup)

## [GNU/kFreeBSD](http://en.wikipedia.org/wiki/GNU/kFreeBSD) ##

GNU/kFreeBSD is one of the Debian distros that is based on the FreeBSD kernel rather than the Linux or Hurd kernels.

Type|Macro
---|---
Identification|`__FreeBSD_kernel__` `&&` `__GLIBC__`

Notice that FreeBSD also defines `__FreeBSD_kernel__` so the `__GLIBC__` macro must be checked to distinguish it.

## [GNU/Linux](http://en.wikipedia.org/wiki/GNU/Linux) ##

Type|Macro
---|---
Identification|`__gnu_linux__`

## [Haiku](https://en.wikipedia.org/wiki/Haiku_%28operating_system%29) ##

Type|Macro|Format|Description
---|---|---|---
Identification|`__HAIKU__`| |
Version|`B_HAIKU_VERSION_'V'`|0x00VV0000|VV = Version<br/><br/>Defined in advance before being reached.<br/><br/>Must be included from [`<BeBuild.h>`](https://git.haiku-os.org/haiku/tree/headers/os/BeBuild.h)
Version|`B_HAIKU_VERSION`|0x00VVRRPP|VV = Version<br/>RR = Revision (Alpha and Beta ordering for VV+1)<br/>PP = Pre (0 or 1 if before RR+1)<br/><br/>Must be included from [`<BeBuild.h>`](https://git.haiku-os.org/haiku/tree/headers/os/BeBuild.h)

##### Example #####

Haiku|`B_HAIKU_VERSION`
---|---
1 Alpha 1|`B_HAIKU_VERSION_1_ALPHA_1` = 0x00000100
1 Alpha 4|`B_HAIKU_VERSION_1_ALPHA_4` = 0x00000400
1 Beta 1|`B_HAIKU_VERSION_1_BETA_1` = 0x00000500
Git version before 1 Beta 4|`B_HAIKU_VERSION_1_PRE_BETA_4` = 0x00000701
1 |`B_HAIKU_VERSION_1` = 0x00010000

## [HI-UX MPP](http://en.wikipedia.org/wiki/HI-UX) ##

Type|Macro
---|---
Identification|`__hiuxmpp`

## [HP-UX](http://en.wikipedia.org/wiki/HP-UX) ##

Type|Macro|Description
---|---|---
Identification|`_hpux`|Defined by HP UPC
Identification|`hpux`|
Identification|`__hpux`|

## [IBM OS/400](http://en.wikipedia.org/wiki/IBM_i) ##

Type|Macro|Format|Description
---|---|---|---
Identification|`__OS400__`||
Version|`__OS400_TGTVRM__`|VRM|V = Version<br/>R = Revision<br/>M = Modification

## [illumos](https://illumos.org) ##

Type|Macro|Description
---|---|---
Identification|`__illumos__`|See also: [13726 distinguish ourselves with a macro](https://www.illumos.org/issues/13726)
Identification|`sun`|Shared with Solaris; use not recommended
Identification|`__sun`|Shared with Solaris; use not recommended

Note that illumos forked from Solaris in ~2010, but continues to provide the identifying definitions that Solaris provided at the point of the fork.

## [INTEGRITY](http://en.wikipedia.org/wiki/Integrity_%28operating_system%29) ##

Type|Macro
---|---
Identification|`__INTEGRITY`

## [Interix Environment](http://en.wikipedia.org/wiki/Interix) ##

Type|Macro|Description
---|---|---
Identification|`__INTERIX`|Defined by GNU C and Visual C++

## [IRIX](http://en.wikipedia.org/wiki/Irix) ##

Type|Macro
---|---
Identification|`sgi`
Identification|`__sgi`

## [Linux kernel](http://en.wikipedia.org/wiki/Linux_kernel) ##

Systems based on the Linux kernel define these macros. There are two major Linux-based operating systems: [GNU/Linux](http://en.wikipedia.org/wiki/GNU/Linux) and [Android](http://en.wikipedia.org/wiki/Android), and numerous others like [Ångström](http://www.angstrom-distribution.org/) or [OpenEmbedded](http://www.openembedded.org)

Type|Macro|Description
---|---|---
Identification|`__linux__`| [1](http://www.faqs.org/docs/Linux-HOWTO/GCC-HOWTO.html#INDEX.25)
Identification|`linux`|Obsolete (not POSIX compliant)
Identification|`__linux`|Obsolete (not POSIX compliant)

## [LynxOS](http://en.wikipedia.org/wiki/LynxOS) ##

Type|Macro
---|---
Identification|`__Lynx__`

## [MacOS](http://en.wikipedia.org/wiki/Mac_OS) ##

Type|Macro|Description
---|---|---
Identification|`macintosh`|Mac OS 9
Identification|`Macintosh`|Mac OS 9
Identification|`__APPLE__` `&&` `__MACH__`|Mac OS X<br/><br/>Defined by GNU C and Intel C++

## [Microware OS-9](http://en.wikipedia.org/wiki/OS-9) ##

Type|Macro|Description
---|---|---
Identification|`__OS9000`|Defined by Ultimate C/C++
Identification|`_OSK`|Defined by Ultimate C/C++

## [MidnightBSD](https://en.wikipedia.org/wiki/MidnightBSD)

Type|Macro|Description
---|---|---
Identification|`__MidnightBSD__`
Identification|`__MidnightBSD_kernel__`
Version|`BSD`
Version|`__MidnightBSD_version`|Must be included from `<sys/param.h>`

## [MINIX](http://en.wikipedia.org/wiki/Minix) ##

Type|Macro
---|---
Identification|`__minix`

## [MiNT](https://en.wikipedia.org/wiki/MiNT) ##

Originally *MiNT is Not TOS*, later renamed to *MiNT is Now TOS*.

Type|Macro
---|---
Identification|`__MINT__`

## [MorphOS](http://en.wikipedia.org/wiki/Morphos) ##

Type|Macro
---|---
Identification|`__MORPHOS__`

## [MPE/iX](http://en.wikipedia.org/wiki/MPE) ##

Type|Macro
---|---
Identification|`mpeix`
Identification|`__mpexl`

## [MSDOS](http://en.wikipedia.org/wiki/MS-DOS) ##

Type|Macro
---|---
Identification|`MSDOS`
Identification|`__MSDOS__`
Identification|`_MSDOS`
Identification|`__DOS__`

## [MSX](http://en.wikipedia.org/wiki/MSX) ##

Type|Macro|Format|Description
---|---|---|---
Identification|`__MSX`||Defined by Z88DK
Identification|`MSX`||Defined by Z88DK

## [Native Client](https://en.wikipedia.org/wiki/Google_Native_Client) ##

Type|Macro
---|---
Identification|`__native_client__`

## [NetBSD](http://en.wikipedia.org/wiki/NetBSD) ##

Type|Macro|Format|Description
---|---|---|---
Identification|`__NetBSD__`| |
Version|`BSD`| |
Version|`NetBSD'V'_'R'`| |V = Version<br/>R = Revision<br/><br/>Must be included from `<sys/param.h>`
Version|`__NetBSD_Version__`|VVRRAAPP00|VV = Version<br/>RR = Revision<br/>AA = Release<br/>PP = Patch<br/><br/>From NetBSD 1.2D (?) until NetBSD 2.0H<br/><br/>Must be included from `<sys/param.h>`
Version|`__NetBSD_Version__`|VVRR00PP00|VV = Version<br/>RR = Revision<br/>PP = Patch<br/><br/>From NetBSD 2.99.9<br/><br/>Must be included from `<sys/param.h>`

##### Example #####

NetBSD|`__NetBSD_Version__`|Macro
---|---|--
0.8| |`NetBSD0_8`
0.9| |`NetBSD0_9`
1.0| |`NetBSD1_0` = 1
1.0A| |`NetBSD1_0` = 2
1.2D|102040000|
1.2.1|102000100|

## [NeXTSTEP](http://en.wikipedia.org/wiki/NeXTSTEP) ##

Type|Macro
---|---
Identification|`NeXT`

## [NonStop](http://en.wikipedia.org/wiki/NonStop) ##

Type|Macro
---|---
Identification|`__TANDEM`

## [Nucleus RTOS](http://en.wikipedia.org/wiki/Nucleus_RTOS) ##

Type|Macro
---|---
Identification|`__nucleus__`

## [OpenBSD](http://en.wikipedia.org/wiki/OpenBSD) ##

Type|Macro|Format|Description
---|---|---|---
Identification|`__OpenBSD__`| |
Version|`BSD`| |
Version|`OpenBSD'V'_'R'`| |V = Version<br/>R = Revision<br/><br/>Must be included from `<sys/param.h>`

##### Example #####

OpenBSD|Macro
---|---
3.1|`OpenBSD3_1`
3.9|`OpenBSD3_9`

## [OS/2](http://en.wikipedia.org/wiki/OS/2) ##

Type|Macro
---|---
Identification|`OS2`
Identification|`_OS2`
Identification|`__OS2__`
Identification|`__TOS_OS2__`

## [Palm OS](http://en.wikipedia.org/wiki/Palmos) ##

Type|Macro|Description
---|---|---
Identification|`__palmos__`|Defined by GNU C in [PRC-Tools](http://prc-tools.sourceforge.net/)

## [Plan 9](http://en.wikipedia.org/wiki/Plan_9_from_Bell_Labs) ##

Type|Macro
---|---
Identification|`EPLAN9`

## [Pyramid DC/OSx](http://en.wikipedia.org/wiki/DC/OSx) ##

Type|Macro
---|---
Identification|`pyr`

## [QNX](http://en.wikipedia.org/wiki/QNX) ##

Type|Macro|Format|Description
---|---|---|---
Identification|`__QNX__`| |QNX 4.x, 7.x, 8.x
Identification|`__QNXNTO__`| |QNX 6.x
Version|`_NTO_VERSION`|VRR|V = Version<br/>RR = Revision<br/><br/>Only available when `__QNXNTO__` is defined.<br/><br/>Must be included from `<sys/neutrino.h>`
Version|`BBNDK_VERSION_CURRENT`|VVRRRRPPPP|V = Version<br/>RRRR = Revision<br/>PPPP = Patch<br/><br/>Only available on [Blackberry 10](http://en.wikipedia.org/wiki/Blackberry_10)<br/><br/>From Blackberry 10.1.0<br/><br/>Must be included from `<bbndk.h>`

##### Example #####

QNX|`_NTO_VERSION`
---|---
6.2|620

## [Reliant UNIX](http://en.wikipedia.org/wiki/Reliant_UNIX) ##

Type|Macro
---|---
Identification|`sinux`

## [SCO OpenServer](http://en.wikipedia.org/wiki/SCO_OpenServer) ##

Type|Macro|Description
---|---|---
Identification|`M_I386`|Defined by GNU C
Identification|`M_XENIX`|Defined by GNU C
Identification|`_SCO_DS`|

## [SerenityOS](https://serenityos.org/) ##

Type|Macro|Description
----|-----|-----------
Identification|`__serenity__`|Defined by [GNU C](https://github.com/SerenityOS/serenity/blob/d2b887a793397a7a22c7ba50e7f6cb704f809446/Toolchain/Patches/gcc/0001-Add-a-gcc-driver-for-SerenityOS.patch#L129) and [Clang](https://github.com/SerenityOS/serenity/blob/d2b887a793397a7a22c7ba50e7f6cb704f809446/Toolchain/Patches/llvm/0003-Driver-Add-support-for-SerenityOS.patch#L68)

## [Solaris](http://en.wikipedia.org/wiki/Solaris_Operating_Environment) ##

Type|Macro|Description
---|---|---
Identification|`sun`|
Identification|`__sun`|
Version|`__'System'_'Version'`|System = `uname -s`<br/>Version = `uname -r`<br/>Any illegal character is replaced by an underscore.<br/><br/>Defined by Sun Studio

Use the SVR4 macros to distinguish between Solaris and SunOS.

```c
#if defined(sun) || defined(__sun)
# if defined(__SVR4) || defined(__svr4__)
/* Solaris */
# else
/* SunOS */
# endif
#endif
```

##### Example #####

Solaris|Macro
---|---
2.7|`__SunOS_5_7`
8 |`__SunOS_5_8`

## [Stratus VOS](http://en.wikipedia.org/wiki/Stratus_VOS) ##

Type|Macro|Format|Description
---|---|---|---
Identification|`__VOS__`| |
Version|`__VOS__`|V|V = Version

Notice that the `__VOS__` macro is defined by the compiler, but as several compilers can co-exist in the same OS release, the version number is not reliable.

## [SVR4 Environment](http://en.wikipedia.org/wiki/UNIX_System_V) ##

Type|Macro|Description
---|---|---
Identification|`__sysv__`|
Identification|`__SVR4`|
Identification|`__svr4__`|
Identification|`_SYSTYPE_SVR4`|Defined on IRIX

## [Syllable](http://en.wikipedia.org/wiki/Syllable_Desktop) ##

Type|Macro
---|---
Identification|`__SYLLABLE__`

## [Symbian OS](http://en.wikipedia.org/wiki/Symbian_OS) ##

Type|Macro
---|---
Identification|`__SYMBIAN32__`

## [Tru64 (OSF/1)](http://en.wikipedia.org/wiki/Digital_UNIX) ##

Type|Macro
---|---
Identification|`__osf__`
Identification|`__osf`

## [Ultrix](http://en.wikipedia.org/wiki/Ultrix) ##

Type|Macro
---|---
Identification|`ultrix`
Identification|`__ultrix`
Identification|`__ultrix__`
Identification|`unix` & `vax`

## [UNICOS](http://en.wikipedia.org/wiki/UNICOS) ##

Type|Macro|Format|Description
---|---|---|---
Identification|`_UNICOS`| |
Version|`_UNICOS`|V|V = Version

## [UNICOS/mp](http://en.wikipedia.org/wiki/Unicos) ##

Type|Macro|Description
---|---|---
Identification|`_CRAY`<br/>`__crayx1`|

## [UNIX Environment](http://en.wikipedia.org/wiki/Unix) ##

Type|Macro
---|---
Identification|`__unix__`
Identification|`__unix`

Notice that not all compilers defines these macros, e.g. the xlC or the DEC C/C++ compiler, so it may be better to use the POSIX or X/Open standard macros instead.

## [UnixWare](http://en.wikipedia.org/wiki/UnixWare) ##

Type|Macro
---|---
Identification|`sco`
Identification|`_UNIXWARE7`

## [U/Win Environment](http://en.wikipedia.org/wiki/UWIN) ##

Type|Macro
---|---
Identification|`_UWIN`

## [VMS](http://en.wikipedia.org/wiki/Vms) ##

Type|Macro|Format|Description
---|---|---|---
Identification|`VMS`| |
Identification|`__VMS`| |
Version|`__VMS_VER`|VVRREPPTT|VV = Version<br/>RR = Revision<br/>E = Edit number<br/>PP = Patch (01 = A, ... 26 = Z)<br/>TT = Type (22 = official)

##### Example #####

VMS|`__VMS_VER`
---|---
6.1|60100022
6.2|60200022
6.2-1I|60210922

## [VxWorks](http://en.wikipedia.org/wiki/VxWorks) ##

Type|Macro|Description
---|---|---
Identification|`__VXWORKS__`|Defined by GNU C and Diab (from ?)
Identification|`__vxworks`|Defined by GNU C and Diab (from ?)
Version|`_WRS_VXWORKS_MAJOR`|Version<br/><br/>Must be included from `<version.h>`
Version|`_WRS_VXWORKS_MINOR`|Revision<br/><br/>Must be included from `<version.h>`
Version|`_WRS_VXWORKS_MAINT`|Patch/maintenance<br/><br/>Must be included from `<version.h>`
Mode|`__RTP__`|For real-time mode
Mode|`_WRS_KERNEL`|For kernel mode

##### Example #####

VxWorks|`_WRS_VXWORKS_MAJOR`|`_WRS_VXWORKS_MINOR`|`_WRS_VXWORKS_MAINT`
---|---|---|---
6.2|6|2|0

## [Windows](http://en.wikipedia.org/wiki/Category:Microsoft_Windows) ##

Type|Macro|Description
---|---|---
Identification|`_WIN16`|Defined for 16-bit environments [1](http://msdn.microsoft.com/en-us/library/ff540443.aspx)
Identification|`_WIN32`|Defined for both 32-bit and 64-bit environments [1](http://msdn.microsoft.com/en-us/library/ff540443.aspx)
Identification|`_WIN64`|Defined for 64-bit environments [1](http://msdn.microsoft.com/en-us/library/ff540443.aspx)
Identification|`__WIN32__`|Defined by Borland C++
Identification|`__TOS_WIN__`|Defined by xlC
Identification|`__WINDOWS__`|Defined for 16-bit-environments by Watcom C/C++ [1](https://github.com/open-watcom/open-watcom-v2/blob/e71622efc810f8cdfd538a85a97eccee8c4feece/bld/cc/c/coptions.c#L357-L360)

## [Windows CE](http://en.wikipedia.org/wiki/Windows_CE) ##

Type|Macro|Format|Description
---|---|---|---
Identification|`_WIN32_WCE`| |Defined by Embedded Visual C++
Version|`_WIN32_WCE`|VRR|V = Version<br/>R = Revision
Identification|`WIN32_PLATFORM_'P'`| |P = Platform
Version|`WIN32_PLATFORM_'P'`|V|P = Platform<br/>V = Version

##### Example #####

Version|`_WIN32_WCE`
---|---
2.01|201
2.11|211
3.0|300
4.0|400
4.1|410
4.2|420
5.0|501

Platform|Macro|Value
---|---|---
H/PC 2000|`WIN32_PLATFORM_HPC2000`|
H/PC Pro 2.11|`WIN32_PLATFORM_HPCPRO`|211
H/PC Pro 3.0|`WIN32_PLATFORM_HPCPRO`|300
Pocket PC|`WIN32_PLATFORM_PSPC`|1
Pocket PC 2002|`WIN32_PLATFORM_PSPC`|310
Windows Mobile 2003|`WIN32_PLATFORM_PSPC`|400
Smartphone 2002|`WIN32_PLATFORM_WFSP`|100

## [Wind/U Environment](http://en.wikipedia.org/wiki/Bristol_Technology_Inc.) ##

Type|Macro|Format|Description
---|---|---|---
Identification|`_WINDU_SOURCE`| |
Version|`_WINDU_SOURCE`|0xVVRRPP|VV = Version<br/>RR = Revision<br/>PP = Patch

##### Example #####

Wind/U|`_WINDU_SOURCE`
---|---
3.1.2|0x030102

## [MVS/ESA, OS/390 and z/OS](http://en.wikipedia.org/wiki/Z/OS) ##

Type|Macro|Description
---|---|---
Identification|`__MVS__`|Host
Identification|`__HOS_MVS__`|Host
Identification|`__TOS_MVS__`|Target

## [VM/ESA and z/VM](https://en.wikipedia.org/wiki/VM_(operating_system)) ##

Type|Macro|Description
---|--|--
Identification|`__VM__`|Host
Identification|`__HOS_VM__`|Host
Identification|`__TOS_VM__`|Target