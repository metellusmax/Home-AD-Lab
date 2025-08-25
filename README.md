# 🧪 Home AD Lab

## 🎯 Objective

The **Home AD Lab** project builds a comprehensive virtual lab environment using **VirtualBox**, simulating a Windows Active Directory (AD) domain. It explores domain operations, event forwarding to **Splunk**, and adversary simulation using **Kali Linux** and **Atomic Red Team**.

This project is designed to provide **hands-on experience** with both **blue team (defensive)** and **red team (offensive)** operations — all within a controlled and realistic environment.

---

## 🧠 Skills Learned

- Installing, configuring, and managing Active Directory domain controllers
- Creating and managing user accounts, groups, and organizational units (OUs)
- Forwarding Windows event logs to Splunk
- Simulating real-world attacks with Atomic Red Team
- Analyzing attack techniques and developing detections in Splunk
- Practicing password attacks and exploiting misconfigurations
- Coordinating multiple tools in a fully integrated lab environment
- Developing critical thinking and cybersecurity problem-solving skills

---

## 🛠️ Tools Used

| Tool                          | Purpose                                                   |
|-------------------------------|-----------------------------------------------------------|
| **VirtualBox**                | Virtualization platform for running lab machines         |
| **Windows Server 2022**       | Active Directory Domain Controller; runs Sysmon          |
| **Windows 10**                | Domain-joined workstation; runs Sysmon + Atomic Red Team |
| **Ubuntu Server**             | Hosts the Splunk server                                  |
| **Splunk**                    | Log ingestion, search, and analysis                      |
| **Sysmon**                    | System activity logging on both Windows machines         |
| **Splunk Universal Forwarder**| Forwards logs to Splunk from Windows machines            |
| **Atomic Red Team**           | Simulates adversary behavior (on Windows 10)             |
| **Kali Linux**                | Attacker machine used for password brute-force testing   |
| **Crowbar**                   | Brute-force tool used on Kali to attack domain accounts  |
| **draw.io**                   | Logical diagram creation                                 |

---

## 🗺️ Lab Architecture & Diagram

Below is the logical diagram created via **draw.io**, used to plan and map the lab environment.

> 📌 *Ref 1: Logical Diagram*

<img width="652" height="617" alt="Lab Diagram" src="https://github.com/user-attachments/assets/fe34b4d1-6d81-456d-b1e4-ec71f38580fe" />

---

## 🧩 Lab Components Overview

1. **Windows Server 2022**
   - Acts as the Domain Controller (AD, DNS, DHCP)
   - Sysmon installed for detailed event logging
   - Logs forwarded to Splunk via Universal Forwarder

2. **Windows 10**
   - Joined to the AD domain
   - Runs Sysmon and Atomic Red Team
   - Logs forwarded to Splunk via Universal Forwarder

3. **Ubuntu Server**
   - Hosts Splunk Enterprise (free license)
   - Ingests logs from both Windows machines for analysis

4. **Kali Linux**
   - Used for red team simulation
   - Uses **Crowbar** to perform brute-force attacks against domain user accounts
   - Helps test Splunk detection rules for failed logins and password spraying

---

## 🔬 Use Cases

- Practice detection engineering with Splunk and Sysmon logs  
- Analyze attack behaviors and build queries for detection  
- Test GPO enforcement and Active Directory misconfigurations  
- Simulate red team TTPs with Atomic Red Team  
- Simulate brute-force and password spraying attacks using Crowbar  
- Perform log correlation and build dashboards in Splunk

---

## 📜 Disclaimer

> ⚠️ This lab is intended for **educational and ethical purposes only**. Never perform offensive operations in environments you do not own or have explicit permission to test.

---

## 🙏 Acknowledgements

- [MyDFIR YouTube Channel](https://www.youtube.com/@MyDFIR)
- [Red Canary Atomic Red Team](https://github.com/redcanaryco/atomic-red-team)
- [Splunk](https://www.splunk.com/)
- [Microsoft Sysinternals (Sysmon)](https://learn.microsoft.com/en-us/sysinternals/)
- [MITRE ATT&CK Framework](https://attack.mitre.org/)

---

## 👤 Author

**Max Metellus**  
[GitHub: @metellusmax](https://github.com/metellusmax/metellusmax)
