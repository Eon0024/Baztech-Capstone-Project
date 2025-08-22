# SOC Capstone Project – BazTech

## 📌 Overview
This project is a **Security Operations Center (SOC) capstone exercise** that simulates real-world cyberattacks in a controlled environment.  
The goal was to evaluate detection, investigation, and response capabilities using **Wazuh SIEM**, network segmentation with **pfSense**, and endpoint log collection from both **Ubuntu** and **Windows** hosts.

## ⚡ Project Objectives
- Simulate brute-force attacks against multiple endpoints.
- Collect and analyze logs from Ubuntu and Windows systems.
- Detect and correlate suspicious activity using Wazuh.
- Recommend short- and long-term security improvements.

## 🛠️ Environment Setup
- **pfSense** – Network segmentation (WAN, LAN, IT Dept, DMZ).
- **Wazuh Manager** – Centralized log collection and analysis.
- **Ubuntu (DMZ server)** – Target for SSH brute-force attacks.
- **Windows 10 workstation** – Target for RDP brute-force attacks.
- **Kali Linux** – Attacker machine for brute-force simulations.

## 🔍 Attack Simulations
1. **SSH brute-force attack** on Ubuntu server (`/var/log/auth.log` showed 45 failed attempts).
2. **RDP brute-force attack** on Windows workstation (Event ID 4625 logs with 6 failed attempts).
3. Wazuh agents detected and correlated the attacks across both endpoints.

## 🧾 Findings
- Same attacker IP was identified targeting both systems.
- SOC team successfully correlated events across hosts.
- No compromise occurred, but clear evidence of reconnaissance and brute-force attempts.

## ✅ Recommendations
- Restrict SSH and RDP access via firewall rules.
- Enforce account lockout policies and Fail2Ban.
- Enable MFA for remote access.
- Deploy IDS/IPS for deeper inspection.
- Strengthen SOC monitoring with advanced correlation rules.

## 📂 Repository Contents
- `Allison's SOC_Capstone_Report:`[Allison's SOC_Capstone_Report.pdf](https://github.com/user-attachments/files/21942268/Allison.s.SOC_Capstone_Report.pdf)
- `Allison's SOC_Capstone_Presentation:`[Allison's SOC_Capstone_Presentation.pdf](https://github.com/user-attachments/files/21942287/Allison.s.SOC_Capstone_Presentation.pdf)
---

👨‍💻 **Author:** Allison  
📅 **Date:** August 2025
