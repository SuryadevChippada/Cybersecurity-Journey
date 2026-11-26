# Boolean Logic

## Overview

Boolean logic is a mathematical system based on two values: true (1) and false (0). Computers use Boolean logic to make decisions, evaluate conditions and process binary data.

Boolean algebra was developed by George Boole. It forms the basis of digital circuits, programming and computer architecture.

## Boolean Values

| Value | Meaning |
|---|---|
| 0 | False |
| 1 | True |

## Logic Gates

Logic gates take binary inputs and produce a binary output according to a specific logical operation.

### AND

AND returns true only when both inputs are true.

Example: Access requires a valid password and successful MFA.

### OR

OR returns true when at least one input is true.

Example: An alert is generated when either of two detection conditions is met.

### NOT

NOT reverses the input value.

| A | NOT A |
|---|---|
| 0 | 1 |
| 1 | 0 |

### XOR

Exclusive OR returns true when two inputs are different. It is commonly used in cryptography and bit manipulation.

### NAND

NAND is the inverse of AND. It returns false only when both inputs are true.

### NOR

NOR is the inverse of OR. It returns true only when both inputs are false.

### XNOR

XNOR is the inverse of XOR. It returns true when both inputs are equal.

## Truth Tables

A truth table shows the output of a logical expression for every possible combination of inputs.

| A | B | AND | OR | XOR | NAND | NOR | XNOR |
|---|---|---|---|---|---|---|---|
| 0 | 0 | 0 | 0 | 0 | 1 | 1 | 1 |
| 0 | 1 | 0 | 1 | 1 | 1 | 0 | 0 |
| 1 | 0 | 0 | 1 | 1 | 1 | 0 | 0 |
| 1 | 1 | 1 | 1 | 0 | 0 | 0 | 1 |

For n Boolean inputs, there are 2^n possible input combinations.

## Boolean Algebra

Boolean algebra provides rules for simplifying logical expressions. In the following expressions, `·` means AND, `+` means OR and `¬` means NOT. These are logical operations, not ordinary arithmetic.

| Law | Expression |
|---|---|
| Identity | A · 1 = A; A + 0 = A |
| Domination | A · 0 = 0; A + 1 = 1 |
| Idempotent | A · A = A; A + A = A |
| Complement | A · ¬A = 0; A + ¬A = 1 |
| Double negation | ¬(¬A) = A |
| Commutative | A · B = B · A; A + B = B + A |
| Associative | (A · B) · C = A · (B · C); (A + B) + C = A + (B + C) |
| Distributive | A · (B + C) = (A · B) + (A · C) |
| Distributive (dual) | A + (B · C) = (A + B) · (A + C) |
| Absorption | A + (A · B) = A; A · (A + B) = A |

## De Morgan's Laws

De Morgan's laws explain how negation affects AND and OR expressions.

```text
NOT (A AND B) = (NOT A) OR (NOT B)
NOT (A OR B)  = (NOT A) AND (NOT B)
```

For example, denying access when either authentication requirement fails is equivalent to denying access when both requirements are not satisfied together.

## Simplifying Boolean Expressions

```text
(A AND B) OR (A AND NOT B)
= A AND (B OR NOT B)
= A AND 1
= A
```

Simplification reduces unnecessary operations and can make program conditions and digital circuits easier to understand.

## Operator Precedence

In conventional Boolean algebra, NOT is evaluated before AND, and AND before OR. Parentheses make the intended evaluation explicit. Programming languages have their own precedence rules.

```text
NOT 0 AND 1 OR 0
= 1 AND 1 OR 0
= 1 OR 0
= 1
```

## Logical and Bitwise Operators

Logical operators evaluate truth values, while bitwise operators operate on individual bits of integers.

| Operation | Python logical | C++ logical | Bitwise (Python/C++) |
|---|---|---|---|
| AND | `and` | `&&` | `&` |
| OR | `or` | `||` | `\|` |
| NOT | `not` | `!` | `~` |
| XOR | `!=` (Boolean operands) | `!=` (Boolean operands) | `^` |

Python's `and` and `or` can return an operand rather than a Boolean when used with non-Boolean values.

## Practical Examples

### Access Control in Python

```python
password_valid = True
mfa_valid = False
account_locked = False

access_granted = password_valid and mfa_valid and not account_locked
print(access_granted)
```

Expected output:

```text
False
```

### Short-Circuit Evaluation in C++

```cpp
#include <iostream>

int main() {
    int denominator = 0;
    bool valid = denominator != 0 && 10 / denominator > 2;
    std::cout << std::boolalpha << valid << '\n';
}
```

Expected output:

```text
false
```

The second condition is not evaluated because the first condition is false. This prevents division by zero in this example. Logical OR similarly stops evaluating once its left operand is true.

### Bit Masking

```python
READ = 0b100
WRITE = 0b010
EXECUTE = 0b001

permissions = READ | EXECUTE
print(bool(permissions & READ))
print(bool(permissions & WRITE))

permissions |= WRITE
permissions &= ~EXECUTE
print(bin(permissions))
```

Expected output:

```text
True
False
0b110
```

## Boolean Logic in Computer Hardware

NAND and NOR are universal gates because either gate type alone can be combined to implement any Boolean function.

A half adder uses XOR to calculate the sum bit and AND to calculate the carry bit.

| A | B | Sum (XOR) | Carry (AND) |
|---|---|---|---|
| 0 | 0 | 0 | 0 |
| 0 | 1 | 1 | 0 |
| 1 | 0 | 1 | 0 |
| 1 | 1 | 0 | 1 |

A full adder also accepts a carry-in bit. Adders are fundamental components of arithmetic logic units (ALUs) in processors.

## Applications in Cybersecurity

- **Access control:** Combine authentication, authorization and account-status conditions to determine whether access is permitted.
- **Firewall rules:** Combine conditions involving addresses, ports and protocols to match network traffic.
- **Networking:** Bitwise AND combines an IP address with a subnet mask to determine the network address.
- **Cryptography:** XOR and other bitwise operations are components of cryptographic algorithms. XOR by itself does not guarantee secure encryption.
- **Detection engineering:** Combine indicators and conditions to identify suspicious activity.
- **Vulnerability research:** Incorrect logical conditions can cause authentication bypasses, authorization errors and input-validation failures.

For example, using OR instead of AND when both a valid password and MFA are required would incorrectly allow access when only one requirement is satisfied.

## Practical Exercises

- Construct truth tables for expressions with three inputs.
- Simplify `(A AND B) OR (A AND NOT B)` using Boolean algebra.
- Verify both De Morgan's laws using truth tables.
- Implement all seven logic gates in Python or C++.
- Modify the access-control example and test every combination of inputs.
- Implement a half adder using XOR and AND.

## Key Takeaways

- Boolean logic operates on true and false values.
- AND, OR and NOT are fundamental logical operations.
- XOR checks whether two Boolean inputs differ.
- NAND and NOR are universal gates.
- Truth tables describe all possible input and output combinations.
- Boolean algebra helps simplify logical expressions.
- Logical operators and bitwise operators serve different purposes.
- Correct Boolean conditions are essential for secure software and access control.
