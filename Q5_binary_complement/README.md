## Question 5: Binary Complement

This FST calculates the binary complement of an input string, flipping 0s to 1s and 1s to 0s.

### Files in this Directory

* **`symbols.txt`**: Defines the binary symbols (0, 1).
* **`binary_complement.txt`**: The text definition of the FST.
* **`binary_complement.fst`**: The compiled binary FST.
* **`input.txt`**: A sample input file for the string "10110".

### How to Run

To test this FST, run the following commands from within this directory:

1.  **Compile the FST:**
    ```bash
    fstcompile --isymbols=symbols.txt --osymbols=symbols.txt binary_complement.txt binary_complement.fst
    ```

2.  **Compile the input and run the test:**
    ```bash
    fstcompile --isymbols=symbols.txt --osymbols=symbols.txt input.txt input.fst
    fstcompose input.fst binary_complement.fst result.fst
    fstprint --isymbols=symbols.txt --osymbols=symbols.txt result.fst
    ```