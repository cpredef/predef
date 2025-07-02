# Pre-defined C/C++ Compiler Macros #

The macros are found here:

* [Standards](Standards.md)
* [Compilers](Compilers.md)
* [Libraries](Libraries.md)
* [Operating systems](OperatingSystems.md)
* [Architectures](Architectures.md)

General guidelines are found here:

* [Version normalization](VersionNormalization.md)
* [Feature macros](FeatureMacros.md)
* [Endianness](Endianness.md)

Please send updates/corrections to [predef-contribute](mailto:predef-contribute@lists.sourceforge.net) or through pull requests on GitHub.

## Introduction ##

C and C++ compilers automatically define certain macros that can be used to check for compiler or operating system features. This is useful when writing portable software.

These pages lists various pre-defined compiler macros that can be used to identify standards, compilers, operating systems, hardware architectures, and even basic run-time libraries at compile-time.

For example, if we want to use a generic or opaque pointer type, we use void pointers. However, ancient K&R compilers (from the time before the first ANSI C standard) do not support void pointers. Instead we can define our own type:

```c
#if defined(__STDC__) || defined(__cplusplus) || defined(_MSC_EXTENSIONS)
typedef void * t_pointer;
#else
typedef char * t_pointer;
#endif
```

Another example, Microsoft Visual C++ version 4.2 added a pragma to reduce compilation times by only including a file once (if <code>_MSC_VER</code> is not defined then it will evaluate to 0 (zero) — however, some compilers may complain about an undefined macro)

```c
#if defined(_MSC_VER) && (_MSC_VER >= 1020)
#pragma once
#endif
```

The macros contained in these pages have been obtained through vendor documentation, the [defines script](http://predef.sourceforge.net/defines.txt), contributors, and third-party source code. No guarantee about the correctness of the macros is given.

An often-used alternative is [Autoconf](http://www.gnu.org/software/autoconf/), which is a more powerful tool to examine various types of features, including compilation options. However, Autoconf is fairly Unix-centric, and requires a Unix layer on other platforms (e.g. Cygwin on Windows). Other alternatives are [Buildtool](http://buildtool.sourceforge.net/), [CMake](http://www.cmake.org/), [SCons](http://www.scons.org/), [PMK](http://pmk.sourceforge.net/), [Jam](http://www.perforce.com/jam/jam.html), [Ant](http://ant.apache.org/), and [Bakefile](http://bakefile.sourceforge.net/).

## Contributors ##

Bjorn Reese, Daniel Stenberg, Greg Roelofs, Steven G. Johnson, Wlodzimierz ABX Skiba, Marc Finet, Philip Newton, Mitchell Charity, Christian Klutz, Seo Sanghyeon, Chris Adami, Geoff Clare, Dan Fandrich, Mike Gorchak, Yuri D'Elia, Gynvael Coldwind, Alain Tauch, Vadim Zeitlin, Steve White, Thomas David Rivers, Tom Honermann, Martin Mitas, Dinesh Chhadwa, Erik Faye-Lund, Leo Davis, Paul Hsieh, Roland Schwarz, Darko Kolakovic, Andy Buonviri, Ming Kin Lai, Kent Johnson, Helmut Bauer, Oliver Schneider, Ron Pimblett, Jose Luis Rodriguez Garcia, Jeroen Ruigrok van der Werven, Uffe Jakobsen, Bryan Ashby, Bruno Haible, Artur Bac, Terry Schwarz, Leo Davis, Markus Duft, William Dang, Paul Green, Ruben Van Boxem, Pau Garcia i Quiles, Mikulas Patocka, Leo Davis, Mark Ferry, Holger Machens, Simon Watts, Paul Hargrove, Hans-Christoph Steiner, Gerald Combs, Denys Bulant, Massimo Morara, Jeremy Bennett, Guillem Jover, Riku Voipio, Jacques Pelletier, Mark Jarvin, Georg Sauthoff, Scot Jenkins, Grzegorz Brzęczyszczykiewicz, John Dallman, Gianmichele Toglia, Robbie Groenewoudt, Andreas Mohr, Алексей Пюрецкий, Sverre Hvammen Johansen, Stefan Tauner, Daniel Garcia, Ozkan Sezer, Dean Saridakis, Frank Long, Kevin Adler, Lisa Felidae.
