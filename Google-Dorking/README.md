# 🔍 TryHackMe Writeup: Google Dorking

## 📝 Room Overview
* **Room Name:** Google Dorking
* **Platform:** TryHackMe
* **Difficulty:** Easy
* **Category:** OSINT / Reconnaissance

## 🎯 Objective
Explaining how Search Engines work and leveraging them into finding hidden content using advanced search operators.

---

## 💡 Tasks & Answers

### Task: Search Engine Basics
* **Question:** Name the key term of what a "Crawler" is used to do.
* **Answer:** `Index`
* **Question:** What is the name of the technique that "Search Engines" use to retrieve this information about websites?
* **Answer:** `Crawling`
* **Question:** What is an example of the type of contents that could be gathered from a website?
* **Answer:** `Keywords`

### Task: Robots.txt & Sitemaps
* **Question:** Where would "robots.txt" be located on the domain "ablog.com"
* **Answer:** `ablog.com/robots.txt`
* **Question:** If a website was to have a sitemap, where would that be located?
* **Answer:** `/sitemap.xml`
* **Question:** How would we only allow "Bingbot" to index the website?
* **Answer:** `User-agent: Bingbot`
* **Question:** How would we prevent a "Crawler" from indexing the directory "/dont-index-me/"?
* **Answer:** `Disallow: /dont-index-me/`
* **Question:** What is the extension of a Unix/Linux system configuration file that we might want to hide from "Crawlers"?
* **Answer:** `.conf`
* **Question:** What is the typical file structure of a "Sitemap"?
* **Answer:** `XML`
* **Question:** What real life example can "Sitemaps" be compared to?
* **Answer:** `Map`
* **Question:** Name the keyword for the path taken for content on a website
* **Answer:** `Route`

### Task: What is Google Dorking?
* **Question:** What would be the format used to query the site bbc.co.uk about flood defences
* **Answer:** `site: bbc.co.uk flood defences`
* **Question:** What term would you use to search by file type?
* **Answer:** `filetype:`
* **Question:** What term can we use to look for login pages?
* **Answer:** `intitle: login`
*
