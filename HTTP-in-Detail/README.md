# 🌐 HTTP in Detail (TryHackMe)

## 🎯 Objective
Understand how HTTP requests are structured and manually send different types of HTTP requests to a web server.

## 🧠 Core Concepts & Execution
* **Execution Environment:** Used the TryHackMe in-browser HTTP emulator to build and send API requests.
* **Tasks Performed:**
  * Sent a `GET` request to `/room` to retrieve data.
  * Sent a `GET` request to `/blog` using an `id` parameter set to 1.
  * Sent a `DELETE` request to `/user/1` to remove an entry.
  * Sent a `PUT` request to `/user/2` with a body parameter `username` set to `admin`.
  * Sent a `POST` request to `/login` using body parameters `username=thm` and `password=letmein` to authenticate.

## 🚩 Proof of Compromise
* **Flags Found:** 
  * `THM{YOU'RE_IN_THE_ROOM}`
  * `THM{YOU_FOUND_THE_BLOG}`
  * `THM{USER_IS_DELETED}`
  * `THM{USER_HAS_UPDATED}`
  * `THM{HTTP_REQUEST_MASTER}`
