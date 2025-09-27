## Question 2: Case Conversion FST

This Finite State Transducer (FST) converts an input string of lowercase letters to uppercase.

### Files in this Directory

* **`symbols.txt`**: Defines the input (a-z) and output (A-Z) symbols.
* **`case_converter.txt`**: The text definition of the FST.
* **`case_converter.fst`**: The compiled binary FST.
* **`case_converter.png`**: A visual diagram of the FST.
* **`input.txt`**: A sample input file for the string "hello".

### How to Run

To test this FST, run the following commands from within this directory:

1.  **Compile the FST:**
    ```bash
    fstcompile --isymbols=symbols.txt --osymbols=symbols.txt case_converter.txt case_converter.fst
    ```

2.  **Compile the input and run the test:**
    ```bash
    fstcompile --isymbols=symbols.txt --osymbols=symbols.txt input.txt input.fst
    fstcompose input.fst case_converter.fst result.fst
    fstprint --isymbols=symbols.txt --osymbols=symbols.txt result.fst
    ```