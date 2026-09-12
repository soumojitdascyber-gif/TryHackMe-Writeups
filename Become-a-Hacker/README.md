# 💻 TryHackMe Writeup: Become a Hacker

## 📝 Room Overview
* **Room Name:** Become a Hacker
* **Platform:** TryHackMe
* **Difficulty:** Easy
* **Category:** Fundamentals / Offensive Security

## 🎯 Objective
Understand the core concept of Offensive Security and get a hands-on introduction to the hacking methodology: discovering hidden web directories and brute-forcing login portals to gain unauthorized access.

---

## 💡 Tasks & Answers

### Task: What is Offensive Security?
* **Question:** Which of the following options better represents the process where you simulate a hacker's actions to find vulnerabilities in a system?
* **Answer:** `Offensive Security`

### Task: Let's Hack - Part 2 of 2
* **Question:** What is the name of the hidden web page you discovered?
* **Answer:** `login`
* **Question:** What is the secret message that you have discovered?
* **Answer:** `born_to_be_a_hacker`

---

## 🧠 Key Learnings
* **Offensive Security vs. Defensive Security:** 
  * *Defensive Security (Blue Team)* is like putting locks on your doors and installing security cameras to catch burglars.
  * *Offensive Security (Red Team)* is hiring a professional to actively try and break into your house using a crowbar, just to prove that your locks are actually weak *before* a real burglar arrives.
* **Hidden Directories:** Developers often create secret pages (like `/login`, `/admin`, or `/backup`) but don't put any visible links to them on the main website. Hackers use automated tools to rapidly guess thousands of folder names until they find these hidden doors.
* **Brute-Forcing (Hydra):** Once a hidden login page is discovered, attackers don't just guess passwords manually. They use powerful tools like **Hydra** to fire thousands of common usernames and passwords at the login form every second until the lock breaks and grants them access.
*
