# Question 1: Binary Concatenation

## Explanation

For every positive integer `x`, its binary representation is the sequence of `0`s and `1`s used to represent that number in binary.

For a given `n`, you create one long string by writing the binary representations of all numbers from `1` to `n` one after another.

For example, when `n = 3`:

`1 → "1"`

`2 → "10"`

`3 → "11"`

Joining them gives `"11011"`.

The resulting string is then interpreted as a decimal integer. Since the resulting number can become extremely large, you only need to output its value modulo `998244353`.

## Problem Statement

For a positive integer `x`, let `binary(x)` denote its binary representation without leading zeros.

For example:
- `binary(1) = "1"`
- `binary(2) = "10"`
- `binary(5) = "101"`

For a given integer `n`, construct the string:

`S = binary(1) + binary(2) + ... + binary(n)`

Now interpret `S` as a DECIMAL integer.

Compute this decimal integer modulo: `998244353`

## Input Format

The first line contains an integer `t`.

The second line contains `t` space-separated integers `n`.

## Output Format

For every test case, print the required value modulo `998244353`.

## Constraints

- `1 <= t <= 1000`
- `1 <= n <= 10^15`

## Examples

### Example 1
**Input:**
```text
2
3 7
```
**Output:**
```text
11011
703895966
```
**Explanation:** 
For `n = 3`, the binary representations without leading zeros are 1 (for 1), 10 (for 2), and 11 (for 3). Concatenating them gives `11011`. Interpreted as a decimal integer, 11011 modulo 998244353 is 11011.
For `n = 7`, the concatenated binary representations form the string `11011100101110111`. Interpreted as a decimal integer, its value modulo 998244353 is 703895966.

## Topics

- [Bit Manipulation](https://youtu.be/H_NCHm3wAMI?si=Y1aY-3B4LooSuVLv)
- [Modular Arithmetic & Fast Exponentiation](https://youtu.be/KdePjukNs98?si=UM5-mjw0zoQLW0dK)
