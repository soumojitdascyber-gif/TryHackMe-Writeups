# 💻 TryHackMe Writeup: Windows Command Line

## 📝 Room Overview
* **Room Name:** Windows Command Line
* **Platform:** TryHackMe
* **Difficulty:** Easy
* **Category:** Fundamentals / Command Line

## 🎯 Objective
Learn the essential Windows commands used for system navigation, network troubleshooting, file management, and process control using the default Windows Command Prompt (`cmd.exe`).

---

## 💡 Tasks & Answers

### Task: Basic System Information
* **Question:** What is the default command line interpreter in the Windows environment?
* **Answer:** `cmd.exe`
* **Question:** What is the OS version of the Windows VM?
* **Answer:** `10.0.20348.2655`
* **Question:** What is the hostname of the Windows VM?
* **Answer:** `WINSRV2022-CORE`

### Task: Network Troubleshooting
* **Question:** Which command can we use to look up the server's physical address (MAC address)?
* **Answer:** `ipconfig /all`
* **Question:** What is the name of the service listening on port 135?
* **Answer:** `RpcSs`
* **Question:** What is the name of the service listening on port 3389?
* **Answer:** `TermService`

### Task: File Management
* **Question:** What are the file’s contents in C:\Treasure\Hunt?
* **Answer:** `THM{CLI_POWER}`

### Task: Task and Process Management
* **Question:** What command would you use to find the running processes related to notepad.exe?
* **Answer:** `tasklist /FI "imagename eq notepad.exe"`
* **Question:** What command can you use to kill the process with PID 1516?
* **Answer:** `taskkill /PID 1516`

### Task: System Control
* **Question:** The command `shutdown /s` can shut down a system. What is the command you can use to restart a system?
* **Answer:** `shutdown /r`
* **Question:** What command can you use to abort a scheduled system shutdown?
* **Answer:** `shutdown /a`

---

## 🧠 Key Learnings
* **The CLI (Command Line Interface):** `cmd.exe` is the original Windows terminal. Think of it as a way to talk directly to the computer's brain without using a mouse or clicking on icons.
* **Network Recon (`ipconfig` & `netstat`):** 
  * `ipconfig /all` is like asking the computer to show its full network ID card (including its physical MAC address). 
  * `netstat` shows you all the open "doors" (ports) on the computer and who is listening behind them (e.g., `TermService` listening on port 3389 for Remote Desktop connections).
* **Process Management (`tasklist` & `taskkill`):** This is the text-based version of the Windows Task Manager. If a program (like notepad or a malicious virus) is running, it gets a unique ID number called a PID (Process ID). You can use `tasklist` to find it, and `taskkill` to forcefully snipe and close it.
* **System Control:** Commands like `shutdown /r` (restart) or `shutdown /a` (abort) are extremely useful when you have remote access to a server and need to reboot it to apply an update or stop an attacker from turning it off.
*
