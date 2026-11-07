---
tags:
  - encoding
  - theory
---
# ASCII code

- $7$ bits ($128$ characters)
- $0$ through $31$: Control/non-printable characters
- $32$ through $64$: Punctuation, symbols, numbers and space
- $65$ through $90$: Uppercase English alphabet letters
- $91$ to $96$: Additional graphemes, such as [ and \
- $97$ to $122$: Lowercase English alphabet letters
- $123$ through $126$: Additional graphemes, such as { and |
- $127$: Control/non-printable character (DEL)
- Extended ASCII: $8$ bits ($256$ characters)

# Unicode

- Either $8$, $16$ or $32$ bits (UTF-$8$, UTF-$16$, UTF-$32$)
- Capable of encoding a maximum of $1,114,112$ characters
- Currently, as of Unicode version $17.0$, there are $297,334$ assigned characters with code points


# Advantage of Unicode over ASCII code

- Uses less storage

# Disadvantage of Unicode over ASCII code

- Supports many more characters
- Reduces encoding problems

| Character Encoding | Description |
| ------------------ | ----------- |

\| ASCII | • Only 128 distinct characters as each character is 7 bits long\
• First 32 characters are non-printing characters used to control devices\
• Sometimes represented in HEX as it only requires 2 digits |\
\| Unicode | • Not standard number of bits (8–32), as many more characters can be represented\
• Used primarily for characters of other languages\
• More frequently used characters have fewer bits |

Formatted from the image with the original wording retained as closely as possible. Note: the source's statement that PWAs cannot use APIs is not generally accurate; modern PWAs can access supported web APIs.
