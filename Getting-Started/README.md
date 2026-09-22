# ☁️ TryHackMe Writeup: Getting Started

## 📝 Room Overview
* **Room Name:** Getting Started
* **Platform:** TryHackMe
* **Difficulty:** Easy
* **Category:** Fundamentals / Web Hacking

## 🎯 Objective
Get started with TryHackMe by practically hacking a fake social media website. The goal is to discover a hidden administrator panel and exploit weak default credentials to gain unauthorized access to the application backend.

---

## 💡 Tasks & Answers

### Task: Let's Hack!
* **Question:** What is the name of the hidden admin page?
* **Answer:** `/test-admin`
* **Question:** What is the username and password in the form username:password?
* **Answer:** `admin:admin`
* **Question:** How many user are signed up to the application?
* **Answer:** `3`
---

## 🧠 Key Learnings
* **Security by Obscurity Fails:** The developers of this fake social media site tried to hide their admin panel by naming it `/test-admin` instead of putting a link to it. This is called "Security by Obscurity" (hiding the key under the doormat). Hackers use directory enumeration tools (like Gobuster or Dirb) to rapidly guess millions of folder names until they find these hidden pages.
* **The Danger of Default Credentials:** Finding the admin panel is only half the battle. The critical flaw here was that the administrators never changed the factory default password (`admin:admin`). In the real world, hackers maintain massive lists of default passwords for every router, webcam, and software platform imaginable. Always change default credentials immediately!
*
