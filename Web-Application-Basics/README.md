# 🌐 TryHackMe Writeup: Web Application Basics

## 📝 Room Overview
* **Room Name:** Web Application Basics
* **Platform:** TryHackMe
* **Difficulty:** Easy
* **Category:** Web Security / AppSec

## 🎯 Objective
Understand the foundational architecture of the World Wide Web: dissecting HTTP/HTTPS mechanics, URL anatomy, request/response headers, status codes, cookie security flags, and REST API manipulation.

---

## 💡 Tasks & Answers

### Task: Web Architecture & URLs
* **Question:** Which component on a computer is responsible for hosting and delivering content for web applications?
* **Answer:** `web server`
* **Question:** Which tool is used to access and interact with web applications?
* **Answer:** `web browser`
* **Question:** Which component acts as a protective layer, filtering incoming traffic to block malicious attacks, and ensuring the security of the web application?
* **Answer:** `web application firewall`
* **Question:** Which protocol provides encrypted communication to ensure secure data transmission between a web browser and a web server?
* **Answer:** `HTTPS`
* **Question:** What term describes the practice of registering domain names that are misspelt variations of popular websites to exploit user errors and potentially engage in fraudulent activities?
* **Answer:** `Typosquatting`
* **Question:** What part of a URL is used to pass additional information, such as search terms or form inputs, to the web server?
* **Answer:** `Query String`

### Task: HTTP Messages & Requests
* **Question:** Which HTTP message is returned by the web server after processing a client's request?
* **Answer:** `HTTP response`
* **Question:** What follows the headers in an HTTP message?
* **Answer:** `Empty Line`
* **Question:** Which HTTP protocol version became widely adopted and remains the most commonly used version for web communication, known for introducing features like persistent connections and chunked transfer encoding?
* **Answer:** `HTTP/1.1`
* **Question:** Which HTTP request method describes the communication options for the target resource, allowing clients to determine which HTTP methods are supported by the web server?
* **Answer:** `OPTIONS`
* **Question:** In an HTTP request, which component specifies the specific resource or endpoint on the web server that the client is requesting, typically appearing after the domain name in the URL?
* **Answer:** `URL Path`
* **Question:** Which HTTP request header specifies the domain name of the web server to which the request is being sent?
* **Answer:** `Host`
* **Question:** What is the default content type for form submissions in an HTTP request where the data is encoded as key-value pairs in a query string format?
* **Answer:** `application/x-www-form-urlencoded`
* **Question:** Which part of an HTTP request contains additional information like host, user agent, and content type, guiding how the web server should process the request?
* **Answer:** `Request Headers`

### Task: HTTP Responses & Status Codes
* **Question:** What part of an HTTP response provides the HTTP version, status code, and a brief explanation of the response's outcome?
* **Answer:** `Status Line`
* **Question:** Which category of HTTP response codes indicates that the web server encountered an internal issue or is unable to fulfill the client's request?
* **Answer:** `Server Error Responses`
* **Question:** Which HTTP status code indicates that the requested resource could not be found on the web server?
* **Answer:** `404`

### Task: Security Headers & Cookie Protection
* **Question:** Which HTTP response header can reveal information about the web server's software and version, potentially exposing it to security risks if not removed?
* **Answer:** `Server`
* **Question:** Which flag should be added to cookies in the Set-Cookie HTTP response header to ensure they are only transmitted over HTTPS, protecting them from being exposed during unencrypted transmissions?
* **Answer:** `Secure`
* **Question:** Which flag should be added to cookies in the Set-Cookie HTTP response header to prevent them from being accessed via JavaScript, thereby enhancing security against XSS attacks?
* **Answer:** `HttpOnly`
* **Question:** In a Content Security Policy (CSP) configuration, which property can be set to define where scripts can be loaded from?
* **Answer:** `script-src`
* **Question:** When configuring the Strict-Transport-Security (HSTS) header to ensure that all subdomains of a site also use HTTPS, which directive should be included to apply the security policy to both the main domain and its subdomains?
* **Answer:** `includeSubDomains`
* **Question:** Which HTTP header directive is used to prevent browsers from interpreting files as a different MIME type than what is specified by the server, thereby mitigating content type sniffing attacks?
* **Answer:** `nosniff`

### Task: Practical API Interaction
* **Question:** Make a GET request to `/api/users`. What is the flag?
* **Answer:** `THM{YOU_HAVE_JUST_FOUND_THE_USER_LIST}`
* **Question:** Make a POST request to `/api/user/2` and update the country of Bob from UK to US. What is the flag?
* **Answer:** `THM{YOU_MODIFIED_THE_USER_DATA}`
* **Question:** Make a DELETE request to `/api/user/1` to delete the user. What is the flag?
* **Answer:** `THM{YOU_HAVE_JUST_DELETED_A_USER}`

---

## 🧠 Key Learnings
* **Client vs. Server Conversation:** Web browsing is just a conversation. Your browser (the client) asks: "Can I have this webpage?" (HTTP Request). The web server replies with an envelope (Headers) and the actual content (Body) along with a three-digit status receipt (HTTP Response, e.g., 200 for OK, 404 for Not Found).
* **HTTP Verbs (Actions):** 
  * `GET` is for reading data without changing anything.
  * `POST` is for sending new data or updating something.
  * `DELETE` tells the database to erase a record.
* **Cookie Shields (`Secure` & `HttpOnly`):** Cookies hold your active login session. If an attacker injects malicious JavaScript (XSS), the `HttpOnly` flag stops that script from stealing your cookie. The `Secure` flag ensures the cookie is never sent across cleartext HTTP, only encrypted HTTPS.
* **Information Leakage via the `Server` Header:** Web servers often boast about themselves by saying "Server: Apache 2.4.41". Removing this header stops attackers from instantly knowing what outdated software you are running.
* **Security Guard Headers (CSP & HSTS):** `CSP` tells the browser: "Only download JavaScript from my trusted server, nowhere else." `HSTS` forces the browser to refuse any insecure HTTP connection completely.
*
