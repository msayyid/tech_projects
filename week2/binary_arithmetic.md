# 1. Binary, Decimal, Octal, Hexadecimal

Computers store information using **bits**.

A **bit** is one digit that can only be:

```text
0 or 1
```

Different number systems use different numbers of allowed digits.

| System      | Base | Allowed digits | Example |
| ----------- | ---: | -------------- | ------- |
| Decimal     |   10 | 0-9            | 156     |
| Binary      |    2 | 0-1            | 101101  |
| Octal       |    8 | 0-7            | 745     |
| Hexadecimal |   16 | 0-9, A-F       | 3F9     |

---

## Decimal - base 10

This is the normal number system we use every day.

Example:

```text
156
```

This means:

```text
1 × 100
5 × 10
6 × 1
```

So:

```text
156 = 100 + 50 + 6
```

Decimal uses powers of 10:

```text
1000  100  10  1
10^3  10^2 10^1 10^0
```

---

## Binary - base 2

Binary only uses:

```text
0 and 1
```

Binary uses powers of 2:

```text
128 64 32 16 8 4 2 1
```

Example:

```text
101101
```

Write the place values:

```text
32 16 8 4 2 1
 1  0 1 1 0 1
```

Now add the places where there is a `1`:

```text
32 + 8 + 4 + 1 = 45
```

So:

```text
101101 binary = 45 decimal
```

Simple idea:

```text
In binary, each position is worth double the position to its right.
```

---

## Octal - base 8

Octal uses digits:

```text
0, 1, 2, 3, 4, 5, 6, 7
```

It does **not** use 8 or 9.

Octal uses powers of 8:

```text
64 8 1
8^2 8^1 8^0
```

Example:

```text
745 octal
```

This means:

```text
7 × 64 = 448
4 × 8  = 32
5 × 1  = 5
```

So:

```text
448 + 32 + 5 = 485
```

Therefore:

```text
745 octal = 485 decimal
```

---

## Hexadecimal - base 16

Hexadecimal uses 16 possible digits:

```text
0 1 2 3 4 5 6 7 8 9 A B C D E F
```

Letters represent numbers above 9:

```text
A = 10
B = 11
C = 12
D = 13
E = 14
F = 15
```

Hex uses powers of 16:

```text
256 16 1
16^2 16^1 16^0
```

Example:

```text
3F9 hex
```

This means:

```text
3 × 256 = 768
F × 16  = 15 × 16 = 240
9 × 1   = 9
```

So:

```text
768 + 240 + 9 = 1017
```

Therefore:

```text
3F9 hex = 1017 decimal
```

---

# 2. Convert Between Bases

There are a few common conversion methods you need.

---

# A. Binary to Decimal

Example:

```text
101101
```

Write place values:

```text
32 16 8 4 2 1
 1  0 1 1 0 1
```

Add only the places with `1`:

```text
32 + 8 + 4 + 1 = 45
```

Answer:

```text
101101 binary = 45 decimal
```

---

# B. Decimal to Binary

Example:

```text
156 decimal to binary
```

Use powers of 2:

```text
128 64 32 16 8 4 2 1
```

Ask: can 128 fit into 156?

Yes.

```text
156 - 128 = 28
```

So put `1` under 128.

Can 64 fit into 28?

No. Put `0`.

Can 32 fit into 28?

No. Put `0`.

Can 16 fit into 28?

Yes.

```text
28 - 16 = 12
```

Can 8 fit into 12?

Yes.

```text
12 - 8 = 4
```

Can 4 fit into 4?

Yes.

```text
4 - 4 = 0
```

Then 2 and 1 are not needed.

```text
128 64 32 16 8 4 2 1
  1  0  0  1 1 1 0 0
```

Answer:

```text
156 decimal = 10011100 binary
```

---

# C. Binary to Octal

This is easier than going through decimal.

Rule:

```text
Group binary digits in groups of 3 from the right.
```

Example:

```text
101101
```

Group into threes:

```text
101 101
```

Convert each group:

```text
101 = 5
101 = 5
```

Answer:

```text
101101 binary = 55 octal
```

Why groups of 3?

Because:

```text
3 binary bits can represent 0 to 7
```

And octal digits are also:

```text
0 to 7
```

---

# D. Binary to Hexadecimal

Rule:

```text
Group binary digits in groups of 4 from the right.
```

Example:

```text
101101
```

Group into fours from the right:

```text
10 1101
```

The first group needs 4 bits, so add leading zeros:

```text
0010 1101
```

Convert each group:

```text
0010 = 2
1101 = 13 = D
```

Answer:

```text
101101 binary = 2D hex
```

Why groups of 4?

Because:

```text
4 binary bits can represent 0 to 15
```

And hex has 16 digits:

```text
0 to F
```

---

# E. Octal to Binary

Each octal digit becomes 3 binary bits.

Example:

```text
745 octal
```

Convert each digit:

```text
7 = 111
4 = 100
5 = 101
```

Put them together:

```text
745 octal = 111100101 binary
```

---

# F. Hex to Binary

Each hex digit becomes 4 binary bits.

Example:

```text
3F9 hex
```

Convert each digit:

```text
3 = 0011
F = 1111
9 = 1001
```

Put them together:

```text
3F9 hex = 0011 1111 1001
```

Remove leading zeros if you want:

```text
1111111001
```

So:

```text
3F9 hex = 1111111001 binary
```

---

# 3. Binary Addition Carry

Binary addition is like decimal addition, but binary only has two digits:

```text
0 and 1
```

So when the result reaches `2`, we carry.

## Basic rules

```text
0 + 0 = 0
0 + 1 = 1
1 + 0 = 1
1 + 1 = 10
```

Important:

```text
1 + 1 = 10 in binary
```

That means:

```text
write 0, carry 1
```

If there is already a carry:

```text
1 + 1 + 1 = 11
```

That means:

```text
write 1, carry 1
```

---

## Example: 1011 + 1101

```text
  1011
+ 1101
------
```

Work from right to left.

### Rightmost column

```text
1 + 1 = 10
```

Write `0`, carry `1`.

```text
carry: 1
  1011
+ 1101
------
     0
```

### Next column

```text
1 + 0 + carry 1 = 10
```

Write `0`, carry `1`.

```text
carry: 1
  1011
+ 1101
------
    00
```

### Next column

```text
0 + 1 + carry 1 = 10
```

Write `0`, carry `1`.

```text
carry: 1
  1011
+ 1101
------
   000
```

### Leftmost column

```text
1 + 1 + carry 1 = 11
```

Write `1`, carry `1`.

Then put final carry at the front.

```text
  1011
+ 1101
------
 11000
```

Answer:

```text
1011 + 1101 = 11000
```

Check in decimal:

```text
1011 binary = 11 decimal
1101 binary = 13 decimal
11 + 13 = 24
11000 binary = 24 decimal
```

---

# 4. Binary Subtraction Borrow

Binary subtraction is like decimal subtraction.

But instead of borrowing `10`, you borrow `2`, because binary is base 2.

## Basic rules

```text
0 - 0 = 0
1 - 0 = 1
1 - 1 = 0
0 - 1 = need to borrow
```

When you borrow in binary:

```text
10 binary = 2 decimal
```

So:

```text
10 - 1 = 1
```

---

## Example: 1101 - 1010

```text
  1101
- 1010
------
```

From right to left:

### Rightmost column

```text
1 - 0 = 1
```

### Next column

```text
0 - 1
```

Cannot do this directly, so borrow from the next column.

The next column has `1`, so borrow from it.

Now the current column becomes:

```text
10 binary
```

So:

```text
10 - 1 = 1
```

The borrowed-from column becomes `0`.

### Next column

Originally it was `1`, but we borrowed from it, so now it is `0`.

```text
0 - 0 = 0
```

### Leftmost column

```text
1 - 1 = 0
```

Answer:

```text
  1101
- 1010
------
  0011
```

So:

```text
1101 - 1010 = 0011
```

or simply:

```text
11
```

Both mean 3 decimal.

---

## Simple way to explain borrow

Say this:

```text
If the top bit is smaller than the bottom bit, borrow from the next column on the left.
In binary, borrowing gives you 2, written as 10.
```

---

# 5. Two’s Complement

Two’s complement is a way computers represent negative numbers.

In normal decimal, we write:

```text
-5
```

But computers store bits, so they need a binary pattern to represent negative numbers.

Two’s complement is the most common method.

---

## How to find two’s complement

Method:

```text
Step 1: Flip every bit
Step 2: Add 1
```

Flipping means:

```text
0 becomes 1
1 becomes 0
```

---

## Example: Find two’s complement of 101010

Original:

```text
101010
```

Step 1: Flip bits:

```text
010101
```

Step 2: Add 1:

```text
010101
+     1
------
010110
```

Answer:

```text
101010 -> 010110
```

---

## Another example: 1001

Original:

```text
1001
```

Flip bits:

```text
0110
```

Add 1:

```text
0110
+  1
----
0111
```

Answer:

```text
1001 -> 0111
```

---

## Why do we use two’s complement?

Because it allows computers to use the same binary addition hardware for both addition and subtraction.

Example idea:

```text
5 - 3
```

can be treated as:

```text
5 + (-3)
```

So the computer only needs addition logic.

---

## Important signed-number idea

In signed two’s complement, the leftmost bit is important.

For an 8-bit number:

```text
00000101 = positive 5
11111011 = negative 5
```

Simple rule:

```text
If the leftmost bit is 0, the number is non-negative.
If the leftmost bit is 1, the number is negative.
```

But be careful: this depends on whether we are treating the number as **signed**.

The same bit pattern can mean different things depending on interpretation.

Example:

```text
11111111
```

As unsigned:

```text
255
```

As signed two’s complement:

```text
-1
```

---

# 6. Fixed-Point Binary

Fixed-point binary is used to represent numbers with fractions.

Example decimal fractions:

```text
12.75
5.125
7.5
```

In normal decimal:

```text
12.75
```

The decimal point separates:

```text
whole number . fraction
```

In binary fixed-point, we do the same:

```text
binary whole number . binary fraction
```

---

## Binary fractional place values

To the left of the point:

```text
8 4 2 1
```

To the right of the point:

```text
1/2   1/4   1/8   1/16   1/32
0.5   0.25  0.125 0.0625 0.03125
```

So:

```text
0.1 binary = 0.5 decimal
0.01 binary = 0.25 decimal
0.001 binary = 0.125 decimal
```

---

## Example: 12.75 with 4 integer bits and 4 fractional bits

Separate it:

```text
12 + 0.75
```

Convert 12 to binary:

```text
12 = 8 + 4
```

Using 4 integer bits:

```text
8 4 2 1
1 1 0 0
```

So:

```text
12 = 1100
```

Now convert 0.75:

```text
0.75 = 0.5 + 0.25
```

Fraction places:

```text
0.5 0.25 0.125 0.0625
 1    1    0      0
```

So:

```text
0.75 = .1100
```

Final answer:

```text
12.75 = 1100.1100
```

---

## Example: 5.125 with 3 integer bits and 5 fractional bits

Separate it:

```text
5 + 0.125
```

Convert 5 to binary with 3 integer bits:

```text
4 2 1
1 0 1
```

So:

```text
5 = 101
```

Convert 0.125:

```text
0.125 = 1/8
```

Fraction places with 5 bits:

```text
0.5 0.25 0.125 0.0625 0.03125
 0    0     1      0       0
```

So:

```text
0.125 = .00100
```

Final answer:

```text
5.125 = 101.00100
```

---

## Example: 7.5 with 4 integer bits and 4 fractional bits

Separate it:

```text
7 + 0.5
```

Convert 7 to binary with 4 integer bits:

```text
8 4 2 1
0 1 1 1
```

So:

```text
7 = 0111
```

Convert 0.5:

```text
0.5 = .1000
```

Final answer:

```text
7.5 = 0111.1000
```

---

## Common mistake with fixed-point

Students often write:

```text
7.5 = 111.1
```

This is mathematically true, but it does not follow the required bit format.

If the question says:

```text
4 integer bits and 4 fractional bits
```

then the answer must have:

```text
4 bits before the point
4 bits after the point
```

So:

```text
111.1
```

must become:

```text
0111.1000
```

---

# 7. 8-bit Unsigned and Signed Ranges

An 8-bit number has 8 binary digits.

Example:

```text
00000000
11111111
```

With 8 bits, there are:

```text
2^8 = 256 possible patterns
```

But those 256 patterns can be interpreted in different ways.

---

# A. 8-bit Unsigned Range

Unsigned means:

```text
No negative numbers
```

All 256 patterns represent zero or positive numbers.

Smallest:

```text
00000000 = 0
```

Largest:

```text
11111111 = 255
```

Why 255?

Place values:

```text
128 64 32 16 8 4 2 1
  1  1  1  1 1 1 1 1
```

Add them:

```text
128 + 64 + 32 + 16 + 8 + 4 + 2 + 1 = 255
```

So:

```text
8-bit unsigned range = 0 to 255
```

Formula:

```text
0 to 2^n - 1
```

For 8 bits:

```text
0 to 2^8 - 1
0 to 256 - 1
0 to 255
```

---

# B. 8-bit Signed Two’s Complement Range

Signed means:

```text
Can represent negative and positive numbers
```

With 8-bit two’s complement:

```text
Range = -128 to +127
```

Why?

There are still 256 patterns total.

They are split like this:

```text
128 negative values
128 non-negative values
```

The non-negative side includes zero:

```text
0 to 127
```

That is 128 values:

```text
0, 1, 2, ..., 127
```

The negative side is:

```text
-128 to -1
```

That is also 128 values.

So the full range is:

```text
-128 to 127
```

Formula:

```text
-2^(n-1) to 2^(n-1) - 1
```

For 8 bits:

```text
-2^7 to 2^7 - 1
-128 to 127
```

---

## Why is the positive maximum 127, not 128?

Because zero takes one of the positive/non-negative patterns.

The non-negative values are:

```text
0 to 127
```

That is already 128 values.

So there is no extra pattern left for +128.

---

## Examples

```text
01111111 = 127
10000000 = -128
11111111 = -1
00000000 = 0
```

Important:

```text
In signed two’s complement, if the leftmost bit is 1, the number is negative.
```

---

# Final Cheat Sheet

## Number systems

```text
Decimal = base 10 = 0-9
Binary = base 2 = 0-1
Octal = base 8 = 0-7
Hex = base 16 = 0-9, A-F
```

## Binary place values

```text
128 64 32 16 8 4 2 1
```

## Binary addition

```text
1 + 1 = 10
Write 0, carry 1
```

## Binary subtraction

```text
0 - 1 means borrow
Borrowing in binary gives 10, which equals 2 decimal
```

## Two’s complement

```text
Flip bits + add 1
```

## Fixed-point

```text
Bits before point = whole-number part
Bits after point = fractional part
```

Fraction values:

```text
0.5, 0.25, 0.125, 0.0625, 0.03125
```

## 8-bit ranges

```text
Unsigned: 0 to 255
Signed two’s complement: -128 to 127
```

# What you should be able to say in class

```text
Binary is base 2, so each place value is a power of 2.
When converting binary to decimal, add the place values where the bit is 1.
Binary addition uses carry because 1 + 1 becomes 10.
Binary subtraction uses borrow, but you borrow 2 instead of 10.
Two’s complement represents negative numbers by flipping bits and adding 1.
Fixed-point binary represents fractions using places like 1/2, 1/4, and 1/8.
With 8 bits unsigned we get 0 to 255, but with signed two’s complement we get -128 to 127.
```
