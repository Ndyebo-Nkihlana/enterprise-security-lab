# Web Application Security Lab (GNS3 + OWASP)

## Overview
This project demonstrates the setup and testing of a simulated enterprise network used for web application security testing.

The lab includes:
- GNS3 network simulation
- Windows Server 2016
- Kali Linux attacker machine
- OWASP Broken Web Applications

## Skills Demonstrated
- Virtual lab design
- Network configuration
- DHCP configuration
- Web application penetration testing concepts
- SQL Injection testing
- Brute force authentication attacks
- Password recovery techniques

## Lab Architecture
See `/architecture` folder.

## Lab Setup
Step-by-step setup documented in `/setup`.

## Security Tests Performed
- Brute Force Attack
- SQL Injection
- Database Enumeration
- Password Hash Manipulation

## Tools Used
- Kali Linux
- Burp Suite Community Edition
- SQLMap
- GNS3
- OWASP Broken Web Apps
- chntpw

## Lab Environment

![Lab Screenshot](screenshots/1.png)
## Disclaimer
This project was conducted in an isolated lab environment for educational purposes only.

# Section A – Lab Environment Setup

## Task 1 – Virtual Lab Setup

A virtual penetration testing environment was created using GNS3 and multiple virtual machines.  
The OWASP Broken Web Applications VM was deployed as the vulnerable target, while Kali Linux served as the attacker machine.

Windows Server 2016 was installed and configured to provide DHCP and internal network services.

### Screenshots
![Step 1](screenshots/1.png)
![Step 2](screenshots/2.png)
![Step 3](screenshots/3.png)
![Step 4](screenshots/4.png)
![Step 5](screenshots/5.png)
![Step 6](screenshots/6.png)
![Step 7](screenshots/7.png)
![Step 8](screenshots/8.png)
![Step 9](screenshots/9.png)
![Step 10](screenshots/10.png)
![Step 11](screenshots/11.png)

---

## Task 2 – Network Configuration

A GNS3 project named **WebTest-Lab** was created to simulate an enterprise network topology.  
Kali Linux, OWASP Broken Web Apps, Windows Server 2016, a Cisco 3745 router, and an Ethernet switch were connected to form the lab environment.

### Screenshots
![Step 1](screenshots/12.png)
![Step 2](screenshots/13.png)
![Step 3](screenshots/14.png)

---

## Task 3 – DHCP Configuration

Network interfaces were configured to allow communication between hosts.  
The Cisco 3745 router was configured as a DHCP server to dynamically assign IP addresses within the Kali Linux network segment.

Successful IP allocation confirmed correct configuration.

### Screenshots
![Step 1](screenshots/15.png)
![Step 2](screenshots/16.png)

---

# Section B – Penetration Test Scenario

## Task 4 – Grey Box Penetration Test Scenario

A grey-box penetration testing scenario simulated an internal security assessment of the Car Care ConnoisseurX (CCCX) environment.

The objective was to identify vulnerabilities using limited prior knowledge of the system.

### Screenshots
![Step 1](screenshots/17.png)
![Step 2](screenshots/18.png)

---

# Section C – Web Application Attacks

## Task 5 – Brute Force Attack

Burp Suite Community Edition was used to perform a brute-force attack against the Bricks Login 3 application.

Default username and password wordlists were used, resulting in successful credential discovery and demonstrating weak authentication controls.

### Screenshots
![Step 1](screenshots/19.png)
![Step 2](screenshots/20.png)
![Step 3](screenshots/21.png)
![Step 4](screenshots/22.png)
![Step 5](screenshots/23.png)
![Step 6](screenshots/24.png)
![Step 7](screenshots/25.png)
![Step 8](screenshots/26.png)

---

## Task 6 – SQL Injection and Database Extraction

A SQL injection attack was conducted against the Mutillidae login application.

Burp Suite captured the login request, which was supplied to SQLMap for automated database enumeration and credential extraction.

Sensitive data retrieval confirmed insufficient input validation.

### Screenshots
![Step 1](screenshots/27.png)
![Step 2](screenshots/28.png)
![Step 3](screenshots/29.png)
![Step 4](screenshots/30.png)
![Step 5](screenshots/31.png)
![Step 6](screenshots/32.png)
![Step 7](screenshots/33.png)
![Step 8](screenshots/34.png)
![Step 9](screenshots/35.png)

---

# Section D – Post Exploitation

## Task 7 – Password Cracking

Post-exploitation testing was performed using the **chntpw** utility to reset the Windows Server 2016 Administrator password.

Offline registry hive modification enabled successful administrator login, demonstrating weak credential protection.

### Screenshots
![Step 1](screenshots/36.png)
![Step 2](screenshots/37.png)
![Step 3](screenshots/38.png)
![Step 4](screenshots/39.png)
![Step 5](screenshots/40.png)
![Step 6](screenshots/41.png)
![Step 7](screenshots/42.png)
![Step 8](screenshots/43.png)
![Step 9](screenshots/44.png)

# Security Recommendations

- Implement account lockout policies.
- Enforce strong password complexity requirements.
- Use parameterized queries to prevent SQL injection.
- Apply least-privilege access controls.
- Enable multi-factor authentication for privileged accounts.
- Conduct regular vulnerability assessments.

---

## Full Penetration Test Report

The complete technical report can be viewed below:

[View Full Report](report/Penetration_Test_Report.pdf)
