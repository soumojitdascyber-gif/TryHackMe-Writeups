# 🔐 TryHackMe Writeup: Cryptography for Dummies

## 📝 Room Overview
* **Room Name:** Cryptography for Dummies
* **Platform:** TryHackMe
* **Difficulty:** Easy
* **Category:** Fundamentals / Cryptography

## 🎯 Objective
Become familiar with the core principles of cryptograph. Learn the differences between symmetric and asymmetric encryption, understand message digests (Hashes), and differentiate between encrypting data and simply encoding it (Base64).

---

## 💡 Tasks & Answers

### Task: Symmetric vs Asymmetric Cryptography
* **Question:** What type of cryptography is more secure?
* **Answer:** `asymmetric`
* **Question:** What type of cryptography is faster?
* **Answer:** `symmetric`
* **Question:** What type of cryptography will a Bank site use?
* **Answer:** `asymmetric`
* **Question:** What will you use to encrypt your messages in asymmetric cryptography?
* **Answer:** `public key`
* **Question:** What will you use to decrypt messages in asymmetric cryptography?
* **Answer:** `private key`
* **Question:** Does symmetric cryptography use two different keys for encryption/decryption? (aye/nay)
* **Answer:** `nay`

### Task: Hashes
* **Question:** What's the MD5 hash of "hashes are cool"?
* **Answer:** `f762d32e3c160900d94b683e927555b9`
* **Question:** What does MD5 stand for?
* **Answer:** `Message Digest 5`
* **Question:** Who created MD5?
* **Answer:** `Ronald Rivest`
### Task: Encoding vs Encryption
* **Question:** Encode the string "cryptographyisuseful" with Base64
* **Answer:** `Y3J5cHRvZ3JhcGh5aXN1c2VmdWw=`
* **Question:** Decode the string "d2F0ZXJtZWxvbg==". What's the secret word?
* **Answer:** `watermelon`

---

## 🧠 Key Learnings
* **Symmetric vs Asymmetric:** 
  * *Symmetric* uses the same key to lock and unlock the data. It's fast, but securely sharing that one key is dangerous.
  * *Asymmetric* uses a Public Key to lock the data and a separate Private Key to unlock it. It's highly secure and is what banks use, but it's much slower.
* **Hashing (One-Way Trip):** Hashes (like MD5) are not encryption; they are digital fingerprints. You can turn "hashes are cool" into `f762d3...`, but you cannot mathematically reverse it. They are used to verify file integrity and store passwords safely.
* **Encoding is NOT Encryption:** Base64 encoding (e.g., turning "watermelon" into `d2F0ZXJtZWxvbg==`) does not use keys. It simply translates data into a different format so it can be safely sent over systems that might break special characters. Anyone can decode it instantly.
*
