# 🐧 TryHackMe Writeup: Linux CLI - Shells Bells

## 📝 Room Overview
* **Room Name:** Linux CLI - Shells Bells
* **Platform:** TryHackMe
* **Difficulty:** Easy
* **Category:** Fundamentals / Linux

## 🎯 Objective
Explore the Linux command-line interface to solve system mysteries. Learn essential commands for directory navigation, log filtering, and escalating privileges to the root user.

---

## 💡 Tasks & Answers

### Task: Linux Investigation
* **Question:** Which CLI command would you use to list a directory?
* **Answer:** `ls`
* **Question:** Which command helped you filter the logs for failed logins?
* **Answer:** `grep`
* **Question:** Which command would you run to switch to the root user?
* **Answer:** `sudo su`
* **Question:** Finally, what flag did Sir Carrotbane leave in the root bash history?
* **Answer:** `THM{until-we-meet-again}`

---

## 🧠 Key Learnings
* **Filtering Noise with `grep`:** In a real-world scenario, log files can contain millions of lines. You can't read them manually. `grep` acts like a powerful search engine for the terminal, instantly filtering out everything except the specific keywords (like "failed logins") you are looking for.
* **Privilege Escalation (`sudo su`):** In Linux, normal users have restricted permissions. The "root" user is the absolute administrator who can change or destroy anything. Attackers always aim to escalate their privileges to root (`sudo su`) to gain total control over the compromised machine.
*
