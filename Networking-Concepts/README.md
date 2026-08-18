# 🏗️ Networking Concepts (TryHackMe)

## 🎯 Objective
Understand network protocols and manually interact with a web server using raw TCP connections.

## 🧠 Core Concepts & Execution
* **Execution Environment:** Used the TryHackMe integrated terminal.
* **Tasks Performed:**
  * Initiated a direct connection to a web server on port 80 using the command: `telnet MACHINE_IP 80`.
  * Manually sent an HTTP GET request (`GET / HTTP/1.1` and `Host: telnet.thm`).
  * Analyzed the server's HTTP `200 OK` response header to identify the web server software and its version.
  * **Discovered Server Version:** `lighttpd/1.4.63`

## 🚩 Proof of Compromise
* **Flag Found:** `THM{TELNET_MASTER}`
*
