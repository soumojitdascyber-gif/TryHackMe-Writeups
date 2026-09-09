# 📡 TryHackMe Writeup: Nmap

## 📝 Room Overview
* **Room Name:** Nmap (Further Nmap)
* **Platform:** TryHackMe
* **Difficulty:** Easy
* **Category:** Offensive Security / Reconnaissance

## 🎯 Objective
Take an in-depth look at Nmap to master port scanning techniques (TCP Connect, SYN, UDP), utilize the Nmap Scripting Engine (NSE) for vulnerability detection, and explore advanced scan types and flags for firewall evasion.

---

## 💡 Tasks & Answers

### Task: Introduction & Nmap Switches
* **Question:** What networking constructs are used to direct traffic to the right application on a server?
* **Answer:** `Ports`
* **Question:** How many of these are available on any network-enabled computer?
* **Answer:** `65535`
* **Question:** [Research] How many of these are considered "well-known"?
* **Answer:** `1024`

### Task: Basic Scan Types & Output Switches
* **Question:** What is the first switch listed in the help menu for a 'Syn Scan'?
* **Answer:** `-sS`
* **Question:** Which switch would you use for a "UDP scan"?
* **Answer:** `-sU`
* **Question:** If you wanted to detect which operating system the target is running on, which switch would you use?
* **Answer:** `-O`
* **Question:** Nmap provides a switch to detect the version of the services running on the target. What is this switch?
* **Answer:** `-sV`
* **Question:** The default output provided by nmap often does not provide enough information for a pentester. How would you increase the verbosity?
* **Answer:** `-v`
* **Question:** Verbosity level one is good, but verbosity level two is better! How would you set the verbosity level to two?
* **Answer:** `-vv`
* **Question:** What switch would you use to save the nmap results in three major formats?
* **Answer:** `-oA`
* **Question:** What switch would you use to save the nmap results in a "normal" format?
* **Answer:** `-oN`
* **Question:** A very useful output format: how would you save results in a "grepable" format?
* **Answer:** `-oG`
* **Question:** Sometimes the results we're getting just aren't enough. If we don't care about how loud we are, we can enable "aggressive" mode. How would you activate this setting?
* **Answer:** `-A`
* **Question:** How would you set the timing template to level 5?
* **Answer:** `-T5`
* **Question:** How would you tell nmap to only scan port 80?
* **Answer:** `-p 80`
* **Question:** How would you tell nmap to scan ports 1000-1500?
* **Answer:** `-p 1000-1500`
* **Question:** A very useful option that should not be ignored: How would you tell nmap to scan all ports?
* **Answer:** `-p-`

### Task: Nmap Scripting Engine (NSE)
* **Question:** How would you activate a script from the nmap scripting library?
* **Answer:** `--script`
* **Question:** How would you activate all of the scripts in the "vuln" category?
* **Answer:** `--script=vuln`
* **Question:** What language are NSE scripts written in?
* **Answer:** `Lua`
* **Question:** Which category of scripts would be a very bad idea to run in a production environment?
* **Answer:** `intrusive`
* **Question:** What optional argument can the `ftp-anon.nse` script take?
* **Answer:** `maxlist`
* **Question:** Search for "smb" scripts in the `/usr/share/nmap/scripts/` directory. What is the filename of the script which determines the underlying OS of the SMB server?
* **Answer:** `smb-os-discovery.nse`
* **Question:** Read through this script. What does it depend on?
* **Answer:** `smb-brute`

### Task: Advanced Scan Mechanics (TCP, SYN, UDP)
* **Question:** Which RFC defines the appropriate behaviour for the TCP protocol?
* **Answer:** `RFC 9293`
* **Question:** If a port is closed, which flag should the server send back to indicate this?
* **Answer:** `RST`
* **Question:** There are two other names for a SYN scan, what are they?
* **Answer:** `Half-Open, Stealth`
* **Question:** Can Nmap use a SYN scan without Sudo permissions (Y/N)?
* **Answer:** `N`
* **Question:** If a UDP port doesn't respond to an Nmap scan, what will it be marked as?
* **Answer:** `open|filtered`
* **Question:** When a UDP port is closed, by convention the target should send back a "port unreachable" message. Which protocol would it use to do so?
* **Answer:** `ICMP`

### Task: Firewall Evasion Techniques
* **Question:** Which of the three shown scan types uses the URG flag?
* **Answer:** `xmas`
* **Question:** Why are NULL, FIN and Xmas scans generally used?
* **Answer:** `Firewall Evasion`
* **Question:** Which common OS may respond to a NULL, FIN or Xmas scan with a RST for every port?
* **Answer:** `Microsoft Windows`
* **Question:** How would you perform a ping sweep on the 172.16.x.x network (Netmask: 255.255.0.0) using Nmap? (CIDR notation)
* **Answer:** `nmap -sn 172.16.0.0/16`
* **Question:** Which simple (and frequently relied upon) protocol is often blocked, requiring the use of the `-Pn` switch?
* **Answer:** `ICMP`
* **Question:** [Research] Which Nmap switch allows you to append an arbitrary length of random data to the end of packets?
* **Answer:** `--data-length`

### Task: Practical Engagement
* **Question:** Does the target ip respond to ICMP echo (ping) requests (Y/N)?
* **Answer:** `N`
* **Question:** Perform an Xmas scan on the first 999 ports of the target -- how many ports are shown to be open or filtered?
* **Answer:** `999`
* **Question:** There is a reason given for this -- what is it?
* **Answer:** `No Response`
* **Question:** Perform a TCP SYN scan on the first 5000 ports of the target -- how many ports are shown to be open?
* **Answer:** `5`
* **Question:** Deploy the `ftp-anon` script against the box. Can Nmap login successfully to the FTP server on port 21? (Y/N)
* **Answer:** `Y`

---

## 🧠 Key Learnings
* **TCP Connect vs. SYN (Stealth) Scan:** 
  * A normal **TCP Connect (`-sT`)** completes the 3-way handshake. It's polite but gets logged by firewalls.
  * A **SYN Scan (`-sS`)** is "Half-Open". You send a SYN, get a SYN/ACK, but then immediately drop the connection before completing it. It avoids many logs but requires Administrator (Sudo) privileges.
* **The Power of NSE (Lua Scripts):** Nmap scripts are written in `Lua` and vastly expand Nmap's capabilities. They have categories like `safe`, `vuln`, and `intrusive`. You should *never* run `intrusive` scripts on a live production server as they can cause crashes. Scripts can also take custom arguments (like `maxlist` for FTP) and have dependencies on other scripts.
* **Defeating Ping Blocks (`-Pn`):** Many modern servers block ICMP (ping) requests. If Nmap can't ping a host, it assumes it's dead and skips it. By using `-Pn`, you force Nmap to assume the host is alive and scan it anyway.
* **Firewall Evasion (Xmas/NULL/FIN & Data Length):** 
  * Firewalls often block standard connection requests. Nmap bypasses this by sending malformed packets (like a Xmas scan, which lights up unusual flags). If the server is confused and stays silent, Nmap assumes the port is `open|filtered`. 
  * *Note:* Windows doesn't follow this rule and replies with `RST` to everything, making these stealth scans useless against Windows targets.
  * Using `--data-length` appends random junk data to your packets, changing their default size and bypassing basic signature-based firewalls that look for standard Nmap packet sizes.
