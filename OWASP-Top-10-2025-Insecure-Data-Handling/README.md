# 🌐 TryHackMe Writeup: OWASP Top 10 2025 - Insecure Data Handling

## 📝 Room Overview
* **Room Name:** OWASP Top 10 2025: Insecure Data Handling
* **Platform:** TryHackMe
* **Difficulty:** Easy
* **Category:** Web Security / AppSec

## 🎯 Objective
Learn about A04, A05, and A08 as they relate to insecure data handling, covering injection flaws, software data integrity, and cryptographic failures.

---

## 💡 Tasks & Answers

### Task 3: A05 Injection
* **Question:** Decrypt the encrypted notes. One of them will contain a flag value. What is it?
* **Answer:** `THM{WEAK_CRYPTO_FLAG}`

### Task 4: A08 Software or Data Integrity Failures
* **Question 1:** Perform an SSTI attack on the practical. You need to read the contents of flag.txt that is located within the same directory as the web application.
* **Answer:** `THM{SSTI_FLAG_OBTAINED}`

* **Question 2:** Use Python to pickle a malicious, serialised payload that reads the contents of flag.txt. What are the contents of flag.txt?
* **Answer:** `THM{INSECURE_DESERIALIZATION}`

---

## 🧠 Key Learnings
* Understood how Cryptographic Failures lead to sensitive data exposure.
* Practically exploited Server Side Template Injection (SSTI) to read system files.
* Learned the dangers of insecure deserialization by crafting malicious pickled payloads in Python.
*
