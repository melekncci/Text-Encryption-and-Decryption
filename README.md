# Frequency Analysis for Caesar Cipher Encryption

## Project Overview

This project focuses on analyzing the frequency of letters in an encrypted text to perform frequency analysis. The encrypted text is assumed to be encrypted using a Caesar cipher, where each letter in the original text is shifted by a fixed number of positions in the alphabet. For example, if the shift is 3, then 'A' would be encrypted as 'D', 'B' as 'E', and so on.

## Objective

The main objective of this project is to write a function that computes the number of occurrences of each letter of the alphabet in the encrypted text. This is useful in cryptanalysis to deduce the encryption key used for the Caesar cipher.

## Features

- **Count Frequency:** Computes and displays the number of occurrences of each letter in the encrypted text.
- **Supports All Letters:** Handles the entire English alphabet, from 'A' to 'Z'.
- **Case Insensitivity:** Treats all letters as uppercase for uniformity in analysis.

## How It Works

1. **Input Text:** Provide the encrypted text for analysis.
2. **Frequency Count:** The function will count the occurrences of each letter from 'A' to 'Z' in the encrypted text.
3. **Output:** The function outputs the frequency of each letter in a readable format.

## Example

Given an encrypted text, the function will output the frequency of each letter in a format similar to:

```
A occurs 29 times in the encrypted text
B occurs 15 times in the encrypted text
C occurs 18 times in the encrypted text
...
Z occurs 7 times in the encrypted text
```

## Installation

To use this project, ensure you have Python installed on your system. Clone the repository and run the script with the encrypted text as input.

```bash
git clone https://github.com/yourusername/frequency-analysis-caesar-cipher.git
cd frequency-analysis-caesar-cipher
```

## Usage

1. **Run the Script:**

   ```bash
   python frequency_analysis.py "Your encrypted text here"
   ```

2. **View Results:** The script will print the frequency count of each letter to the console.

## Code Example

Here is an example of how the function is implemented in Python:

```python
def count_letter_frequency(text):
    # Initialize a dictionary to hold letter counts
    letter_counts = {chr(i): 0 for i in range(65, 91)}
    
    # Count occurrences of each letter
    for char in text.upper():
        if char in letter_counts:
            letter_counts[char] += 1
    
    # Print the frequency of each letter
    for letter, count in letter_counts.items():
        print(f"{letter} occurs {count} times in the encrypted text")

# Example usage
encrypted_text = "Your encrypted text here"
count_letter_frequency(encrypted_text)
```

## Contributing

Contributions are welcome! If you have suggestions or improvements, please fork the repository and submit a pull request.

## References

- [Caesar Cipher](https://en.wikipedia.org/wiki/Caesar_cipher)
