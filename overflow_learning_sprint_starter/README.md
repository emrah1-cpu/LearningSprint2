# Overflow Lab — Interactive Integer Overflow Visualizer

A safe, interactive teaching module for **SE/CprE 4210 Learning Sprint #2, Problem 1**.

## What the app teaches

- Why integer types have a fixed numerical range.
- What happens when fixed-width arithmetic wraps past that range.
- How **signed two's-complement** and **unsigned** interpretations differ.
- How the bit representation relates to decimal and hexadecimal values.
- Why **signed overflow in C is undefined behavior**, even though two's-complement hardware may wrap.

## Run locally

1. Download or clone this repository.
2. Double-click `index.html` or open it in a modern web browser.
3. No installation, server, external packages, or account is required.

## Interactive features

1. Select a 4-, 8-, 16-, or 32-bit integer width.
2. Choose signed or unsigned interpretation.
3. Enter operands A and B and select addition or subtraction.
4. View the mathematical answer, stored result, decimal/hex output, and each bit.
5. Use the four preset buttons to explore overflow, underflow, and an in-range example.

## Example cases

| Mode | Width | Expression | Math result | Stored result |
| --- | --- | --- | --- | --- |
| Signed | 8-bit | 120 + 20 | 140 | -116 |
| Unsigned | 8-bit | 255 + 1 | 256 | 0 |
| Unsigned | 8-bit | 0 - 1 | -1 | 255 |
| Signed | 8-bit | 8 + 12 | 20 | 20 |
| Signed | 4-bit | 7 + 1 | 8 | -8 |

## Implementation notes

All arithmetic uses JavaScript `BigInt` to preserve exact results. The program masks results to the selected width using modulo `2^n`, then interprets the stored bits as signed or unsigned. Input validation rejects decimals, malformed numbers, and operands outside the selected type's range.

This is an educational visualization; it does not execute user code or exploit any vulnerability. It does not perform network requests or store personal data.

## Automated tests (optional)

If you have Node.js installed, run `node test.js`. The app itself does not require Node.js.

## Sprint team

- Group: Hackerteam # 22
- Contributors: Emrah Sadikov -- Application development, testing, documentation
- Repository: https://github.com/emrah1-cpu/LearningSprint2

## Reflection

See [`reflection.md`](reflection.md). Replace the prompts with your group's genuine development experience before submitting.
