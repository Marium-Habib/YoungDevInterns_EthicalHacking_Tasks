# 📡 Hands-On Task – Nmap & Wireshark Analysis

In this task, I performed a basic **Nmap scan** on the local network to discover active hosts and open ports, and used **Wireshark** to capture and analyze network packets. Both tools are essential for network scanning and packet analysis, which are crucial steps in ethical hacking.

---

## 📝 Task Description

- Perform a basic **Nmap scan** on your local network to identify live hosts and their open ports.  
- Capture and analyze network traffic using **Wireshark** during scanning or regular network activity.

---

## 🔧 Tools Used

| Tool          | Purpose                                            |
|---------------|----------------------------------------------------|
| **Nmap**      | Network scanning to discover live hosts and ports |
| **Wireshark** | Real-time packet capturing and detailed analysis  |

---

## ⚙️ Step 1: Nmap Scan on Local Network

### 🔹 Objective

Identify active devices and open ports on the local network

![nmap Test Screenshot](Images/netstat_output.png)


---

## ⚙️ Step 2: Capture and Analyze Packets with Wireshark

### 🔹 Objective

Capture packets during Nmap scan or normal network activity and analyze them in detail.

### 🔹 Packet Capture Process

* Open Wireshark and select the correct network interface (e.g., `eth0` or `wlan0`).
* Use filters to focus on relevant packets during analysis.

#### ICMP Filter
![Wireshark Screenshot](Images/netstat_output.png)

#### DNS Filter
![Wireshark Screenshot](Images/netstat_output.png)

---

## 🧠 Key Learnings

* How Nmap detects live hosts and services on a network
* The types of packets exchanged during scanning (SYN, ICMP, etc.)
* Using Wireshark filters to analyze network traffic effectively
* Practical experience with network scanning and packet capturing tools
