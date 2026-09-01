# 🪟 TryHackMe Writeup: Windows Fundamentals 1

## 📝 Room Overview
* **Room Name:** Windows Fundamentals 1
* **Platform:** TryHackMe
* **Difficulty:** Easy
* **Category:** Fundamentals / Operating Systems

## 🎯 Objective
Learn the core components of the Windows operating system, including desktop navigation, the NTFS file system, user account management, and built-in security controls.

---

## 💡 Tasks & Answers

### Task: The Desktop (GUI) & Taskbar
* **Question:** What encryption can you enable on Pro that you can't enable in Home?
* **Answer:** `BitLocker`
* **Question:** Which selection will hide/disable the Search box?
* **Answer:** `Hidden`
* **Question:** Which selection will hide/disable the Task View button?
* **Answer:** `Show Task View button`
* **Question:** Besides Clock and Network, what other icon is visible in the Notification Area?
* **Answer:** `Action Center`

### Task: The Windows File System
* **Question:** What is the meaning of NTFS?
* **Answer:** `New Technology File System`

### Task: User Accounts & Management
* **Question:** What is the name of the other user account?
* **Answer:** `tryhackmebilly`
* **Question:** What groups is this user a member of?
* **Answer:** `Remote Desktop Users,Users`
* **Question:** What built-in account is for guest access to the computer?
* **Answer:** `Guest`
* **Question:** What is the account description?
* **Answer:** `window$Fun1!`

### Task: Settings, Control Panel & Task Manager
* **Question:** What does UAC mean?
* **Answer:** `User Account Control`
* **Question:** In the Control Panel, change the view to Small icons. What is the last setting in the Control Panel view?
* **Answer:** `Windows Defender Firewall`
* **Question:** What is the keyboard shortcut to open Task Manager?
* **Answer:** `Ctrl+Shift+Esc`

---

## 🧠 Key Learnings
* **BitLocker:** This is a built-in Windows tool that scrambles (encrypts) your entire hard drive. If someone steals your laptop, they can't read your files without the password.
* **NTFS:** This stands for New Technology File System. Think of it as the master rulebook Windows uses to organize, store, and find every single file on your hard drive. 
* **UAC (User Account Control):** This is the security warning pop-up that asks, "Do you want to allow this app to make changes to your device?" It acts as a guard to stop viruses from secretly installing themselves without your permission.
* **User Groups:** Windows lets you put users into different "groups" (like regular 'Users' or 'Remote Desktop Users'). This makes it easy for administrators to control exactly what a person is allowed to do or see on the computer.
*
