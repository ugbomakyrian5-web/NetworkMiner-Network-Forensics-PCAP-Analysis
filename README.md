# 🔍 SOC Lab: NetworkMiner Network Forensics & PCAP Analysis (SOC Level 1)

[![Platform](https://img.shields.io/badge/Platform-TryHackMe-black?style=flat&logo=tryhackme)](https://tryhackme.com)
[![Path](https://img.shields.io/badge/Path-SOC%20Level%201-blue?style=flat)](https://tryhackme.com/path/outline/soclevel1)
[![Topic](https://img.shields.io/badge/Topic-Network%20Forensics%20%26%20PCAP%20Analysis-007ACC?style=flat)](https://tryhackme.com/room/networkminer)
[![Difficulty](https://img.shields.io/badge/Difficulty-Medium-orange?style=flat)](https://tryhackme.com/room/networkminer)
[![Status](https://img.shields.io/badge/Status-Completed-success?style=flat)]()
[![Tool](https://img.shields.io/badge/Tool-NetworkMiner-green?style=flat)](https://netresec.com)

**Real-world network forensics lab** using **NetworkMiner** (v1.6 & v2.7) to perform rapid PCAP triage, artifact extraction, credential harvesting, file carving, and anomaly detection — core skills used daily by SOC Analysts and Threat Hunters.

Analyzed 6 different PCAP files and successfully answered all 22 questions with full documentation.

## 📌 Quick Summary
**Room**: NetworkMiner  
**Scenario**: Multiple captured network traffic files containing reconnaissance, credential theft, file exfiltration, device information, and anomalies  
**Key Deliverables**:
- Host profiling & OS fingerprinting
- Credential extraction (usernames + full NTLM hashes)
- File, image, and email carving
- TLS anomaly detection
- Tool version comparison (v1.6 vs v2.7)
- All 22 room questions answered with annotated evidence

## 🎯 Objectives & Achievements
✅ Mastered NetworkMiner interface and all major tabs (Hosts, Sessions, DNS, Credentials, Files, Images, Parameters, Keywords, Messages, Anomalies)  
✅ Performed fast PCAP triage on real captured traffic  
✅ Extracted credentials, files, images, emails, and cleartext data  
✅ Identified operating systems, devices, and suspicious behavior  
✅ Detected TLS anomalies and MAC address conflicts  
✅ Compared NetworkMiner v1.6 vs v2.7 capabilities  
✅ Delivered complete, professional forensic documentation

## 🛠 Tools & Workflow
- TryHackMe Ubuntu 20.04 VM (split-view)
- NetworkMiner Free Edition (v1.6.1 and v2.7.2)
- Hosts, Sessions, Credentials, Files, Images, Messages, Parameters, Anomalies tabs + metadata viewer

## 🔎 Detailed Analysis & Findings

### mx-3.pcap Analysis
- Total frames: **460**
- IP addresses sharing same MAC with 145.253.2.203: **2**
- Packets sent from 65.208.228.223: **72**
- Web server banner: **Apache**

### mx-4.pcap Analysis
- Extracted username for 02694W-WIN10: **`#B\Administrator`**
- Extracted full NTLM hash for the logged-in user

### mx-7.pcap Analysis
- Linux distribution in frame 63075: **CentOS**
- Page header in frame 75942: **Password-Ned AB**
- Source address of image `ads.bmp.2E5F0FD9[1].bmp`: **80.239.178.187**
- Possible TLS anomaly frame: **36255**

### mx-9.pcap Analysis (Messages)
- Platform that sent email starting with “You have more”: **Facebook**
- Email address of Branson Matheson: **`branson@sandsite.org`**

### Case1.pcap & Case2.pcap Exercises
- OS of host 131.151.37.122: **Windows NT 4**
- USB product brand name: **ASIX**
- Phone model extracted: **Lumia 535**
- Password for homer.pwned.se@gmx.com: **`spring2015`**
- DNS query of frame 62001: **`pop.gmx.com`**

## 🔎 Evidence – Lab Screenshots
**All 22 screenshots are fully annotated and included below:**

### 1. Total number of frames in mx-3.pcap
<img width="1366" height="729" alt="image" src="https://github.com/user-attachments/assets/69569c31-5354-4763-97e0-6dafeac5b3f8" />

### 2. IP addresses sharing same MAC with 145.253.2.203
<img width="1366" height="726" alt="image" src="https://github.com/user-attachments/assets/6fc8c9c3-cf7b-452d-bc75-17fc395c0f4c" />

### 3. Packets sent from host 65.208.228.223
<img width="1362" height="728" alt="image" src="https://github.com/user-attachments/assets/b15512e7-aa8b-476c-a08b-809734a4afd7" />

### 4. Web server banner under host 65.208.228.223
<img width="1364" height="726" alt="image" src="https://github.com/user-attachments/assets/69b596b4-3234-4592-bfc1-2dbbb26b8e83" />

### 5. Extracted username for 02694W-WIN10 host
<img width="1366" height="724" alt="image" src="https://github.com/user-attachments/assets/b001badb-84d0-4e78-b4d5-630e8440dd12" />

### 6. Extracted NTLM hash for the logged-in user
<img width="1366" height="724" alt="image" src="https://github.com/user-attachments/assets/e084a8b1-ad20-4f36-87ca-cf69dd32e05c" />

### 7. Linux distro mentioned in frame 63075
<img width="1366" height="726" alt="image" src="https://github.com/user-attachments/assets/182e6e90-5355-4443-90be-ffa4fb475850" />

### 8. Page header associated with frame 75942
<img width="1366" height="733" alt="image" src="https://github.com/user-attachments/assets/f7be31d1-2ee4-4673-a686-edbd74a9e58c" />

### 9. Source address of image ads.bmp.2E5F0FD9[1].bmp
<img width="1366" height="733" alt="image" src="https://github.com/user-attachments/assets/f1dbe853-5b24-4432-8c7d-dfeb9bfcf16f" />

### 10. Frame number of the possible TLS anomaly
<img width="1366" height="727" alt="image" src="https://github.com/user-attachments/assets/faed13dc-1ae2-4836-a490-054230c47792" />

### 11. Platform that sent email starting with “You have more”
<img width="1366" height="726" alt="image" src="https://github.com/user-attachments/assets/434477d6-45d5-46e6-98d7-5f52b130e15e" />

### 12. Email address of Branson Matheson
<img width="1366" height="726" alt="image" src="https://github.com/user-attachments/assets/ec62183f-8882-461e-8716-457ae7018db3" />

### 13. OS name of host 131.151.37.122
<img width="1366" height="724" alt="image" src="https://github.com/user-attachments/assets/1e49b917-366d-41cf-b9a5-2bf827073684" />

### 14. Data bytes received from host 131.151.32.91 to 131.151.37.122 (port 1065)
<img width="1364" height="724" alt="image" src="https://github.com/user-attachments/assets/96784e45-9818-4d86-ae97-0ba689b73752" />

### 15. Data bytes received from host 131.151.37.122 to 131.151.32.21 (port 143)
<img width="1366" height="722" alt="image" src="https://github.com/user-attachments/assets/02e29e46-9e73-4c40-9537-110c424645bf" />

### 16. Sequence number of frame 9 (v1.6)
<img width="1366" height="728" alt="image" src="https://github.com/user-attachments/assets/65915786-116e-4d2c-a022-e712a7b727b2" />

### 17. Number of detected content types
<img width="1366" height="727" alt="image" src="https://github.com/user-attachments/assets/a89458e4-f115-4ba2-b195-54514c231c1e" />

### 18. USB product’s brand name
<img width="1366" height="728" alt="image" src="https://github.com/user-attachments/assets/94659e46-2854-47c3-9dbe-c7c42f089d0b" />

### 19. Name of the phone model
<img width="1366" height="728" alt="image" src="https://github.com/user-attachments/assets/a859af66-1c9e-4f0d-b2e1-1365ee384653" />

### 20. Source IP of the fish image
<img width="1366" height="724" alt="image" src="https://github.com/user-attachments/assets/58a44988-399a-42b5-8415-efb352e82bd0" />

### 21. Password of homer.pwned.se@gmx.com
<img width="1366" height="728" alt="image" src="https://github.com/user-attachments/assets/ba855c73-16cc-47e1-9ed9-be848fef9b7b" />

### 22. DNS Query of frame 62001
<img width="1366" height="726" alt="image" src="https://github.com/user-attachments/assets/96edb96d-7958-47dc-b0be-5de206ff0400" />

## 🧠 MITRE ATT&CK Mapping
| Tactic              | Technique                        | ID      | Observed in Lab                     |
|---------------------|----------------------------------|---------|-------------------------------------|
| Discovery           | Network Service Scanning         | T1046   | Reconnaissance traffic              |
| Credential Access   | Adversary-in-the-Middle          | T1557   | Credential harvesting               |
| Collection          | Data from Network Share          | T1039   | File & image carving                |
| Discovery           | System Information Discovery     | T1082   | OS & device fingerprinting          |

## 🛡 Defensive Recommendations
- Deploy NetworkMiner or similar NFAT tools for rapid PCAP triage during incidents
- Enforce TLS decryption and monitor for anomalous TLS records
- Block cleartext credential transmission and unusual DNS/ICMP activity
- Combine NetworkMiner (quick overview) with Wireshark (deep analysis)

## 📌 Key Takeaways & Real-World Value
- NetworkMiner is excellent for **fast artifact extraction** and initial triage — critical during time-sensitive incidents
- Understanding tool limitations (v1.6 vs v2.7) shows practical operational awareness
- This lab directly translates to real SOC workflows where analysts must quickly pull IOCs before deep-dive investigation

**Hands-on network forensics & PCAP analysis** — ready for Tier-1/2 SOC Analyst, Threat Hunter, and Blue Team roles.

Feel free to fork, star, or reach out with questions. Open to feedback and collaboration!

**Completed:** March 2026

MIT License – see the [LICENSE](LICENSE) file for details.
