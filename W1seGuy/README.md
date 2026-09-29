# 🕵️ TryHackMe Writeup: W1seGuy

## 📝 Room Overview
* **Room Name:** W1seGuy
* **Platform:** TryHackMe
* **Difficulty:** Easy / Medium
* **Category:** Cryptography / CTF

## 🎯 Objective
Solve the cryptography challenges involving XOR brute-forcing and known-plaintext attacks to retrieve the hidden flags.

---

## 💡 Tasks & Answers

### Task: Capture the Flags
* **Question:** What is the first flag?
* **Answer:** `THM{p1aIntExtAtt4ckcAnr3alLyhUrty0urx0r}`
* **Question:** What is the second and final flag?
* **Answer:** `THM{BrUt3_ForC1nG_XOR_cAn_B3_FuN_nO?}`

---

## 🧠 Key Learnings
* **XOR Cryptography:** XOR (Exclusive OR) is a bitwise operation used in encryption. If you have the ciphertext and a known part of the plaintext (like "THM{"), you can reverse-engineer the XOR key.
* **Plaintext Attacks:** The first flag explicitly mentions a plaintext attack (`p1aIntExtAtt4ck...`), which means using known pieces of the original message to break the encryption.
* **Brute-Forcing XOR:** The second flag (`BrUt3_ForC1nG_XOR...`) shows that if the key space is small enough, you can write a script to brute-force the XOR key and reveal the hidden message.
*
