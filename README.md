# Zeek-Security-tool

## 📌 Project Overview
This project demonstrates the use of Zeek, a network security monitoring tool, to analyze network traffic and detect suspicious activities.

Zeek captures network packets and generates structured logs which help in understanding network behavior and identifying potential threats.

---

## 🚀 Features
- Live network traffic monitoring
- Log generation and analysis
- Detection of suspicious activity (port scanning)
- DNS and connection tracking

---

## ⚙️ Tools Used
- Zeek (Network Security Monitor)
- Nmap (for simulating attacks)
- Ubuntu (Virtual Machine)

---

## 🧪 Demonstration

### 1. Live Traffic Monitoring
- Captured network traffic using Zeek
- Generated logs like conn.log and dns.log

### 2. Suspicious Activity Detection
- Simulated port scanning using Nmap
- Observed abnormal connection patterns in logs

### 3. Log Analysis
- Analyzed fields such as:
  - Source IP (id.orig_h)
  - Destination IP (id.resp_h)
  - Port numbers
  - Connection state

---

## 📂 Important Logs
- `conn.log` → Network connections
- `dns.log` → DNS queries
- `http.log` → Web traffic (if available)

---

## 🧠 Key Learning
Zeek does not directly label attacks but provides detailed logs. Suspicious behavior is identified by analyzing patterns like:
- Multiple rapid connections
- Short connection durations
- Reset connection states (RSTRH)

---

## 📦 Installation (Summary)

```bash
echo 'deb http://download.opensuse.org/repositories/security:/zeek/xUbuntu_24.04/ /' | sudo tee /etc/apt/sources.list.d/zeek.list
curl -fsSL https://download.opensuse.org/repositories/security:zeek/xUbuntu_24.04/Release.key | sudo gpg --dearmor -o /etc/apt/trusted.gpg.d/zeek.gpg
sudo apt update
sudo apt install zeek -y
