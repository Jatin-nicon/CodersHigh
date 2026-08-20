# The question formed from "The Code Book" by Simon Singh

**Book Name:** The Code Book  
**Writer:** Simon Singh  
**Study Guide: Day 3 Programming Edition (Pages 16 to 20)**  

---

### Question 1: [Programming Challenge] Coding the Caesar Cipher (The Algorithm)

*   **The Scenario:** During his campaigns, Julius Caesar needed a reliable way to communicate instructions to his military commanders. He used a physical rotating disc mechanism (described in Figure 3 of *The Code Book*) to shift each letter of the message by a fixed rotation. This cipher is built on a simple modular math algorithm.
*   **The Programming Task:**
    1. Write a Python function `caesar_encrypt(plaintext: str, shift: int) -> str` that replicates Caesar's encryption method.
    2. Your function must handle both uppercase and lowercase letters, shifting them by the specified integer value while wrapping around the alphabet securely.
    3. Any non-alphabetic character (spaces, numbers, punctuation) must remain completely untouched in its original position.
    4. *Test Case:* What is the ciphertext of `caesar_encrypt("Keep the Nakama Safe", 3)`? Show your full Python implementation.

---

### Question 2: [Programming Challenge] Decrypting Caesar via Brute Force (Without the Key)

*   **The Scenario:** Suppose your scouts intercept an encrypted message. You know that it was sent by a Roman general using a standard Caesar shift, but you do not know the key shift they used. Since the total key space is tiny (exactly 25 useful shifts), you decide to write a cryptanalysis script to crack it.
*   **The Programming Task:**
    1. Write a Python function `caesar_brute_force_without_key(ciphertext: str) -> dict` that automatically performs a brute-force attack on any Caesar-encrypted string.
    2. The function must execute all 25 possible reverse-shifts *without* knowing or being provided the key beforehand, returning a dictionary mapping each possible shift key (1 to 25) to its corresponding decrypted string.
    3. Your algorithm must keep spaces, casing, and punctuation intact.
    4. *Test Case:* Input the ciphertext `"Wkh Qdndpd Phhwvdwgda"` into your function. Find the correct key and the plain English message. Show your full Python implementation.

---

### Question 3: [Programming Challenge] Implementing Kerckhoffs' Principle (Algorithm vs. Key)

*   **The Scenario:** Auguste Kerckhoffs stated a golden rule of modern cryptography: *\"The security of a cryptosystem must not depend on keeping secret the algorithm; it depends only on keeping secret the key.\"* To demonstrate this, you want to build a software system where the encryption code (the algorithm) is open and public, but the actual key is loaded dynamically from an external, hidden source.
*   **The Programming Task:**
    1. Create a Python class called `SecureCryptosystem` that implements a substitution algorithm.
    2. The class must *not* hardcode its shift or key map inside the algorithm. Instead, design a constructor `__init__(self, key_source: str)` that dynamically reads and loads the key from an external, hidden configuration file (e.g., a `.env` file or local text file) representing the "hidden key."
    3. Implement an open, public `encrypt(self, text: str) -> str` method within this class.
    4. Write a script to demonstrate that if an attacker copies your entire Python class (the algorithm), they still cannot decrypt any intercepted traffic unless they have access to the physical, external key configuration. Show your full code structure.

---

### Question 4: [Programming Challenge] Generating Keys of the Mind (Deterministic Monoalphabetic Cipher)

*   **The Scenario:** A general using a monoalphabetic substitution cipher faces a major vulnerability: writing down a randomized 26-letter substitution alphabet is a physical security risk, but memorizing a random sequence of letters is humanly impossible. To solve this, generals use a "keyword" in their minds to generate a consistent, scrambled substitution alphabet on the fly.
*   **The Programming Task:**
    1. Write a Python function `generate_cipher_alphabet(keyword: str) -> str` that takes a memorable keyword (e.g., `"NAKAMA"`), converts it to uppercase, removes duplicate letters, and places it at the start of the cipher alphabet. The function must then fill the remaining slots with the rest of the English alphabet in normal alphabetical order.
        *   *Example:* If the keyword is `"NAKAMA"`, the duplicate letters are removed to yield `"NAKM"`. The remaining letters of the alphabet (excluding N, A, K, M) are then appended, resulting in: `"NAKMBCDEFGHILOPQRSTUVWXYZ"`.
    2. Write a function `monoalphabetic_encrypt(plaintext: str, cipher_alphabet: str) -> str` that performs substitution using your generated alphabet.
    3. Write the corresponding `monoalphabetic_decrypt(ciphertext: str, cipher_alphabet: str) -> str` function.
    4. *Test Case:* If your keyword is `"ZENFINE"`, generate the cipher alphabet and encrypt the message `"Hardware and Artificial Intelligence"`. Show your full Python implementation.

---

### Question 5: [Programming Challenge] Simulating the Supercomputer Wall (Brute-Force Complexity)

*   **The Scenario:** While a simple shift cipher has only 25 keys, a general monoalphabetic substitution cipher has a key space of $26! \approx 4 \times 10^{26}$ (400 septillion) possible keys. An attacker claims they can build a supercomputer cluster to brute-force decryptions at a rate of 10 billion ($10^{10}$) keys per second. To prove why this brute-force approach is completely impossible against general substitution, you decide to write a time-complexity simulator.
*   **The Programming Task:**
    1. Write a Python function `simulate_brute_force_time(keys_per_second: float) -> None` that calculates and prints the maximum time required to test all possible keys for:
        *   A Caesar shift cipher (25 keys).
        *   A Monoalphabetic substitution cipher ($26!$ keys).
    2. Convert the outputs into human-readable time strings (e.g., seconds, hours, days, years, or multiples of the age of the universe, assuming the age of the universe is $1.38 \times 10^{10}$ years).
    3. As a sub-challenge, write a utility function `character_frequency_analysis(text: str) -> dict` that counts and returns the percentage frequency of each letter in an input ciphertext. Explain in comments how this frequency analysis function serves as a shortcut that breaks the 400 septillion limit in milliseconds. Show your full code implementation.

---

### Question 6: [Programming Challenge] The Fractional-Shift Cipher (The 18.5 Paradox)

*   **The Scenario:** To add a layer of complexity that resists standard Caesar shift decrypters, you decide to design a custom "Fractional Shift" algorithm. Since shifting a discrete alphabet character by a fraction is impossible, you approximate a shift of 18.5 by alternating the shift values across the message based on character positions.
*   **The Programming Task:**
    1. Write a Python function `fractional_shift_encrypt(plaintext: str) -> str` that implements the following rule:
        *   For alphabetic letters located at **odd 0-based indices** of the message string, apply a standard Caesar shift of **18**.
        *   For alphabetic letters located at **even 0-based indices** of the message string, apply a standard Caesar shift of **19**.
    2. Write the corresponding decryption function `fractional_shift_decrypt(ciphertext: str) -> str` to reverse the process.
    3. Both functions must preserve spaces, casing, and punctuation while correctly wrapping around the 26-letter alphabet.
    4. *Test Case:* Encrypt the string `"Meet the Tech Lead of SAC Tomorrow"` using your function, then decrypt it to verify it returns the original string. Show your complete code.
