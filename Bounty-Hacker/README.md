# 🤠 TryHackMe Writeup: Bounty Hacker

## 📝 Room Overview
* **Room Name:** Bounty Hacker
* **Platform:** TryHackMe
* **Difficulty:** Easy
* **Category:** Offensive Security / Capture The Flag (CTF)

## 🎯 Objective
Prove your status as an Elite Bounty Hacker by compromising a target machine. This involves network enumeration, exploiting anonymous FTP access to gather intelligence (usernames and wordlists), brute-forcing SSH credentials, and escalating privileges to root.

---

## 💡 Tasks & Answers

### Task: Compromise the Machine
* **Question:** Who wrote the task list?
* **Answer:** `lin`
* **Question:** What service can you bruteforce with the text file found?
* **Answer:** `SSH`
* **Question:** What is the users password?
* **Answer:** `RedDr4gonSynd1cat3`
* **Question:** user.txt
* **Answer:** `THM{CR1M3_SyNd1C4T3}`
* **Question:** root.txt
* **Answer:** `THM{B0UNTY_H4cK3r}`

---

## 🧠 Key Learnings: The Attack Chain Explained

1. **Reconnaissance (Nmap):** 
   Every hack starts with finding the open doors. You run `nmap` to scan the machine. You discover that ports 21 (FTP), 22 (SSH), and 80 (HTTP) are open. 

2. **Enumeration (FTP Anonymous Login):** 
   You notice FTP (File Transfer Protocol) is open. A common misconfiguration is leaving "Anonymous" login enabled, meaning anyone can log in without a password. By connecting to the FTP server (`ftp <Target_IP>`) and logging in with the username `anonymous`, you find two files: a task list and a text file containing potential passwords. Reading the task list reveals a username: `lin`.

3. **Weaponization & Exploitation (Hydra):** 
   Now you have a valid username (`lin`) and a custom dictionary list of passwords from the FTP server. Since port 22 (SSH) is open, you can use **Hydra** to automatically test every password in that text file against the SSH service until you find the correct one (`RedDr4gonSynd1cat3`). 

4. **Privilege Escalation:** 
   Once logged in via SSH as the user `lin`, you get the `user.txt` flag. However, you are just a standard user. You need to become 'root' (the superadmin). By checking what commands `lin` can run with superuser permissions (using `sudo -l`), you likely found a binary (like `tar` or `less`) that can be exploited to spawn a root shell, allowing you to capture the final `root.txt` flag.
