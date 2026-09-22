# 🎣 TryHackMe Writeup: Phishing: HiddenEye

## 📝 Room Overview
* **Room Name:** Phishing: HiddenEye
* **Platform:** TryHackMe
* **Difficulty:** Easy
* **Category:** Offensive Security / Social Engineering

## 🎯 Objective
Learn how to use HiddenEye, a tool designed to create convincing phishing pages for platforms like Gmail, Snapchat, and PayPal. Understand the difference between legitimate and fake websites, and explore the core concepts of social engineering.

---

## 💡 Tasks & Answers

### Task: Installation & Creating your first phishing page!
* **Question:** Which image shows a legit web-page? They are identical and most phishing pages nowadays have HTTPS enabled. (Image 1 or Image 2)
* **Answer:** `Image 2`
* **Question:** What will you use this tool for?
* **Answer:** `Educational Purposes`
* **Question:** What is the weakest link in cyber-security?
* **Answer:** `Humans`
* **Question:** Do most phishing pages have HTTPS (Yay/Nay)?
* **Answer:** `Yay`
---

## 🧠 Key Learnings
* **The Weakest Link:** You can spend millions of dollars on advanced firewalls, intrusion detection systems, and encryption. However, if a hacker sends a fake login email to an employee and that human employee types their password into the fake site, all that expensive security is bypassed instantly. This is why humans are universally considered the weakest link in cybersecurity.
* **The HTTPS Myth:** Many people are taught to "look for the padlock" in their browser, assuming HTTPS means a website is safe. This is incredibly dangerous. HTTPS *only* means the connection between you and the server is encrypted. Anyone, including a hacker, can get an SSL certificate for free. Today, most modern phishing pages use HTTPS to trick victims into feeling safe.
* **Automated Phishing Tools:** Tools like HiddenEye automate the process of cloning the exact HTML/CSS of legitimate login portals (like Gmail) and setting up a local server to harvest the credentials entered by the victim. 
*
