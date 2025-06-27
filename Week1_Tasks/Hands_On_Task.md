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

Images/nmap_scan.png


---

## ⚙️ Step 2: Capture and Analyze Packets with Wireshark

### 🔹 Objective

Capture packets during Nmap scan or normal network activity and analyze them in detail.

### 🔹 Packet Capture Process

* Open Wireshark and select the correct network interface (e.g., `eth0` or `wlan0`).
* Start capturing before running the Nmap scan to record all traffic.
* Use filters to focus on relevant packets during analysis.

### 🔹 Useful Filters

```text
# Show packets to/from a specific IP address
ip.addr == 192.168.56.101

# Show only TCP packets
tcp

# Show only ICMP packets (e.g., ping requests)
icmp
```

### 🔹 What to Observe

* SYN, ACK, FIN packets during port scanning
* ICMP Echo Requests and Replies
* Protocol and port information in packet headers

### 📸 Screenshot Reference

`screenshots/wireshark_capture.png`

### 📄 Packet Analysis Notes

`outputs/wireshark_notes.txt`

---

## 🧠 Key Learnings

* How Nmap detects live hosts and services on a network
* The types of packets exchanged during scanning (SYN, ICMP, etc.)
* Using Wireshark filters to analyze network traffic effectively
* Practical experience with network scanning and packet capturing tools

---

## 📁 Recommended Folder Structure

```
hands_on_nmap_wireshark/
│
├── screenshots/
│   ├── nmap_scan.png
│   └── wireshark_capture.png
│
├── outputs/
│   ├── nmap_scan.txt
│   └── wireshark_notes.txt
│
└── README.md
```

---

## 👩‍💻 Intern Details

**Name:** Marium Habib
**Program:** YoungDev Interns – Ethical Hacking
**Task:** Hands-On Nmap & Wireshark Analysis
**Date:** June 2025

---

## ⚠️ Disclaimer

> This task was performed in a **safe, legal, and isolated environment** using Kali Linux and virtual machines. It is intended for **educational purposes only**.

```

---

You can copy this entire content into a `README.md` file and upload it directly to your GitHub repo.  
If you want, I can also help prepare the full folder structure with placeholder screenshots and output files. Let me know!
```
