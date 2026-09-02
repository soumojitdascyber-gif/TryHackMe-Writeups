# 🔒 TryHackMe Writeup: Security Principles

## 📝 Room Overview
* **Room Name:** Security Principles
* **Platform:** TryHackMe
* **Difficulty:** Easy
* **Category:** Fundamentals / Defense

## 🎯 Objective
Learn the foundational security triad (CIA), its opposing threat model (DAD), common security models, and architectural design principles (ISO/IEC 19249) used to secure enterprise networks.

---

## 💡 Tasks & Answers

### Task: The CIA Triad
* **Question:** Click on "View Site" and answer the five questions. What is the flag that you obtained at the end?
* **Answer:** `THM{CIA_TRIAD}`

### Task: DAD (Disclosure, Alteration, and Destruction/Denial)
* **Question:** The attacker managed to gain access to customer records and dumped them online. What is this attack?
* **Answer:** `Disclosure`
* **Question:** A group of attackers were able to locate both the main and the backup power supply systems and switch them off. As a result, the whole network was shut down. What is this attack?
* **Answer:** `Destruction/Denial`

### Task: Fundamental Concepts of Security Models
* **Question:** Click on "View Site" and answer the four questions. What is the flag that you obtained at the end?
* **Answer:** `THM{SECURITY_MODELS}`

### Task: ISO/IEC 19249 (Design Principles)
* **Question:** Which principle are you applying when you turn off an insecure server that is not critical to the business?
* **Answer:** `2`
* **Question:** Your company hired a new sales representative. Which principle are they applying when they tell you to give them access only to the company products and prices?
* **Answer:** `1`
* **Question:** While reading the code of an ATM, you noticed a huge chunk of code to handle unexpected situations such as network disconnection and power failure. Which principle are they applying?
* **Answer:** `5`

---

## 🧠 Key Learnings
* **CIA vs. DAD:** CIA is the good side: Confidentiality (keeping secrets), Integrity (keeping data accurate), and Availability (keeping systems online). DAD is the evil twin: Disclosure (stealing secrets), Alteration (tampering with data), and Destruction/Denial (crashing systems).
* **Least Privilege (Principle 1):** Only give people the exact access they need to do their job, and nothing more. For example, a sales rep needs access to the product catalog, but they have zero business looking at the HR payroll system.
* **Attack Surface Reduction (Principle 2):** If you don't need a server or a feature, turn it off or remove it. A hacker cannot break into a door that no longer exists.
* **Failing Safely (Principle 5):** Things will break (power outages, internet drops). Systems must be built so that when they crash, they lock down safely instead of accidentally spitting out secret database code or customer information on the error screen.
*
