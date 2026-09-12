# 🌐 TryHackMe Writeup: Introductory Networking

## 📝 Room Overview
* **Room Name:** Introductory Networking
* **Platform:** TryHackMe
* **Difficulty:** Easy
* **Category:** Fundamentals / Networking

## 🎯 Objective
Understand the core theories of computer networking, including the OSI Model, TCP/IP Model, encapsulation, and hands-on usage of essential command-line networking tools (Ping, Traceroute, WHOIS, and Dig).

---

## 💡 Tasks & Answers

### Task: The OSI Model
* **Question:** Which layer would choose to send data over TCP or UDP? 
* **Answer:** `4`
* **Question:** Which layer checks received information to make sure that it hasn't been corrupted? 
* **Answer:** `2`
* **Question:** In which layer would data be formatted in preparation for transmission? 
* **Answer:** `2`
* **Question:** Which layer transmits and receives data? 
* **Answer:** `1`
* **Question:** Which layer encrypts, compresses, or otherwise transforms the initial data to give it a standardised format? 
* **Answer:** `6`
* **Question:** Which layer tracks communications between the host and receiving computers? 
* **Answer:** `5`
* **Question:** Which layer accepts communication requests from applications? 
* **Answer:** `7`
* **Question:** Which layer handles logical addressing?
* **Answer:** `3`
* **Question:** When sending data over TCP, what would you call the "bite-sized" pieces of data?
* **Answer:** `Segments`
* **Question:** [Research] Which layer would the FTP protocol communicate with?
* **Answer:** `7`
* **Question:** Which transport layer protocol would be best suited to transmit a live video?
* **Answer:** `UDP`

### Task: Encapsulation
* **Question:** How would you refer to data at layer 2 of the encapsulation process (with the OSI model)?
* **Answer:** `Frames`
* **Question:** How would you refer to data at layer 4 of the encapsulation process (with the OSI model), if the UDP protocol has been selected?
* **Answer:** `Datagrams`
* **Question:** What process would a computer perform on a received message?
* **Answer:** `De-encapsulation`
* **Question:** Which is the only layer of the OSI model to add a trailer during encapsulation?
* **Answer:** `Data Link`
* **Question:** Does encapsulation provide an extra layer of security (Aye/Nay)?
* **Answer:** `Aye`

### Task: The TCP/IP Model
* **Question:** Which model was introduced first, OSI or TCP/IP?
* **Answer:** `TCP/IP`
* **Question:** Which layer of the TCP/IP model covers the functionality of the Transport layer of the OSI model (Full Name)?
* **Answer:** `Transport`
* **Question:** Which layer of the TCP/IP model covers the functionality of the Session layer of the OSI model (Full Name)?
* **Answer:** `Application`
* **Question:** The Network Interface layer of the TCP/IP model covers the functionality of two layers in the OSI model. These layers are Data Link, and?.. (Full Name)?
* **Answer:** `Physical`
* **Question:** Which layer of the TCP/IP model handles the functionality of the OSI network layer?
* **Answer:** `Internet`
* **Question:** What kind of protocol is TCP?
* **Answer:** `Connection-based`
* **Question:** What is SYN short for?
* **Answer:** `Synchronise`
* **Question:** What is the second step of the three way handshake?
* **Answer:** `SYN/ACK`

### Task: Networking Tools (Ping, Traceroute, WHOIS, DNS/Dig)
* **Question:** What command would you use to ping the bbc.co.uk website?
* **Answer:** `ping bbc.co.uk`
* **Question:** Ping muirlandoracle.co.uk. What is the IPv4 address?
* **Answer:** `217.160.0.152`
* **Question:** What switch lets you change the interval of sent ping requests?
* **Answer:** `-i`
* **Question:** What switch would allow you to restrict requests to IPv4?
* **Answer:** `-4`
* **Question:** What switch would give you a more verbose output?
* **Answer:** `-v`
* **Question:** What switch would you use to specify an interface when using Traceroute?
* **Answer:** `-i`
* **Question:** What switch would you use if you wanted to use TCP SYN requests when tracing the route?
* **Answer:** `-T`
* **Question:** [Lateral Thinking] Which layer of the TCP/IP model will traceroute run on by default (Windows)?
* **Answer:** `Internet`
* **Question:** What is the registrant postal code for facebook.com?
* **Answer:** `94025`
* **Question:** When was the facebook.com domain first registered (Format: DD/MM/YYYY)?
* **Answer:** `29/03/1997`
* **Question:** Which city is the registrant based in? (microsoft.com)
* **Answer:** `Redmond`
* **Question:** [OSINT] What is the name of the golf course that is near the registrant address for microsoft.com?
* **Answer:** `Bellevue Golf Course`
* **Question:** What is the registered Tech Email for microsoft.com?
* **Answer:** `msnhst@microsoft.com`
* **Question:** What is DNS short for?
* **Answer:** `Domain Name System`
* **Question:** What is the first type of DNS server your computer would query when you search for a domain?
* **Answer:** `Recursive`
* **Question:** What type of DNS server contains records specific to domain extensions (i.e. .com, .co.uk*, etc)*?
* **Answer:** `Top-Level Domain`
* **Question:** Where is the very first place your computer would look to find the IP address of a domain?
* **Answer:** `Hosts File`
* **Question:** [Research] Google runs two public DNS servers. One of them can be queried with the IP 8.8.8.8, what is the IP address of the other one?
* **Answer:** `8.8.4.4`
* **Question:** If a DNS query has a TTL of 24 hours, what number would the dig query show?
* **Answer:** `86400`

---

## 🧠 Key Learnings
* **The OSI Model (7 Layers):** Think of the OSI model like sending a physical letter. 
  * Layer 7 (Application) is you writing the letter. 
  * Layer 3 (Network) is the post office adding the destination IP address (like a home address). 
  * Layer 1 (Physical) is the actual mail truck or fiber optic cable carrying the message.
* **TCP vs. UDP (Layer 4):** 
  * **TCP** is like a certified phone call. It guarantees the message arrives in order and checks for errors (Connection-based). 
  * **UDP** is like throwing a ball. It's incredibly fast, but if the ball drops, it doesn't care (best for live video or gaming where speed matters more than perfection).
* **Encapsulation:** When data moves down the OSI model from Layer 7 to Layer 1, each layer adds its own "envelope" (header) of instructions. At Layer 4 it's a Segment, at Layer 3 it's a Packet, at Layer 2 it's a Frame. When the receiving computer gets it, it unboxes it (De-encapsulation).
* **Basic Tools:**
  * `Ping`: Checks if a computer is alive by shouting "Hello!" and waiting for a reply.
  * `Traceroute`: Maps out every single router (hop) your data jumps through to reach its destination.
  * `WHOIS`: The phonebook of the internet. It tells you who owns a domain name and where they live.
  * `Dig/DNS`: Translates human names (like google.com) into computer numbers (IP addresses).
