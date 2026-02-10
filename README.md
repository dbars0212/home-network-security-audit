# 🔐 Home Network Security Audit Lab

## 📌 Project Overview

Conducted a security-focused assessment of a home network to simulate real-world attacker reconnaissance techniques. The objective was to identify exposed services, validate firewall effectiveness, and reduce the overall attack surface.

This lab demonstrates hands-on experience with network scanning, threat identification, and security hardening — skills directly applicable to SOC Analyst and Cybersecurity roles.

---

## 🎯 Objectives

* Perform external and internal reconnaissance
* Identify open, filtered, and closed ports
* Detect potentially risky services
* Evaluate NAT and firewall behavior
* Recommend security hardening actions

---

## 🛠 Tools Used

* **Nmap** – Network discovery and security auditing
* **Ubuntu Server** – Scanning environment
* **Home Router Firewall** – Security validation

---

## 🔎 Methodology

### 1️⃣ Host Discovery

Verified router accessibility and bypassed ICMP blocking:

```bash
sudo nmap -Pn <public-ip>
```

---

### 2️⃣ Full TCP Port Scan

Enumerated all 65,535 ports to identify exposed services:

```bash
sudo nmap -Pn -p- -T4 --max-retries 2 <public-ip>
```

**Result:**

* The majority of ports filtered (strong firewall posture)
* One high-numbered port was detected and investigated

---

### 3️⃣ Service Detection

Performed targeted fingerprinting on discovered ports:

```bash
sudo nmap -Pn -sV -p<port> <public-ip>
```

---

## 📊 Key Findings

✅ Firewall actively filtered unsolicited traffic
✅ No commonly exploited ports exposed (Telnet, FTP, RDP)
✅ NAT functioning correctly
✅ Minimal external attack surface

**Security Assessment:** Strong defensive posture comparable to enterprise baseline configurations.

---

## 🛡 Security Improvements Implemented

* Reviewed router for unnecessary port forwarding
* Recommended disabling UPnP to prevent automatic port exposure
* Verified remote administration was disabled
* Confirmed firmware was up to date

---

## 🚨 Skills Demonstrated

* Network reconnaissance
* Threat analysis
* Security auditing
* Firewall validation
* Risk mitigation
* Technical documentation

---

## 💡 What I Learned

This project strengthened my ability to think like an attacker while acting as a defender — identifying weaknesses before they can be exploited.

It also reinforced the importance of layered security controls such as NAT, firewall rules, and service minimization.

---

## ✅ Future Enhancements

* Perform vulnerability scans using NSE scripts
* Build a segmented home lab network
* Integrate SIEM for traffic monitoring
* Conduct internal lateral movement simulations

---

## 👨‍💻 Author

**Darnell Barber**
B.S. Information Systems & Cybersecurity

Aspiring SOC Analyst passionate about threat detection, incident response, and defensive security.

