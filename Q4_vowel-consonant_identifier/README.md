## Question 4: Vowel-Consonant Identifier

This FST identifies characters in an input string, mapping vowels to the output symbol 'v' and consonants to 'c'.

### Files in this Directory

* **`symbols.txt`**: Defines the input (a-z, A-Z) and output (v, c) symbols.
* **`vowel_consonant.txt`**: The text definition of the FST.
* **`vowel_consonant.fst`**: The compiled binary FST.
* **`input.txt`**: A sample input file for the string "Automata".

### How to Run

To test this FST, run the following commands from within this directory:

1.  **Compile the FST:**
    ```bash
    fstcompile --isymbols=symbols.txt --osymbols=symbols.txt vowel_consonant.txt vowel_consonant.fst
    ```

2.  **Compile the input and run the test:**
    ```bash
    fstcompile --isymbols=symbols.txt --osymbols=symbols.txt input.txt input.fst
    fstcompose input.fst vowel_consonant.fst result.fst
    fstprint --isymbols=symbols.txt --osymbols=symbols.txt result.fst
    ```