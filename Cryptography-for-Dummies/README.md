# 🔐 TryHackMe Writeup: Cryptography for Dummies

## 📝 Room Overview
* **Room Name:** Cryptography for Dummies
* **Platform:** TryHackMe
* **Difficulty:** Easy
* **Category:** Fundamentals / Cryptography

## 🎯 Objective
Become familiar with the core principles of cryptography[span_13](start_span)[span_13](end_span). Learn the differences between symmetric and asymmetric encryption, understand message digests (Hashes), and differentiate between encrypting data and simply encoding it (Base64).

---

## 💡 Tasks & Answers

### Task: Symmetric vs Asymmetric Cryptography
* **Question:** What type of cryptography is more secure?
* **Answer:** `asymmetric`[span_14](start_span)[span_14](end_span)
* **Question:** What type of cryptography is faster?
* **Answer:** `symmetric`[span_15](start_span)[span_15](end_span)
* **Question:** What type of cryptography will a Bank site use?
* **Answer:** `asymmetric`[span_16](start_span)[span_16](end_span)
* **Question:** What will you use to encrypt your messages in asymmetric cryptography?
* **Answer:** `public key`[span_17](start_span)[span_17](end_span)
* **Question:** What will you use to decrypt messages in asymmetric cryptography?
* **Answer:** `private key`[span_18](start_span)[span_18](end_span)
* **Question:** Does symmetric cryptography use two different keys for encryption/decryption? (aye/nay)
* **Answer:** `nay`[span_19](start_span)[span_19](end_span)

### Task: Hashes
* **Question:** What's the MD5 hash of "hashes are cool"?
* **Answer:** `f762d32e3c160900d94b683e927555b9`[span_20](start_span)[span_20](end_span)
* **Question:** What does MD5 stand for?
* **Answer:** `Message Digest 5`[span_21](start_span)[span_21](end_span)
* **Question:** Who created MD5?
* **Answer:** `Ronald Rivest`[span_22](start_span)[span_22](end_span)

### Task: Encoding vs Encryption
* **Question:** Encode the string "cryptographyisuseful" with Base64
* **Answer:** `Y3J5cHRvZ3JhcGh5aXN1c2VmdWw=`[span_23](start_span)[span_23](end_span)
* **Question:** Decode the string "d2F0ZXJtZWxvbg==". What's the secret word?
* **Answer:** `watermelon`[span_24](start_span)[span_24](end_span)

---

## 🧠 Key Learnings
* **Symmetric vs Asymmetric:** 
  * *Symmetric* uses the same key to lock and unlock the data. It's fast, but securely sharing that one key is dangerous[span_25](start_span)[span_25](end_span).
  * *Asymmetric* uses a Public Key to lock the data and a separate Private Key to unlock it. It's highly secure and is what banks use, but it's much slower[span_26](start_span)[span_26](end_span).
* **Hashing (One-Way Trip):** Hashes (like MD5) are not encryption; they are digital fingerprints. You can turn "hashes are cool" into `f762d3...`[span_27](start_span)[span_27](end_span), but you cannot mathematically reverse it. They are used to verify file integrity and store passwords safely.
* **Encoding is NOT Encryption:** Base64 encoding (e.g., turning "watermelon" into `d2F0ZXJtZWxvbg==`) does not use keys[span_28](start_span)[span_28](end_span). It simply translates data into a different format so it can be safely sent over systems that might break special characters. Anyone can decode it instantly.
*
