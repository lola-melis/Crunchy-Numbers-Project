# Crunchy Sequence Project


## Overview

This project involves generating the first 50 terms of the Crunchy sequence, determining whether they are prime or composite, and showing that they are of the form \(2^n3^m\).

### Crunchy Sequence Definition:
As defined in the reference book, the Crunchy sequence starts with the numbers 1, 2, 3, and 4. Each successive number after 4 is the next number that is uniquely expressible as the product of two previous sequence terms.

## Functions Implemented

### `generate_crunchy_sequence(n)`
This function generates the first `n` numbers of the Crunchy sequence. It begins with an initial sequence of [1, 2, 3, 4] and continues adding terms until the sequence contains `n` numbers. 

- **Process**: 
  - A while loop runs until the sequence reaches length `n`.
  - It calls the helper function `is_unique_product(num, sequence)` to check if a given number `num` can be uniquely represented as the product of two previous sequence terms.
  - If true, `num` is added to the sequence, otherwise, the loop continues with the next number.

### `is_unique_product(num, sequence)`
This helper function determines whether the given number `num` can be expressed uniquely as the product of two terms from the current sequence.
- If more than one pair of terms can produce `num`, it returns `False`. 
- Otherwise, it returns `True` and the number is added to the sequence.

### `classify_numbers(sequence)`
This function takes the generated Crunchy sequence and classifies each number as prime or composite and verifies that each number is of the form \(2^n3^m\). 

- **Process**:
  - Each number in the sequence is divided by 2 and by 3. 
  - The number of times it can be divided by 2 is stored in `n`, and the number of times it can be divided by 3 is stored in `m`.
  - Additionally, the function checks if the number is prime or composite using the `is_prime()` function.

### `is_prime(num)`
This function checks whether a given number is prime, based on the method taught in class.

## Results

After generating the sequence, I demonstrated that each number is of the form \(2^n3^m\), and as expected, all numbers (except 2 and 3) were composite. The results from the `classify_numbers` function confirmed this, providing a list of each number along with its classification (prime/composite) and values of `n` and `m`.

## Conclusion

This project successfully generates the first 50 terms of the Crunchy sequence, classifies them as prime or composite, and shows that each term is of the form \(2^n3^m\).
