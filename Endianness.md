## Introduction ##

[Endianness](http://en.wikipedia.org/wiki/Endianness) is the order of the bytes in multi-byte data types, such as `int` or `float`. It may vary from processor to processor, and even from operating system to operating system. Detecting the correct endianness is difficult for several reasons:

* [Bi-endianness](http://en.wikipedia.org/wiki/Endianness#Bi-endian_hardware): Some processors support multiple endian modes, even to the extent of allowing dynamically changing between big and little-endian.
* [Middle-endianness](http://en.wikipedia.org/wiki/Endianness#Middle-endian): The two most common types of endianness are byte-swapped big-endian (ABCD) and byte-swapped little-endian (DCBA), but some older processors use other types. For instance, [PDP-11](http://en.wikipedia.org/wiki/PDP-11) used word-swapped little-endian (BADC), and [Honeywell 316](http://en.wikipedia.org/wiki/Honeywell_316) used word-swapped big-endian (CDAB).
* Integer vs floating-point: Some processors use a different endian model for integers versus floating-point values.
* Processor vs operating system: Most operating systems follow the endianness of the underlying hardware, but some (e.g. [VOS](http://en.wikipedia.org/wiki/Stratus_VOS)) retain their historic big-endian environment even when ported to little-endian processors.

## Recommendations ##

Some compilers or system headers provide macros to determine endianness, but they are difficult to use correctly, so we suggest that you follow this prioritized list of advice:

* Avoid endianness whenever possible.
* Use endian-neutral code (see example below.)
* Use existing conversion functions, such as `htons()` to convert between network byte-order and the native byte-order of the processor.
* Detect endianness at run-time (see example below.)
* Detect endianness at configuration-time, for example by using the Autoconf `AC_C_BIGENDIAN` feature. While this method works well when the same platform is used to build and host (execute) the package, you must take care when using autoconf in a cross-development environment, as the endianness of the build and host platforms may not be identical.
* Detect endianness at compile-time. There are several options:
* Use system header.
* Use pre-defined endian macros.
* Use pre-defined processor macros.

## Endian-neutral code ##

When endianness is needed for (de)marshalling binary data, you can write endian-neutral conversion as follows. Please notice that the code assume that the exchange format is big-endian (network byte-order). These functions can easily be adapted to other integer types, simply by changing the type at the `/* Type */` comments.

```c
#include <limits.h>

/* Type */ unsigned int
endian_native_unsigned_int(/* Type */ unsigned int net_number)
{
/* Type */ unsigned int result = 0;
int i;

for (i = 0; i < (int)sizeof(result); i++) {
result <<= CHAR_BIT;
result += (((unsigned char *)&net_number)[i] & UCHAR_MAX);
}
return result;
}

/* Type */ unsigned int
endian_net_unsigned_int(/* Type */ unsigned int native_number)
{
/* Type */ unsigned int result = 0;
int i;

for (i = (int)sizeof(result) - 1; i >= 0; i--) {
((unsigned char *)&result)[i] = native_number & UCHAR_MAX;
native_number >>= CHAR_BIT;
}
return result;
}
```

## Detect endianness at run-time ##

```c
#include <stdint.h>

enum {
ENDIAN_UNKNOWN,
ENDIAN_BIG,
ENDIAN_LITTLE,
ENDIAN_BIG_WORD, /* Middle-endian, Honeywell 316 style */
ENDIAN_LITTLE_WORD /* Middle-endian, PDP-11 style */
};

int endianness(void)
{
union
{
uint32_t value;
uint8_t data[sizeof(uint32_t)];
} number;

number.data[0] = 0x00;
number.data[1] = 0x01;
number.data[2] = 0x02;
number.data[3] = 0x03;

switch (number.value)
{
case UINT32_C(0x00010203): return ENDIAN_BIG;
case UINT32_C(0x03020100): return ENDIAN_LITTLE;
case UINT32_C(0x02030001): return ENDIAN_BIG_WORD;
case UINT32_C(0x01000302): return ENDIAN_LITTLE_WORD;
default: return ENDIAN_UNKNOWN;
}
}
```

The example above uses exact-width integer types. These types are optional if the underlying hardware does not support them. In that case the example will fail to compile. If you want the example to work in this case too, we suggest that you use the corresponding minimum-width integer types, e.g. `uint_least8_t` and `uint_least32_t`, and return ENDIAN_UNKNOWN if `sizeof(uint_least8_t) != 1` and `sizeof(uint_least32_t) != 4`.

## Detect endianness at compile-time ##

Please notice that the follow list of macros is not exhaustive.

##### System headers #####

Some compilers or system headers provide macros to specify endianness. Unfortunately, there is no standard for the names of the macros or even of the header files. Many operating systems contains the following macros in `<sys/param.h>`. Operating systems that use the GNU C library generally provide a header named `<endian.h>` containing these macros.

Type|Macro|Value
---|---|---
Big endian|`__BYTE_ORDER`|`__BIG_ENDIAN`
Little endian|`__BYTE_ORDER`|`__LITTLE_ENDIAN`
Little endian (word-swapped)|`__BYTE_ORDER`|`__PDP_ENDIAN`

##### Pre-defined endian macros #####

Type|Macro|Value
---|---|---
Big endian|`__BIG_ENDIAN__`<br/>`__ARMEB__`<br/>`__THUMBEB__`<br/>`__AARCH64EB__`<br/>`_MIPSEB`<br/>`__MIPSEB`<br/>`__MIPSEB__`|
Big endian|`__BYTE_ORDER__`|`__ORDER_BIG_ENDIAN__`
Big endian|`__FLOAT_WORD_ORDER__`|`__ORDER_BIG_ENDIAN__`
Little endian|`__LITTLE_ENDIAN__`<br/>`__ARMEL__`<br/>`__THUMBEL__`<br/>`__AARCH64EL__`<br/>`_MIPSEL`<br/>`__MIPSEL`<br/>`__MIPSEL__`|
Little endian|`__BYTE_ORDER__`|`__ORDER_LITTLE_ENDIAN__`
Little endian|`__FLOAT_WORD_ORDER__`|`__ORDER_LITTLE_ENDIAN__` 
