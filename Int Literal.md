@location: /literals/int/
# Integer Literals
*Direct (literal) expression of an integral, (`int` or `long`), value in source code.*

## Syntax
(1) decimal-literal --> (1)
(2) hexadecimal-literal --> (1)
(3) octal-literal --> (1)
(4) binary-literal --> (1)
---
(1) [int-literal-suffix]

### where...
* decimal-literal: Either,
	1. the digit `0`, or
	2. a non-zero decimal digit (`1`, `2`, `3`, `4`, `5`, `6`, `7`, `8`, `9`),
followed by any number of decimal digits (`0`, `1`, `2`, `3`, `4`, `5`, `6`, `7`, `8`, `9`).
* hexadecimal-literal: The string prefix^[1] `0x` or `0X`, followed by at least one hexadecimal digit (`0`, `1`, `2`, `3`, `4`, `5`, `6`, `7`, `8`, `9`, `a`, `b`, `c`, `d`, `e`, `f`, `A`, `B`, `C`, `D`, `E`, `F`). ^[1](The prefix is not composed of digits and therefore cannot have interleaved underscores; `0_x123` and `0x_123` are both invalid, for example.)
* octal-literal: The digit `0` followed by at least one octal digit (`0`, `1`, `2`, `3`, `4`, `5`, `6`, `7`).
* binary-literal: The string prefix^[2] `0b` or `0B`, followed by at least one binary digit (`0`, `1`).
* int-literal-suffix: 

### and...
* Each pair of consecutive digits (including the `0` prefix digit for (1.3)s) can be separated by any number of underscores, (e.g., `0x47ab == 0x47_a__b`).