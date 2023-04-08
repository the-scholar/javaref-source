@location: /literals/int/
# Integer Literals
*A direct (literal) expression of an integral, (`int` or `long`), value in source code.*

## Syntax
decimal-literal [integer-type-suffix]
hexadecimal-literal [integer-type-suffix]
octal-literal [integer-type-suffix]
binary-literal [integer-type-suffix]

where:
* A {decimal-literal} is either:
	1. the digit `0`
	2. a non-zero decimal digit (`1`, `2`, `3`, `4`, `5`, `6`, `7`, `8`, `9`)
followed by any number of decimal digits (`0`, `1`, `2`, `3`, `4`, `5`, `6`, `7`, `8`, `9`)
* A {hexadecimal-literal} is the string prefix^[1] `0x` or `0X`, followed by at least one hexadecimal digit (`0`, `1`, `2`, `3`, `4`, `5`, `6`, `7`, `8`, `9`, `a`, `b`, `c`, `d`, `e`, `f`, `A`, `B`, `C`, `D`, `E`, `F`).
* An {octal-literal} is the digit `0` followed by at least one octal digit (`0`, `1`, `2`, `3`, `4`, `5`, `6`, `7`)
* A {binary-literal} is the string prefix^[1] `0b` or `0B`, followed by at least one binary digit (`0`, `1`)
* An {integer-type-suffix} is the letter `L` or `l`

^[1](The prefix itself is not composed of digits and therefore cannot have interleaved underscores; `0_x123` and `0x_123` are both invalid, for example.)

such that:
Each pair of consecutive digits (including the `0` prefix digit for {octal-literal}) can be separated by any number of underscores, (e.g., `0x47ab == 0x47_a__b`).

### Syntax Elements
A decimal integer literal (base 10), using digits `0` through `10`.
A hexadecimal integer literal (base 16), using the same digits as base 10 as well as digits `A` through `F` with values `10` through `15`. Capitalization is ignored, so `A` is equivalent to `a`, `B` to `b`, etc.
An octal integer literal (base 8), using digits `0` through `7`. The `0` prefix is only used to signify that the literal is in octal notation and does not otherwise affect the literal's value.
A binary integer literal (base 2), using digits `0` and `1`.

## Value

## Examples
[[1]] Simple Examples:
```
int x = 0b00101001; // 41
int y = 41;
System.out.println(x == y); // Prints true
```
Output:
```output
true
```

```
for (int i = 0xF; i >= 0x0; i--)
	System.out.println(i);	// println(...) prints integers in decimal (base 10)
```
Output:
```output
15
14
13
12
11
10
9
8
7
6
5
4
3
2
1
0
```

[[2]] Bitflags &amp; Bitmasks:
```
int x = 0b0110; // equal to 6
final int FLAG = 0b0001;

// Enable flag:
x |= FLAG;// x is now 0b0111 which is equal to 7

// Disable flag:
x ^= FLAG;// x is now 0b0110 which is 6

// Check for flag:
boolean flagOn = (x & FLAG) != 0;
if (flagOn)
   doSomething();
```

[[3]] Octal Numbers
```
// Each octal digit is 3 bits
System.out.println(0b111 == 07); // true
System.out.println(0b111000 == 070); // true

// Octal 7 is binary 111
// Octal 0 is binary 000
System.out.pintln(0b111_000_111_000 == 07070); // true
```
Output:
```output
true
true
true
```

## Notes
1. `0` is the only integer literal whose leftmost digit is `0` that is not an octal literal.