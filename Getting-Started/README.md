# ☁️ TryHackMe Writeup: Getting Started

## 📝 Room Overview
* **Room Name:** Getting Started
* **Platform:** TryHackMe
* **Difficulty:** Easy
* **Category:** Fundamentals / Web Hacking

## 🎯 Objective
Get started with TryHackMe by practically hacking a fake social media website[span_0](start_span)[span_0](end_span). The goal is to discover a hidden administrator panel and exploit weak default credentials to gain unauthorized access to the application backend.

---

## 💡 Tasks & Answers

### Task: Let's Hack!
* **Question:** What is the name of the hidden admin page?
* **Answer:** `/test-admin`[span_1](start_span)[span_1](end_span)
* **Question:** What is the username and password in the form username:password?
* **Answer:** `admin:admin`[span_2](start_span)[span_2](end_span)
* **Question:** How many user are signed up to the application?
* **Answer:** `3`[span_3](start_span)[span_3](end_span)

---

## 🧠 Key Learnings
* **Security by Obscurity Fails:** The developers of this fake social media site tried to hide their admin panel by naming it `/test-admin` instead of putting a link to it[span_4](start_span)[span_4](end_span). This is called "Security by Obscurity" (hiding the key under the doormat). Hackers use directory enumeration tools (like Gobuster or Dirb) to rapidly guess millions of folder names until they find these hidden pages.
* **The Danger of Default Credentials:** Finding the admin panel is only half the battle. The critical flaw here was that the administrators never changed the factory default password (`admin:admin`)[span_5](start_span)[span_5](end_span). In the real world, hackers maintain massive lists of default passwords for every router, webcam, and software platform imaginable. Always change default credentials immediately!
*
