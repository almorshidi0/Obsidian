This episode explains how computers store and represent numerical data and text using binary, building on the logic gates and binary concepts introduced in the previous episode. It also discusses the importance of standards like ASCII and Unicode for interoperability.

## 🔢 Binary Numbers
*   Computers use **binary numbers** (base-2) to represent numerical data.
    *   Like decimal numbers (base-10), binary numbers use place values, but instead of powers of 10 (1, 10, 100), they use powers of 2 (1, 2, 4, 8).
    *   Each digit in a binary number is called a **bit**.
*   For example, the binary number 101 represents (1 \* 4) + (0 \* 2) + (1 \* 1) = 5 in decimal.
*   Larger numbers require more digits (bits) in binary. For example:
    *   10110111 (binary) is (1\*128) + (0\*64) + (1\*32) + (1\*16) + (0\*8) + (1\*4) + (1\*2) + (1\*1) = 183 (decimal)
*   **Binary Addition** works similarly to decimal addition, with carries when a sum exceeds the base. For example, 183 + 19 in binary is 10110111 + 00010011 = 11001010, which is 202 in decimal.

## 💾 Bits and Bytes
*   A **bit** is a single binary digit (0 or 1).
*   A **byte** is a group of 8 bits.
*   Larger units are built from bytes:
    *   **Kilobyte (KB):** 1000 bytes or 1024 bytes (2^10).
    *   **Megabyte (MB):** 1 million bytes.
    *   **Gigabyte (GB):** 1 billion bytes.
    *  **Terabyte (TB):** 1 trillion bytes.
*   Computers often operate in chunks of bits such as 8-bit, 32-bit or 64-bit.
    *   An 8-bit system can represent 256 (2^8) different values.
    *   A 32-bit system can represent just under 4.3 billion different values.
    *   A 64-bit system can represent around 9.2 quintillion different values.

## ➕ Negative Numbers and Floating Points
*   To represent **negative numbers**, computers typically use the first bit as a sign bit: 0 for positive and 1 for negative.
*  This reduces the range of values but allows for both positive and negative number representation.
*   **Floating-point numbers** are used to represent numbers with decimal points.
    *   These are stored in a way similar to scientific notation, with a significand (the number) and an exponent.
   *   The **IEEE 754 standard** is most commonly used. In a 32-bit system, 1 bit is for the sign, 8 for the exponent, and 23 for the significand.

## 🔤 Representing Text
*   Computers use numbers to represent letters and symbols.
*   Early methods included numbering the alphabet (A=1, B=2, etc.).
    *   Francis Bacon used 5-bit sequences to encode letters.

### 📜 ASCII
*   **ASCII (American Standard Code for Information Interchange)** is a 7-bit code that can represent 128 different characters, including upper and lowercase letters, numbers, punctuation, and control codes.
    *   For example, 'a' is 97, 'A' is 65, ':' is 58.
*   ASCII allowed different computers to exchange data (**interoperability**).
*   Extended ASCII used 8-bits and the extra 128 codes to represent "national characters". This was not standardized, leading to issues when sharing data across countries.

### 🌍 Unicode
*   **Unicode** is a universal encoding scheme that uses 16-bits, with space for over a million codes.
    *   It encompasses every character from every language, mathematical symbols, and graphical characters like emoji.
*   Unicode resolved the problem of incompatibility among different national character codes.

## 🎬 Everything is Binary
*   Under the hood, everything on a computer is represented by sequences of bits.
    *   Text messages, videos, web pages, and even operating systems are long strings of 1s and 0s.

This episode explains how all forms of information can be represented using binary numbers, from positive and negative integers, to floating-point values, to text characters, setting the stage for the next episode which will begin exploring how computers manipulate these binary sequences.
