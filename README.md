🧩 Pin Extractor (Poem Cryptography Challenge)

Project Description

This repository contains a solution to the "Pin Extractor" coding challenge. The core of the project is a single Python function, pin_extractor, designed to decode a secret numerical PIN hidden within a collection of poems or multi-line strings.

The project demonstrates key Python concepts, including:

Function definition and iteration over input lists.

String manipulation (.split() with custom delimiters like \n).

List iteration using enumerate to access both index and value simultaneously.

Conditional logic to prevent IndexError and apply the decoding rules.

The Decoding Logic

The secret PIN digit for the $n$-th line of a poem is determined by the length of the $n$-th word in that line, following these rules:

Line Index: The line number ($n$, starting from 0) is used as the index.

Word Index: The $n$-th word in the line is selected.

Digit Value:

If the length of the $n$-th word is greater than the line index ($n$), the digit is the word's length.

Otherwise (if the word's length is less than or equal to the line index, or if the word does not exist), the digit is '0'.

The function collects these digits for every line of every poem, compiling a list of secret codes.

Usage

The pin_extractor function accepts a single argument: a list of strings (poems).

Prerequisites

You only need a Python interpreter (Python 3.x recommended) to run the script.

Running the Code

Save the provided code as pin_extractor.py.

Execute the file from your terminal:

python pin_extractor.py


Example Input and Output

The provided script uses the following three example poems:

Input:

poems = [
    """Stars and the moon\nshine in the sky\nwhite and bright\nuntil the end of the night""",
    'The grass is green\nwhere and there\nhoping for rain\nbefore it turns yellow',
    'There\nonce\nwas\na\ndragon'
]


The script will output the list of extracted secret codes based on the decoding rules.

File Structure

The entire solution is contained in a single file:

pin_extractor.py: Contains the completed pin_extractor(poems) function and example usage.
