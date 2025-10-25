# 🧩 Pin Extractor (Poem Cryptography Challenge)

## Project Description

This Python script contains the complete solution to the "Pin Extractor" coding challenge. 
The core of the project is a single function, `pin_extractor`, designed to decode a secret 
numerical PIN hidden within a collection of poems or multi-line strings.

The function iterates through multiple poems, processes each one line-by-line, and 
extracts a digit based on the length of a specific word in that line.

## The Decoding Logic

The secret PIN digit for the $n$-th line of a poem is determined by the length of the $n$-th 
word in that line, following these rules:

1. **Line Index (n):** Used as the index to select the word.
2. **Word Index:** The $n$-th word in the line is selected (e.g., line_index 0 uses words[0]).
3. **Digit Value:**
    * If the length of the $n$-th word is **greater than** the line index ($n$), the digit is the **word's length**.
    * Otherwise (if the word is too short or the length is <= $n$), the digit is **'0'**.

The function returns a list of strings, where each string is the extracted secret code for one poem.

## Usage Example

The execution section at the bottom of this file demonstrates how to call the function 
with a list of sample poems and prints the resulting secret codes.

To run this file:
```bash
python documentation.py
```

"""
