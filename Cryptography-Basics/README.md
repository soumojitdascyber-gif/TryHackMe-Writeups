# 🔐 TryHackMe Writeup: Cryptography Basics

## 📝 Room Overview
* **Room Name:** Cryptography Basics
* **Platform:** TryHackMe
* **Difficulty:** Easy
* **Category:** Fundamentals / Cryptography

## 🎯 Objective
Learn the core principles of cryptography, including the difference between plaintext and ciphertext, historical ciphers, basic cryptographic mathematics (Modulo, XOR), and modern symmetric encryption standards (AES vs. DES).

---

## 💡 Tasks & Answers

### Task: Why Cryptography? & Compliance
* **Question:** What is the standard required for handling credit card information?
* **Answer:** `PCI DSS`

### Task: Plaintext to Ciphertext
* **Question:** What do you call the encrypted plaintext?
* **Answer:** `ciphertext`
* **Question:** What do you call the process that returns the plaintext?
* **Answer:** `decryption`

### Task: Historical Ciphers
* **Question:** Knowing that XRPCTCRGNEI was encrypted using Caesar Cipher, what is the original plaintext?
* **Answer:** `ICANENCRYPT`

### Task: Types of Encryption (Symmetric)
* **Question:** Should you trust DES? (Yea/Nay)
* **Answer:** `Nay`
* **Question:** When was AES adopted as an encryption standard?
* **Answer:** `2001`

### Task: Basic Cryptographic Math (Modulo & XOR)
* **Question:** What's 1001 ⊕ 1010?
* **Answer:** `0011`
* **Question:** What's 118613842%9091?
* **Answer:** `3565`
* **Question:** What's 60%12?
* **Answer:** `0`

---

## 🧠 Key Learnings
* **Plaintext vs. Ciphertext:** "Plaintext" is normal, readable data (like a regular text message). "Ciphertext" is the scrambled, unreadable secret code. "Decryption" is the process of translating that secret code back into normal text using a key.
* **Caesar Cipher:** An ancient, basic encryption method where you simply shift the alphabet by a certain number of spaces (e.g., shifting 'A' by 3 becomes 'D'). It is fun but totally insecure today.
* **DES vs. AES:** Think of DES (Data Encryption Standard) as a rusty old padlock; computers are so fast now that they can break it in hours. You should never trust it. AES (Advanced Encryption Standard), adopted in 2001, is the modern, heavy-duty bank vault used globally today.
* **Cryptographic Math (Modulo & XOR):** 
  * **Modulo (%)** is simply "clock math." It's just asking for the *remainder* of a division. (e.g., 60 divided by 12 is exactly 5 with 0 remainder, so 60%12 = 0).
  * **XOR (⊕)** is a binary logic switch used to scramble data. If the bits are the same (1 and 1, or 0 and 0), the result is 0. If they are different (1 and 0), the result is 1. (e.g., 1001 ⊕ 1010 = 0011).
* **PCI DSS:** If a company touches credit card data, they must follow strict legal rules (Payment Card Industry Data Security Standard). Cryptography is legally required here to protect customer money.
*
