# GE102 Module: Conversion of Number Systems

**Mathematics in the Modern World (GE102)** · Prepared by **Clinton Joshua S. Anoche** · 2 hours

This 2-hour module teaches students to convert values among the decimal, binary, octal, hexadecimal, and binary-coded decimal (BCD) number systems, in any direction.

## Contents

- [Module Information](#module-information)
- [Learning Outcomes](#learning-outcomes)
- [Time Allocation](#time-allocation)
- [Part 1: Introduction to Number Systems](#part-1-introduction-to-number-systems-10-minutes)
- [Part 2: Decimal and Binary](#part-2-decimal-and-binary-20-minutes)
- [Part 3: Decimal with Octal and Hexadecimal](#part-3-decimal-with-octal-and-hexadecimal-20-minutes)
- [Part 4: Binary, Octal, and Hexadecimal by Grouping](#part-4-binary-octal-and-hexadecimal-by-grouping-15-minutes)
- [Part 5: Binary-Coded Decimal (BCD)](#part-5-binary-coded-decimal-bcd-15-minutes)
- [Part 6: Converting Among All Systems](#part-6-converting-among-all-systems-10-minutes)
- [Practice Activities](#practice-activities-15-minutes)
- [Closing and Synthesis](#closing-and-synthesis-10-minutes)
- [Assignment](#assignment)
- [References](#references)

## Module Information

| Item | Details |
| --- | --- |
| Course | Mathematics in the Modern World |
| Course code | GE102 |
| Module topic | Conversion of values among decimal, binary, octal, hexadecimal, and binary-coded decimal number systems |
| Prepared by | Clinton Joshua S. Anoche |
| Target learners | College students (General Education) |
| Duration | 2 hours (120 minutes) |
| Assessment | Guided and independent practice sets in this module |

## Learning Outcomes

By the end of this module, students should be able to:

1. Explain positional notation, base, and digit sets for the five number systems.
2. Convert between decimal and binary using repeated division and place-value expansion.
3. Convert between decimal and octal or hexadecimal.
4. Convert among binary, octal, and hexadecimal by grouping bits.
5. Encode and decode decimal numbers in 8421 BCD.
6. Convert a value from any one of the five systems to any other, and check the result by converting back.

## Time Allocation

The 120 minutes are split into seven teaching parts, two practice blocks, and a closing synthesis.

| Segment | Content | Minutes |
| --- | --- | --- |
| Opening | Hook, outcomes, quick review of place value | 5 |
| Part 1 | Introduction to number systems | 10 |
| Part 2 | Decimal and binary | 20 |
| Part 3 | Decimal with octal and hexadecimal | 20 |
| Part 4 | Binary, octal, hexadecimal by grouping | 15 |
| Part 5 | Binary-coded decimal (BCD) | 15 |
| Part 6 | Converting among all systems | 10 |
| Practice | Guided practice (pairs) and independent activity | 15 |
| Closing | Synthesis, reflection, assignment | 10 |
| **Total** |  | **120** |

**Materials:** whiteboard or slides, printed copy of this module, and scratch paper. Calculators are allowed only to check answers, not to convert.

## Part 1: Introduction to Number Systems (10 minutes)

Every number system is positional: a digit's value depends on its position, and each position is worth a power of the base.

**Motivation.** We count in base 10 because we have ten fingers, but computers store everything as on/off signals, so they work in base 2. Octal and hexadecimal are compact ways for people to read long binary strings, and BCD is how calculators, digital clocks, and cash registers keep decimal digits exact.

### Positional notation

A whole number with digits d(n) ... d(1) d(0) in base b has the value:

```math
N = d_n b^n + d_{n-1} b^{n-1} + \cdots + d_1 b^1 + d_0 b^0
```

Example in base 10: 4,306 = 4(10³) + 3(10²) + 0(10¹) + 6(10⁰).

### The five systems

| System | Base | Digits used | Written as |
| --- | --- | --- | --- |
| Decimal | 10 | 0 to 9 | 156₁₀ |
| Binary | 2 | 0, 1 | 10011100₂ |
| Octal | 8 | 0 to 7 | 234₈ |
| Hexadecimal | 16 | 0 to 9, A to F (A=10, B=11, C=12, D=13, E=14, F=15) | 9C₁₆ |
| BCD (8421) | 10 (coded in 4-bit groups) | each decimal digit written as 4 bits | 0001 0101 0110 |

The subscript tells which system a numeral belongs to. Without it, 101 could mean one hundred one, five, sixty-five, or 257.

### Reference table: 0 to 15

Students should know this table by heart; it powers every shortcut later in the module.

| Decimal | Binary | Octal | Hexadecimal | BCD |
| --- | --- | --- | --- | --- |
| 0 | 0000 | 0 | 0 | 0000 |
| 1 | 0001 | 1 | 1 | 0001 |
| 2 | 0010 | 2 | 2 | 0010 |
| 3 | 0011 | 3 | 3 | 0011 |
| 4 | 0100 | 4 | 4 | 0100 |
| 5 | 0101 | 5 | 5 | 0101 |
| 6 | 0110 | 6 | 6 | 0110 |
| 7 | 0111 | 7 | 7 | 0111 |
| 8 | 1000 | 10 | 8 | 1000 |
| 9 | 1001 | 11 | 9 | 1001 |
| 10 | 1010 | 12 | A | 0001 0000 |
| 11 | 1011 | 13 | B | 0001 0001 |
| 12 | 1100 | 14 | C | 0001 0010 |
| 13 | 1101 | 15 | D | 0001 0011 |
| 14 | 1110 | 16 | E | 0001 0100 |
| 15 | 1111 | 17 | F | 0001 0101 |

**Quick check (2 minutes, whole class):** What is the value of the digit 7 in 7,350₁₀? In 1070₈? Answer: 7,000 (7 × 10³), and 7 × 8¹ = 56.

## Part 2: Decimal and Binary (20 minutes)

To go from binary to decimal, add up the place values; to go from decimal to binary, divide by 2 repeatedly and collect the remainders.

### Binary to decimal: place-value expansion

The place values in binary are powers of 2:

| Position | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Place value | 128 | 64 | 32 | 16 | 8 | 4 | 2 | 1 |

**Example 1.** Convert 101101₂ to decimal.

| Bit | 1 | 0 | 1 | 1 | 0 | 1 |
| --- | --- | --- | --- | --- | --- | --- |
| Place value | 32 | 16 | 8 | 4 | 2 | 1 |
| Contribution | 32 | 0 | 8 | 4 | 0 | 1 |

Sum: 32 + 8 + 4 + 1 = **45**. So 101101₂ = 45₁₀.

### Decimal to binary: repeated division by 2

**Steps.**

1. Divide the number by 2 and write the quotient and the remainder (0 or 1).
2. Divide the quotient by 2 again. Repeat until the quotient is 0.
3. Read the remainders from the last one to the first (bottom to top).

**Example 2.** Convert 156₁₀ to binary.

| Division | Quotient | Remainder |
| --- | --- | --- |
| 156 ÷ 2 | 78 | 0 |
| 78 ÷ 2 | 39 | 0 |
| 39 ÷ 2 | 19 | 1 |
| 19 ÷ 2 | 9 | 1 |
| 9 ÷ 2 | 4 | 1 |
| 4 ÷ 2 | 2 | 0 |
| 2 ÷ 2 | 1 | 0 |
| 1 ÷ 2 | 0 | 1 |

Reading the remainders from bottom to top gives **10011100**. So 156₁₀ = 10011100₂.

**Check:** 128 + 16 + 8 + 4 = 156.

**Example 3.** Convert 83₁₀ to binary using subtraction of place values: 83 = 64 + 16 + 2 + 1, so the bits for 64, 16, 2, and 1 are 1 and all others are 0. Result: **1010011₂**.

### Fractions (enrichment)

For the fractional part, multiply by 2 repeatedly and record the whole-number part each time, reading top to bottom.

**Example 4.** Convert 0.625₁₀ to binary.

| Multiplication | Product | Bit |
| --- | --- | --- |
| 0.625 × 2 | 1.25 | 1 |
| 0.25 × 2 | 0.5 | 0 |
| 0.5 × 2 | 1.0 | 1 |

So 0.625₁₀ = 0.101₂. Together with the whole part, 13.625₁₀ = 1101.101₂. Going back: the place values after the point are 1/2, 1/4, 1/8, so 0.101₂ = 1/2 + 1/8 = 0.625.

**Try it (3 minutes, pairs):** Convert 214₁₀ to binary and 11010110₂ to decimal. Answers: 11010110₂ and 214₁₀. (They are the same number, so each answer checks the other.)

## Part 3: Decimal with Octal and Hexadecimal (20 minutes)

The two methods from Part 2 work for any base: expand by place value to reach decimal, and divide repeatedly by the target base to leave decimal.

| Direction | Method | Divide or multiply by |
| --- | --- | --- |
| Octal or hexadecimal to decimal | Multiply each digit by its place value and add | Powers of 8 or 16 |
| Decimal to octal | Repeated division, read remainders bottom to top | 8 |
| Decimal to hexadecimal | Repeated division, read remainders bottom to top; write remainders 10 to 15 as A to F | 16 |

### Octal

Place values: ... 4096, 512, 64, 8, 1.

**Example 5.** Convert 365₈ to decimal.

3(64) + 6(8) + 5(1) = 192 + 48 + 5 = **245**. So 365₈ = 245₁₀.

**Example 6.** Convert 245₁₀ to octal.

| Division | Quotient | Remainder |
| --- | --- | --- |
| 245 ÷ 8 | 30 | 5 |
| 30 ÷ 8 | 3 | 6 |
| 3 ÷ 8 | 0 | 3 |

Read bottom to top: **365₈**, which matches Example 5.

### Hexadecimal

Place values: ... 4096, 256, 16, 1. Remember A=10, B=11, C=12, D=13, E=14, F=15.

**Example 7.** Convert 2F9₁₆ to decimal.

2(256) + 15(16) + 9(1) = 512 + 240 + 9 = **761**. So 2F9₁₆ = 761₁₀.

**Example 8.** Convert 761₁₀ to hexadecimal.

| Division | Quotient | Remainder | Hex digit |
| --- | --- | --- | --- |
| 761 ÷ 16 | 47 | 9 | 9 |
| 47 ÷ 16 | 2 | 15 | F |
| 2 ÷ 16 | 0 | 2 | 2 |

Read bottom to top: **2F9₁₆**, which matches Example 7.

**Example 9.** Convert 1000₁₀ to octal and to hexadecimal.

- Octal: 1000 ÷ 8 = 125 r 0; 125 ÷ 8 = 15 r 5; 15 ÷ 8 = 1 r 7; 1 ÷ 8 = 0 r 1. Read upward: **1750₈**.
- Hexadecimal: 1000 ÷ 16 = 62 r 8; 62 ÷ 16 = 3 r 14 (E); 3 ÷ 16 = 0 r 3. Read upward: **3E8₁₆**.

**Common mistakes to watch for:**

- Reading the remainders top to bottom instead of bottom to top.
- Writing 10 to 15 as two digits in hexadecimal instead of A to F.
- Using the digits 8 or 9 in an octal numeral (they do not exist in base 8).

**Try it (3 minutes, pairs):** Convert 725₈ and 1A4₁₆ to decimal. Answers: 469 and 420.

## Part 4: Binary, Octal, and Hexadecimal by Grouping (15 minutes)

Because 8 = 2³ and 16 = 2⁴, one octal digit equals exactly 3 bits and one hexadecimal digit equals exactly 4 bits, so no division is needed.

| Conversion | Group the bits in | Start grouping from |
| --- | --- | --- |
| Binary to octal | 3s | The right (the binary point for fractions) |
| Binary to hexadecimal | 4s | The right |
| Octal to binary | Replace each digit with 3 bits | |
| Hexadecimal to binary | Replace each digit with 4 bits | |

Pad the leftmost group with zeros if it is short. Zeros on the far left do not change the value.

**Example 10.** Convert 101101110₂ to octal and to hexadecimal.

- Octal (groups of 3): 101 | 101 | 110 = 5 | 5 | 6, so **556₈**.
- Hexadecimal (groups of 4, padded): 0001 | 0110 | 1110 = 1 | 6 | E, so **16E₁₆**.
- Check: all three equal 366 in decimal.

**Example 11.** Convert 7A3₁₆ to binary.

7 = 0111, A = 1010, 3 = 0011. Result: **011110100011₂** (the leading 0 may be dropped: 11110100011₂).

**Example 12.** Convert 2475₈ to binary.

2 = 010, 4 = 100, 7 = 111, 5 = 101. Result: **010100111101₂** (or 10100111101₂).

### Octal to hexadecimal and back: use binary as the bridge

There is no direct digit-to-digit rule between octal and hexadecimal, so go through binary: expand, then regroup.

**Example 13.** Convert 556₈ to hexadecimal.

1. Octal to binary: 5 = 101, 5 = 101, 6 = 110, giving 101101110.
2. Regroup in 4s from the right: 0001 | 0110 | 1110.
3. Hexadecimal digits: **16E₁₆**.

**Example 14.** Convert A5₁₆ to octal.

1. Hexadecimal to binary: A = 1010, 5 = 0101, giving 10100101.
2. Regroup in 3s from the right: 010 | 100 | 101.
3. Octal digits: **245₈**.
4. Check: A5₁₆ = 10(16) + 5 = 165 and 245₈ = 2(64) + 4(8) + 5 = 165.

**Try it (3 minutes, pairs):** Convert 10110111₂ to hexadecimal and 3F₁₆ to octal. Answers: B7₁₆ and 77₈.

## Part 5: Binary-Coded Decimal (BCD) (15 minutes)

BCD writes each decimal digit separately as a 4-bit binary group, so it is a code for decimal digits, not a base that converts by place value.

The 8421 BCD weights in each group are 8, 4, 2, and 1. Only the codes 0000 to 1001 (0 to 9) are valid. The groups 1010 to 1111 never appear in BCD.

| Decimal digit | 0 | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 9 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| BCD | 0000 | 0001 | 0010 | 0011 | 0100 | 0101 | 0110 | 0111 | 1000 | 1001 |

### Decimal to BCD and BCD to decimal

**Example 15.** Convert 468₁₀ to BCD. Encode each digit: 4 = 0100, 6 = 0110, 8 = 1000. Result: **0100 0110 1000**.

**Example 16.** Convert 1001 0011 0101 (BCD) to decimal. Split into groups of 4: 1001 = 9, 0011 = 3, 0101 = 5. Result: **935₁₀**.

### BCD is not the same as binary

Compare 45₁₀ in the two forms:

| Form | Value of 45₁₀ | Bits used |
| --- | --- | --- |
| Pure binary | 101101 | 6 |
| BCD | 0100 0101 | 8 |

BCD needs more bits, but it keeps each decimal digit separate, which makes display and exact decimal arithmetic simple.

### BCD with the other systems

There is no direct shortcut between BCD and binary, octal, or hexadecimal, because BCD groups follow decimal digits. Always go through decimal.

| To convert | Route |
| --- | --- |
| BCD to binary, octal, or hexadecimal | BCD → decimal → target system |
| Binary, octal, or hexadecimal to BCD | Source system → decimal → BCD |

**Example 17.** Convert 0010 0111 (BCD) to binary and to hexadecimal.

1. BCD to decimal: 0010 = 2, 0111 = 7, so 27₁₀.
2. Decimal to binary: 27 = 16 + 8 + 2 + 1, so **11011₂**.
3. Decimal to hexadecimal: 27 ÷ 16 = 1 r 11 (B), so **1B₁₆**.

**Example 18.** Convert 11001010₂ to BCD.

1. Binary to decimal: 128 + 64 + 8 + 2 = 202.
2. Decimal to BCD: 2 = 0010, 0 = 0000, 2 = 0010.
3. Result: **0010 0000 0010**.

**Example 19.** Convert 365₈ to BCD. Octal to decimal gives 245, and decimal to BCD gives **0010 0100 0101**.

**Try it (3 minutes, pairs):** Convert 5E₁₆ to BCD. Answer: 5E₁₆ = 94₁₀ = **1001 0100**.

## Part 6: Converting Among All Systems (10 minutes)

Any conversion can be done with two hubs: use binary as the bridge for octal and hexadecimal, and use decimal as the bridge for BCD.

### Route map

Read each row as "from this system" and each column as "to this system".

| From \\ To | Decimal | Binary | Octal | Hexadecimal | BCD |
| --- | --- | --- | --- | --- | --- |
| **Decimal** | n/a | Divide by 2 | Divide by 8 | Divide by 16 | Encode each digit in 4 bits |
| **Binary** | Place values | n/a | Group in 3s | Group in 4s | Via decimal |
| **Octal** | Place values | Each digit to 3 bits | Via binary | Via binary | Via decimal |
| **Hexadecimal** | Place values | Each digit to 4 bits | Via binary | Via binary | Via decimal |
| **BCD** | Decode each 4-bit group | Via decimal | Via decimal | Via decimal | n/a |

### Full-cycle example

**Example 20.** Start with 156₁₀ and convert it to every other system, then return to decimal.

| Step | Conversion | Method | Result |
| --- | --- | --- | --- |
| 1 | Decimal to binary | Divide by 2 (Example 2) | 10011100 |
| 2 | Binary to octal | Groups of 3: 010 \| 011 \| 100 | 234 |
| 3 | Binary to hexadecimal | Groups of 4: 1001 \| 1100 | 9C |
| 4 | Decimal to BCD | Encode 1, 5, 6 | 0001 0101 0110 |
| 5 | BCD back to decimal | Decode 0001, 0101, 0110 | 156 |

The same number in all five systems:

| Decimal | Binary | Octal | Hexadecimal | BCD |
| --- | --- | --- | --- | --- |
| 156 | 10011100 | 234 | 9C | 0001 0101 0110 |

**Check every result back to decimal:** 2(64) + 3(8) + 4 = 156 and 9(16) + 12 = 156.

### Habits that prevent errors

- Always write the base as a subscript.
- Convert back to decimal to check your answer.
- When grouping bits, start from the right and pad on the left.
- Never use a digit that is not allowed in the base (no 8 in octal, no letters past F in hexadecimal).

## Practice Activities (15 minutes)

Students first work in pairs on Set A (6 minutes), then individually on Set B (9 minutes). Show all steps; answers without solutions earn no credit.

### Set A: Guided practice (pairs)

1. Convert 37₁₀ to binary.
2. Convert 1100111₂ to decimal.
3. Convert 612₈ to decimal.
4. Convert 2C7₁₆ to decimal.
5. Convert 110101101₂ to octal and to hexadecimal.
6. Convert 429₁₀ to BCD.

### Set B: Independent activity

1. Convert 201₁₀ to binary.
2. Convert 101011₂ to decimal.
3. Convert 500₁₀ to octal.
4. Convert 3F2₁₆ to decimal.
5. Convert 777₈ to binary.
6. Convert 11101001₂ to hexadecimal.
7. Convert 659₁₀ to BCD.
8. Convert 0011 1000 0111 (BCD) to decimal.
9. Convert 2B₁₆ to octal.
10. Convert 1D₁₆ to BCD.
11. Challenge: Convert 0101 0010 0110 (BCD) to binary and to hexadecimal.

### Answer key (for the facilitator)

| Item | Answer | Key step |
| --- | --- | --- |
| A1 | 100101₂ | 32 + 4 + 1 = 37 |
| A2 | 103₁₀ | 64 + 32 + 4 + 2 + 1 |
| A3 | 394₁₀ | 6(64) + 1(8) + 2 |
| A4 | 711₁₀ | 2(256) + 12(16) + 7 |
| A5 | 655₈ and 1AD₁₆ | Groups 110 \| 101 \| 101 and 0001 \| 1010 \| 1101; both equal 429₁₀ |
| A6 | 0100 0010 1001 | Encode 4, 2, 9 |
| B1 | 11001001₂ | 128 + 64 + 8 + 1 = 201 |
| B2 | 43₁₀ | 32 + 8 + 2 + 1 |
| B3 | 764₈ | 500 ÷ 8 = 62 r 4; 62 ÷ 8 = 7 r 6; 7 ÷ 8 = 0 r 7 |
| B4 | 1010₁₀ | 3(256) + 15(16) + 2 |
| B5 | 111111111₂ | 7 = 111, repeated three times |
| B6 | E9₁₆ | 1110 = E, 1001 = 9 |
| B7 | 0110 0101 1001 | Encode 6, 5, 9 |
| B8 | 387₁₀ | 0011 = 3, 1000 = 8, 0111 = 7 |
| B9 | 53₈ | 2B = 0010 1011 = 101011 = 101 \| 011 |
| B10 | 0010 1001 | 1D₁₆ = 29₁₀, then encode 2 and 9 |
| B11 | 1000001110₂ and 20E₁₆ | BCD gives 526₁₀; 526 = 512 + 8 + 4 + 2; 526 ÷ 16 = 32 r 14 (E), 32 ÷ 16 = 2 r 0 |

## Closing and Synthesis (10 minutes)

Students leave knowing one method per conversion and a way to check each answer.

**Summary of the module**

- Every number system is positional: value = sum of digit × base^position.
- Decimal to any base: divide repeatedly by the base and read the remainders upward.
- Any base to decimal: expand by place values.
- Binary, octal, and hexadecimal convert by grouping bits in 3s (octal) and 4s (hexadecimal).
- BCD stores each decimal digit as 4 bits; convert to or from other systems through decimal.

**Reflection questions (5 minutes, think-pair-share)**

1. Why do computer engineers prefer hexadecimal over long binary strings?
2. Why does 45₁₀ need 6 bits in binary but 8 bits in BCD?
3. Which conversion do you find hardest, and which check will you use to catch your own mistakes?

## Assignment

Submit on paper or as a file before the next meeting. Show complete solutions.

1. Convert 1,024₁₀ to binary, octal, hexadecimal, and BCD.
2. Convert 7F3₁₆ to decimal, binary, and octal.
3. Convert 0111 1001 0001 (BCD) to decimal, binary, and hexadecimal.
4. Convert 1011011101₂ to octal and hexadecimal by grouping.
5. Write a short paragraph explaining where each of the five systems is used in everyday technology.

## References

Supplementary reading (confirm the edition available in your library):

- Floyd, T. *Digital Fundamentals*. Pearson.
- Mano, M. M., and Ciletti, M. D. *Digital Design*. Pearson.
- The prescribed GE102 Mathematics in the Modern World text and syllabus of the course.
