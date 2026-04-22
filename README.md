# Ubuntu 24.04 STIG Hardening Lab 🔐

## 📌 Overview
This project demonstrates the implementation of DISA STIG-aligned security controls on an Ubuntu 24.04 virtual machine using OpenSCAP. The lab simulates a real-world vulnerability remediation workflow by identifying noncompliant configurations, applying fixes, and validating improvements through iterative scanning.

---

## 🎯 Objectives
- Perform a baseline STIG compliance assessment
- Identify high-impact security misconfigurations
- Apply targeted remediations
- Measure and validate compliance improvement
- Document technical challenges and solutions

---

## 🧪 Lab Environment
- **OS:** Ubuntu 24.04 (VM)
- **Hypervisor:** Oracle VirtualBox
- **Host:** Windows 11
- **Tools:**
  - OpenSCAP
  - SCAP Security Guide (SSG)
  - Linux CLI

---

## 📊 Compliance Results

| Metric | Initial Scan | Final Scan |
|------|------------|-----------|
| Compliance Score | ~65% | Improved |
| High Severity Failures | Multiple | Reduced |
| Total Failed Rules | 151 | Reduced |

> ⚠️ Note: Some findings require OS reinstall or architecture changes and were documented instead of forcefully remediated.

---

## 🔧 Remediation Highlights

### 🔐 Boot Security
- Configured GRUB bootloader password
- Secured boot process against unauthorized modification

### 👤 Authentication Hardening
- Disabled empty password logins
- Strengthened account security policies

### 🧾 Audit & Logging
- Fixed audit rule file permissions
- Ensured proper monitoring configurations

### 🛡️ System Integrity
- Installed and initialized AIDE
- Verified integrity monitoring setup

### 🔌 Service Hardening
- Disabled insecure services
- Reduced attack surface

### ⚙️ System Configuration
- Set system time to UTC
- Disabled Ctrl-Alt-Del reboot/logout behavior

---

## ❗ Key Challenges & Troubleshooting

- GRUB misconfiguration caused system lockout  
  → Resolved via recovery mode and config rollback  

- Some GNOME settings required dconf configuration instead of gsettings  

- Certain STIG controls failed due to:
  - FIPS mode not enabled
  - Lack of full disk encryption
  - Installation-time dependencies  

---

## 📸 Screenshots

| Description | Image |
|------------|------|
| Initial Scan Results |
<img width="1176" height="648" alt="Initial Scan" src="https://github.com/user-attachments/assets/3f55efa0-66c5-4fbc-bb9a-83fcccd0ad27" />
| High Severity Findings |
<img width="1162" height="560" alt="Number of High Severity Findings" src="https://github.com/user-attachments/assets/f07496a8-dab7-471d-9e42-8e715fdfb737" />
| Remediation Example | 
<img width="1060" height="671" alt="Screenshot 2026-04-21 184420" src="https://github.com/user-attachments/assets/1bba9f84-4c30-4f0b-b0f3-63d23880229f" />
<img width="1011" height="87" alt="Screenshot 2026-04-21 163055" src="https://github.com/user-attachments/assets/c9a2cc7e-094c-4969-88c5-9f6d4e38b8bc" />
<img width="1017" height="255" alt="Screenshot 2026-04-21 161147" src="https://github.com/user-attachments/assets/24364c40-a682-433a-8174-77b4fe163b5e" />
<img width="1005" height="669" alt="Screenshot 2026-04-21 161902" src="https://github.com/user-attachments/assets/feec0a14-b2f8-4c6e-a745-084ef562e3d4" />
<img width="1039" height="38" alt="Screenshot 2026-04-21 181952" src="https://github.com/user-attachments/assets/a1e9525f-2f9c-4099-ab90-36e048b1a0ad" />
| Final Scan Results | 
<img width="1290" height="887" alt="Final Scan" src="https://github.com/user-attachments/assets/8ce506a0-3126-49bb-aba1-47ce416e9068" />
<img width="1167" height="504" alt="Number of High Severities Reduced" src="https://github.com/user-attachments/assets/6e000855-2c33-481d-96fe-95c982e957ef" />


---

## 🧠 Lessons Learned

- STIG compliance requires both technical fixes and architectural decisions  
- Some controls cannot be safely applied post-installation  
- Misconfiguring boot security can impact system recoverability  
- Iterative scanning is critical for validation  
- Troubleshooting is a core part of compliance work  

---

## 🛠️ Skills Demonstrated

- Linux system hardening  
- STIG compliance implementation  
- OpenSCAP vulnerability scanning  
- Security remediation workflows  
- Root cause analysis and troubleshooting  
- Risk-based decision making  
