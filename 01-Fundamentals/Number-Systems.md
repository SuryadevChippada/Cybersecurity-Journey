# Number Systems

## Overview

Number systems are different ways of representing numerical values. Each number system has a base (radix), which determines the number of unique digits available.

Computers primarily use binary because digital circuits operate using two states, represented by 0 and 1. Hexadecimal and octal provide shorter and more readable representations of binary values.

## Types of Number Systems

| Number System | Base | Digits |
|---|---:|---|
| Decimal | 10 | 0–9 |
| Binary | 2 | 0–1 |
| Octal | 8 | 0–7 |
| Hexadecimal | 16 | 0–9, A–F |

## Decimal (Base 10)

Decimal is the number system used in everyday life. Each digit represents a power of 10 depending on its position.

Example:

```text
345 = (3 × 10²) + (4 × 10¹) + (5 × 10⁰)
    = 300 + 40 + 5
    = 345
```

## Binary (Base 2)

Binary uses only two digits: 0 and 1.

Each binary digit is called a bit. Computers use binary to represent instructions, numbers, characters, images and other types of data.

Example:

```text
Binary: 1011

= (1 × 2³) + (0 × 2²) + (1 × 2¹) + (1 × 2⁰)
= 8 + 0 + 2 + 1
= 11
```

### Binary Place Values

| Position | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|
| Value | 128 | 64 | 32 | 16 | 8 | 4 | 2 | 1 |

An unsigned 8-bit binary number can represent values from 0 to 255.

## Octal (Base 8)

Octal uses digits from 0 to 7. Each digit represents a power of 8.

Example:

```text
Octal: 157

= (1 × 8²) + (5 × 8¹) + (7 × 8⁰)
= 64 + 40 + 7
= 111
```

Octal is commonly encountered in Unix and Linux file permissions.

For example:

```bash
chmod 755 script.sh
```

The permission values represent:

- 4 = Read
- 2 = Write
- 1 = Execute

Therefore:

| Value | Binary | Permission |
|---|---|---|
| 7 | 111 | rwx |
| 5 | 101 | r-x |
| 5 | 101 | r-x |

The owner has read, write and execute permissions, while the group and others have read and execute permissions.

## Hexadecimal (Base 16)

Hexadecimal uses 16 symbols, consisting of digits 0–9 and letters A–F.

| Decimal | Binary | Hexadecimal |
|---:|---|---|
| 0 | 0000 | 0 |
| 1 | 0001 | 1 |
| 2 | 0010 | 2 |
| 3 | 0011 | 3 |
| 4 | 0100 | 4 |
| 5 | 0101 | 5 |
| 6 | 0110 | 6 |
| 7 | 0111 | 7 |
| 8 | 1000 | 8 |
| 9 | 1001 | 9 |
| 10 | 1010 | A |
| 11 | 1011 | B |
| 12 | 1100 | C |
| 13 | 1101 | D |
| 14 | 1110 | E |
| 15 | 1111 | F |

One hexadecimal digit represents four binary bits. Two hexadecimal digits represent one byte.

Example:

```text
Hexadecimal: 2F

= (2 × 16¹) + (15 × 16⁰)
= 32 + 15
= 47
```

Hexadecimal values are commonly written with the prefix `0x`.

```text
0xFF = 255
0x10 = 16
0xA0 = 160
```

Hexadecimal is useful when working with memory addresses, machine instructions, MAC addresses, hashes and raw file contents.

## Number System Conversions

### Decimal to Binary

To convert a decimal number to binary, repeatedly divide the number by 2 and record the remainders.

Example: Convert 25 to binary.

```text
25 ÷ 2 = 12 remainder 1
12 ÷ 2 =  6 remainder 0
 6 ÷ 2 =  3 remainder 0
 3 ÷ 2 =  1 remainder 1
 1 ÷ 2 =  0 remainder 1
```

Reading the remainders from bottom to top:

```text
25₁₀ = 11001₂
```

### Binary to Decimal

Multiply each digit by its corresponding power of 2 and add the results.

```text
11001₂

= (1 × 16) + (1 × 8) + (0 × 4) + (0 × 2) + (1 × 1)
= 25₁₀
```

### Decimal to Octal

Repeatedly divide the decimal number by 8.

```text
83 ÷ 8 = 10 remainder 3
10 ÷ 8 =  1 remainder 2
 1 ÷ 8 =  0 remainder 1

83₁₀ = 123₈
```

### Octal to Decimal

```text
123₈

= (1 × 8²) + (2 × 8¹) + (3 × 8⁰)
= 64 + 16 + 3
= 83₁₀
```

### Decimal to Hexadecimal

Repeatedly divide the decimal number by 16.

```text
254 ÷ 16 = 15 remainder 14 (E)
 15 ÷ 16 =  0 remainder 15 (F)

254₁₀ = FE₁₆
```

### Hexadecimal to Decimal

```text
FE₁₆

= (15 × 16¹) + (14 × 16⁰)
= 240 + 14
= 254₁₀
```

### Binary to Hexadecimal

Divide the binary number into groups of four bits, starting from the right. Add leading zeros if necessary.

```text
Binary: 11010110

1101 | 0110
  D  |   6

11010110₂ = D6₁₆
```

### Hexadecimal to Binary

Replace each hexadecimal digit with its four-bit binary equivalent.

```text
Hexadecimal: A7

A = 1010
7 = 0111

A7₁₆ = 10100111₂
```

### Binary to Octal

Divide the binary number into groups of three bits, starting from the right.

```text
Binary: 110101

110 | 101
 6  |  5

110101₂ = 65₈
```

### Octal to Binary

Replace each octal digit with its three-bit binary equivalent.

```text
Octal: 65

6 = 110
5 = 101

65₈ = 110101₂
```

## Binary Arithmetic

### Addition

The basic rules of binary addition are:

```text
0 + 0 = 0
0 + 1 = 1
1 + 0 = 1
1 + 1 = 10
```

Example:

```text
   1011   (11)
 + 0110   (6)
 -------
  10001   (17)
```

### Subtraction

Binary subtraction follows a similar borrowing mechanism to decimal subtraction.

```text
   1101   (13)
 - 0101   (5)
 -------
   1000   (8)
```

### Multiplication

```text
0 × 0 = 0
0 × 1 = 0
1 × 0 = 0
1 × 1 = 1
```

Example:

```text
    101   (5)
  ×  11   (3)
  -----
    101
+  1010
  -----
   1111   (15)
```

### Division

Binary division follows the same general principle as decimal long division.

```text
1100 ÷ 10 = 110

12 ÷ 2 = 6
```

## Signed and Unsigned Numbers

Unsigned numbers represent zero and positive values.

Signed numbers can represent both positive and negative values.

For an n-bit unsigned integer:

```text
Minimum = 0
Maximum = 2ⁿ − 1
```

For an n-bit signed integer using two's complement:

```text
Minimum = −2ⁿ⁻¹
Maximum = 2ⁿ⁻¹ − 1
```

| Bits | Unsigned Range | Signed Range |
|---:|---|---|
| 8 | 0 to 255 | −128 to 127 |
| 16 | 0 to 65,535 | −32,768 to 32,767 |
| 32 | 0 to 4,294,967,295 | −2,147,483,648 to 2,147,483,647 |
| 64 | 0 to 2⁶⁴ − 1 | −2⁶³ to 2⁶³ − 1 |

The interpretation of a binary value depends on whether it is treated as signed or unsigned.

For example:

```text
11111111

Unsigned 8-bit: 255
Signed 8-bit:   -1
```

## One's Complement

One's complement is obtained by reversing every bit of a binary number.

```text
Original:         00000101
One's complement: 11111010
```

Every 0 becomes 1, and every 1 becomes 0.

When used as a signed-number representation, one's complement has two representations of zero, which is one reason two's complement is generally preferred.

## Two's Complement

Two's complement is the standard method used to represent signed integers in modern computers.

To represent a negative number:

1. Convert the positive number to binary using the required bit width.
2. Invert all bits.
3. Add 1.

Example: Represent −5 using 8 bits.

```text
Positive 5:       00000101
Invert bits:      11111010
Add 1:          + 00000001
                  --------
Negative 5:       11111011
```

Another example:

```text
 5 = 00000101
-5 = 11111011
```

Adding both values:

```text
   00000101
 + 11111011
 ----------
  100000000
```

Keeping only the lowest eight bits gives `00000000`, which represents zero.

Two's complement allows the same binary addition circuitry to handle signed addition and subtraction.

## Integer Overflow and Underflow

Integer overflow occurs when a calculation produces a value greater than the maximum representable value of its data type.

Integer underflow, in this context, occurs when a calculation produces a value below the minimum representable value.

Example using an unsigned 8-bit integer:

```text
Maximum value: 255

  11111111
+ 00000001
----------
 100000000
```

When stored using only eight bits with wrapping arithmetic:

```text
00000000 = 0
```

Similarly:

```text
0 − 1 = 255
```

The exact behaviour depends on the programming language and data type.

In C and C++, unsigned integer arithmetic wraps modulo 2ⁿ, while signed integer overflow generally results in undefined behaviour.

Integer overflow can cause security vulnerabilities when values are used for memory allocation, array indexing, buffer sizes or input validation.

## Bits and Bytes

A bit is the smallest unit of digital information and can contain either 0 or 1.

A byte consists of eight bits.

| Unit | Size |
|---|---|
| Bit | 1 binary digit |
| Nibble | 4 bits |
| Byte | 8 bits |
| Kilobyte (KB) | 1,000 bytes |
| Kibibyte (KiB) | 1,024 bytes |
| Megabyte (MB) | 1,000,000 bytes |
| Mebibyte (MiB) | 1,048,576 bytes |
| Gigabyte (GB) | 1,000,000,000 bytes |
| Gibibyte (GiB) | 1,073,741,824 bytes |

The number of possible combinations that can be represented using n bits is:

```text
2ⁿ
```

For example:

```text
4 bits  = 16 combinations
8 bits  = 256 combinations
16 bits = 65,536 combinations
32 bits = 4,294,967,296 combinations
```

## Bitwise Operations

Bitwise operations manipulate individual bits of a binary value.

They are commonly used in low-level programming, networking, cryptography and operating systems.

### AND

Returns 1 only when both bits are 1.

```text
  1100
& 1010
------
  1000
```

Commonly used for bit masking and network subnet calculations.

### OR

Returns 1 when at least one of the bits is 1.

```text
  1100
| 1010
------
  1110
```

Commonly used to enable individual flags.

### XOR

Returns 1 when the two bits are different.

```text
  1100
^ 1010
------
  0110
```

XOR has the following useful properties:

```text
A XOR A = 0
A XOR 0 = A
(A XOR B) XOR B = A
```

XOR is used as a component in cryptographic algorithms, checksums and other low-level operations. XOR alone does not provide secure encryption.

### NOT

Inverts every bit.

```text
Original: 1100
NOT:      0011
```

The example assumes a fixed width of four bits.

### Left Shift

Moves bits to the left.

```text
00000101 << 1 = 00001010

5 << 1 = 10
```

For unsigned integers, shifting left by one position is equivalent to multiplying by 2 modulo the representable range, assuming a valid shift count.

### Right Shift

Moves bits to the right.

```text
00001010 >> 1 = 00000101

10 >> 1 = 5
```

For unsigned integers, shifting right by one position is equivalent to integer division by 2.

Right-shift behaviour for negative signed values depends on the language and its version.

### Bitwise Truth Table

| A | B | AND | OR | XOR |
|---|---|---|---|---|
| 0 | 0 | 0 | 0 | 0 |
| 0 | 1 | 0 | 1 | 1 |
| 1 | 0 | 0 | 1 | 1 |
| 1 | 1 | 1 | 1 | 0 |

## Practical Examples

### Number Conversion in Python

```python
number = 42

print("Decimal:", number)
print("Binary:", bin(number))
print("Octal:", oct(number))
print("Hexadecimal:", hex(number))
```

Expected output:

```text
Decimal: 42
Binary: 0b101010
Octal: 0o52
Hexadecimal: 0x2a
```

Converting values back to decimal:

```python
print(int("101010", 2))
print(int("52", 8))
print(int("2A", 16))
```

Expected output:

```text
42
42
42
```

### Bitwise Operations in Python

```python
a = 12
b = 10

print("AND:", a & b)
print("OR:", a | b)
print("XOR:", a ^ b)
print("NOT (8-bit):", (~a) & 0xFF)
print("Left shift:", a << 1)
print("Right shift:", a >> 1)
```

Expected output:

```text
AND: 8
OR: 14
XOR: 6
NOT (8-bit): 243
Left shift: 24
Right shift: 6
```

### Examining File Contents

The `xxd` command can be used to view the hexadecimal representation of a file.

```bash
printf 'Hello' > example.txt
xxd example.txt
```

Expected output:

```text
00000000: 4865 6c6c 6f    Hello
```

The hexadecimal values represent the ASCII characters:

| Character | Decimal | Hexadecimal |
|---|---:|---|
| H | 72 | 48 |
| e | 101 | 65 |
| l | 108 | 6C |
| l | 108 | 6C |
| o | 111 | 6F |

## Applications in Cybersecurity

### Networking

IPv4 addresses consist of 32 bits and are normally displayed as four decimal octets.

```text
192.168.1.1

11000000.10101000.00000001.00000001
```

Understanding binary is important for subnetting, network masks and packet analysis.

### Linux File Permissions

Linux file permissions can be represented using octal numbers.

```text
755 = rwxr-xr-x
644 = rw-r--r--
700 = rwx------
600 = rw-------
```

Incorrect file permissions can expose sensitive information or provide unnecessary access.

### Memory Analysis

Memory addresses are commonly displayed in hexadecimal.

```text
0x7FFE1234
0x00401000
```

Hexadecimal representation makes large binary values easier to read when debugging programs or examining memory.

### Digital Forensics

File signatures are often represented in hexadecimal.

| File Type | Hexadecimal Signature |
|---|---|
| PNG | 89 50 4E 47 0D 0A 1A 0A |
| JPEG | FF D8 FF |
| PDF | 25 50 44 46 2D |
| ELF | 7F 45 4C 46 |
| ZIP (common local file header) | 50 4B 03 04 |

File signatures can help identify file formats even when file extensions are missing or incorrect. A signature alone does not guarantee that a file is valid or safe.

### Cryptography

Cryptographic hashes, encryption keys and binary data are frequently represented in hexadecimal.

A SHA-256 digest contains 256 bits, which can be represented using 64 hexadecimal characters.

Hexadecimal is only a representation of data. It does not provide encryption or confidentiality.

### Reverse Engineering

Machine instructions, executable files, memory addresses and register values are frequently displayed in hexadecimal.

Understanding binary, hexadecimal and bitwise operations is essential when analysing compiled programs.

### Vulnerability Research

Incorrect handling of integer values can lead to vulnerabilities such as:

- Integer overflow
- Integer underflow
- Signedness errors
- Incorrect memory allocation
- Out-of-bounds memory access

Understanding how integers are represented and manipulated helps explain why these vulnerabilities occur.

## Key Takeaways

- Computers represent digital information using binary.
- Decimal uses base 10, binary uses base 2, octal uses base 8 and hexadecimal uses base 16.
- One hexadecimal digit represents four bits.
- One octal digit represents three bits.
- One byte contains eight bits.
- Two's complement is used to represent signed integers.
- Bitwise operations manipulate individual bits.
- Integer representation and overflow are important in software security.
- Binary and hexadecimal are fundamental to networking, cryptography, digital forensics and reverse engineering.
