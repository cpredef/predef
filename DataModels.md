## [Data Models](https://www.unix.org/whitepapers/64bit.html) ##

Data type | LP32 | ILP32 | LP64 | LLP64 | ILP64 | SILP64
---|---|---|---|---|---|---
char | 8 | 8 | 8 | 8 | 8 | 8
short | 16 | 16 | 16 | 16 | 16 | 64
int | 16 | 32 | 32 | 32 | 64 | 64
long | 32 | 32 | 64 | 32 | 64 | 64
long long | | | 64 | 64 | 64 | 64
pointer | 32 | 32 | 64 | 64 | 64 | 64

## LP32 ##

Macro | Description
---|---
`__fourbyteints__` = 0| Defined by MPW and Metrowerks on Motorola 68k targets when configured to use 16-bit int

## ILP32 ##

Macro | Description
---|---
`_ILP32` | Defined by HP aCC and Sun Studio
`__ILP32__` | Defined by GNU C
`__fourbyteints__` = 1| Defined by MPW and Metrowerks on Motorola 68k targets when configured to use 32-bit int

## LP64 ##

Macro | Description
---|---
`_LP64` | Defined by HP aCC and Sun Studio
`__LP64__` | Defined by GNU C
