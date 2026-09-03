# 📡 TryHackMe Writeup: Active Reconnaissance

## 📝 Room Overview
* **Room Name:** Active Reconnaissance
* **Platform:** TryHackMe
* **Difficulty:** Easy
* **Category:** Threat Intelligence / Reconnaissance

## 🎯 Objective
Learn how to actively interact with target systems using standard command-line tools (Ping, Traceroute, Telnet, Netcat) and web browsers to map infrastructure and identify running services.

---

## 💡 Tasks & Answers

### Task: Web Browser & Developer Tools
* **Question:** Browse to the following website... Using the Developer Tools, figure out the total number of questions.
* **Answer:** `8`

### Task: Ping
* **Question:** Which option would you use to set the size of the data carried by the ICMP echo request?
* **Answer:** `-s`
* **Question:** What is the size of the ICMP header in bytes?
* **Answer:** `8`
* **Question:** Does MS Windows Firewall block ping by default? (Y/N)
* **Answer:** `Y`
* **Question:** Deploy the VM... issue the command `ping -c 10 MACHINE_IP`. How many ping replies did you get back?
* **Answer:** `10`

### Task: Traceroute
* **Question:** In Traceroute A, what is the IP address of the last router/hop before reaching tryhackme.com?
* **Answer:** `172.67.69.208`
* **Question:** In Traceroute B, what is the IP address of the last router/hop before reaching tryhackme.com?
* **Answer:** `104.26.11.229`
* **Question:** In Traceroute B, how many routers are between the two systems?
* **Answer:** `25`

### Task: Telnet
* **Question:** Start the attached VM... use the telnet client to connect to the VM on port 80. What is the name of the running server?
* **Answer:** `Apache`
* **Question:** What is the version of the running server (on port 80 of the VM)?
* **Answer:** `2.4.61`

### Task: Netcat
* **Question:** Start the VM... use Netcat to connect to the VM port 21. What is the version of the running server?
* **Answer:** `0.17`

---

## 🧠 Key Learnings
* **Active vs Passive:** Active recon means your computer is directly communicating with the target's computer. You leave digital footprints, and their security systems (like firewalls) will see you.
* **Ping:** Think of `ping` like knocking on a door to see if someone is home. If they reply, you know the server is online. Note: Windows computers usually ignore this knock by default to hide themselves from hackers.
* **Traceroute:** When you send data across the internet, it doesn't go in a straight line; it jumps through many different routers. `traceroute` maps out every single jump (hop) your data takes to reach the target.
* **Banner Grabbing (Telnet/Netcat):** Imagine calling a company and their answering machine says, "Welcome to Apache Server Version 2.4". That message is called a "banner". Tools like Telnet and Netcat let you connect to a server just to read these banners, telling you exactly what software and version the target is running so you know how to exploit it.
*
