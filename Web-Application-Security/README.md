# 🌐 TryHackMe Writeup: Web Application Security

## 📝 Room Overview
* **Room Name:** Web Application Security
* **Platform:** TryHackMe
* **Difficulty:** Easy
* **Category:** Web Security / AppSec

## 🎯 Objective
Learn the fundamentals of web applications and practically explore common top-tier security vulnerabilities like Authentication Failures, Cryptographic Failures, and IDOR.

---

## 💡 Tasks & Answers

### Task: Web Application Security Risks
* **Question:** What do you need to access a web application?
* **Answer:** `Browser`

### Task: Practical Example of Web Application Security
* **Question:** You discovered that the login page allows an unlimited number of login attempts without trying to slow down the user or lock the account. What is the category of this security risk?
* **Answer:** `Identification and Authentication Failure`
* **Question:** You noticed that the username and password are sent in cleartext without encryption. What is the category of this security risk?
* **Answer:** `Cryptographic Failures`

### Task: IDOR (Insecure Direct Object Reference)
* **Question:** Check the other users to discover which user account was used to make the malicious changes and revert them. After reverting the changes, what is the flag that you have received?
* **Answer:** `THM{IDOR_EXPLORED}`

---

## 🧠 Key Learnings
* **Authentication Failure:** If a website lets you guess a password a million times without locking your account, a hacker can just use an automated robot tool to keep guessing passwords until it gets the right one.
* **Cryptographic Failure (Cleartext):** When you log in, if the website doesn't scramble (encrypt) your password, it gets sent across the internet as plain text. Anyone spying on the Wi-Fi network can read your password exactly as you typed it, just like reading a postcard.
* **IDOR (Insecure Direct Object Reference):** Imagine you are looking at your profile picture and the website link says `website.com/user=5`. If you change that `5` to a `6` and suddenly see another person's private details, that is an IDOR vulnerability. The website blindly trusted the number and forgot to check if you were actually authorized to look at user 6's data.
*
