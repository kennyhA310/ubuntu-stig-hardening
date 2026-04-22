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
<img width="1007" height="148" alt="Remediation Example" src="https://github.com/user-attachments/assets/6490fede-f89a-40d5-aecb-400ac51110b7" />
| Final Scan Results | 
<img width="1290" height="887" alt="Final Scan" src="https://github.com/user-attachments/assets/8ce506a0-3126-49bb-aba1-47ce416e9068" />

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
