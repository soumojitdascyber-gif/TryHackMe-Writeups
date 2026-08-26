# 🎣 TryHackMe Writeup: Phishing Analysis Fundamentals

## 📝 Room Overview
* **Room Name:** Phishing Analysis Fundamentals
* **Platform:** TryHackMe
* **Difficulty:** Easy
* **Category:** Blue Team / Email Security

## 🎯 Objective
Learn all the components that make up an email and how to analyze email headers and sources to detect phishing attempts.

---

## 💡 Tasks & Answers

### Task: Analyzing Email Attachments & Decoding
* **Question 1:** What is the Content-Type of the attachment in the `email2.txt` file?
* **Answer:** `application/pdf`

* **Question 2:** What is the name of the attachment?
* **Answer:** `zmqpalgh.pdf`

* **Question 3:** Decode the base64 string. What is the hidden flag value?
* **Answer:** `THM{BENIGN_PDF_ATTACHMENT}`

---

## 🧠 Key Learnings
* Understood how to read raw email source code to identify attachments and their Content-Types.
* Learned how to extract and decode Base64 encoded payloads from email bodies to uncover hidden data.
*
