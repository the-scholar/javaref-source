@location: /literals/int/
# Integer Literals
*A direct (literal) expression of an integral, (`int` or `long`), value in source code.*

## Syntax
(1) decimal-literal [integer-type-suffix]
(2) hexadecimal-literal [integer-type-suffix]
(3) octal-literal [integer-type-suffix]
(4) binary-literal [integer-type-suffix]

where:
* A {decimal-literal} is either:
	1. the digit `0`, or
	2. a non-zero decimal digit (`1`, `2`, `3`, `4`, `5`, `6`, `7`, `8`, `9`),
followed by any number of decimal digits (`0`, `1`, `2`, `3`, `4`, `5`, `6`, `7`, `8`, `9`),
* A {hexadecimal-literal} is the string prefix^[1] `0x` or `0X`, followed by at least one hexadecimal digit (`0`, `1`, `2`, `3`, `4`, `5`, `6`, `7`, `8`, `9`, `a`, `b`, `c`, `d`, `e`, `f`, `A`, `B`, `C`, `D`, `E`, `F`),
^[1](The prefix itself is not composed of digits and therefore cannot have interleaved underscores; `0_x123` and `0x_123` are both invalid, for example),
* An {octal-literal} is the digit `0` followed by at least one octal digit (`0`, `1`, `2`, `3`, `4`, `5`, `6`, `7`),
* A {binary-literal} is the string prefix^[2] `0b` or `0B`, followed by at least one binary digit (`0`, `1`),
* An {integer-type-suffix} is the letter `L` or `l`,

such that:
Each pair of consecutive digits (including the `0` prefix digit for (1.3)s) can be separated by any number of underscores, (e.g., `0x47ab == 0x47_a__b`).

### Elements
(1) A decimal integer literal (base 10), using digits `0` through `10`.
(2) A hexadecimal integer literal (base 16), using the same digits as base 10 as well as digits `A` through `F` with values `10` through `15`. Capitalization is ignored, so `A` is equivalent to `a`, `B` to `b`, etc.
(3) An octal integer literal (base 8), using digits `0` through `7`. The `0` prefix is only used to signify that the literal is in octal notation and does not otherwise affect the literal's value.
(4) A binary integer literal (base 2), using digits `0` and `1`.

## Value


## Notes
1. `0` is the only integer literal whose leftmost digit is `0` that is not an octal literal.