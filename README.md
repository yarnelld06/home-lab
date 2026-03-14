# Home Lab — Active Directory & Cybersecurity Environment

**Yarnell Dixon Jr**  
CompTIA A+ | CompTIA Security+  
B.S. Cybersecurity — Western Governors University  
[Notion Portfolio](https://veiled-paneer-e13.notion.site/Yarnell-Dixon-IT-Support-Portfolio-31880d4604ca8020ba61f88c5b74e8ee) | [LinkedIn](https://linkedin.com/in/yarnell-dixon-jr)

---

## About This Lab

I built this home lab from scratch to get real hands-on experience outside of the classroom. Everything here runs in VirtualBox on my personal machine, and it simulates the kind of environment you'd find in an actual enterprise setting. My goal with this lab is to develop practical IT and cybersecurity skills that go beyond certification studying, and to document my progress as I work toward a career in cybersecurity and penetration testing.

---

## Environment Overview

| Component | Details |
|---|---|
| Virtualization | Oracle VirtualBox |
| Domain Controller | DC01, Windows Server 2022 |
| Client Machine | CLIENT01, Windows 10 |
| Linux Machine | Ubuntu VM |
| Domain | corp.local |
| IP Scheme | 192.168.56.x |

---

## Labs Completed

### 1. Password Reset / Account Lockout Troubleshooting
I simulated a domain user locked out of their workstation with an incorrect password error. I tracked down the account in Active Directory Users and Computers, verified the account status, reset the password, and enforced a change at next logon. Confirmed the user could successfully log back into CLIENT01.

**Skills:** AD user management, account lockout resolution, domain connectivity troubleshooting

---

### 2. Shared Folder Access Troubleshooting
Set up a company file share on DC01 with NTFS permissions tied to a security group. Added a test user to the group through Active Directory, mapped the network drive on CLIENT01, and verified the user had proper access to the shared files.

**Skills:** Windows file sharing, NTFS permissions, security group membership, network drive mapping

---

### 3. Group Policy Management — Domain Security Controls
Created a Group Policy Object called Company Security Policy and linked it to the corp.local domain. Configured password complexity requirements, set a maximum password age of 60 days, and restricted standard users from accessing the Control Panel. Used gpresult /r on CLIENT01 to confirm the policy was applied correctly.

**Skills:** GPO creation and deployment, password policy enforcement, user environment restrictions, gpresult verification

---

### 4. DNS Resolution Failure Troubleshooting
Diagnosed a DNS misconfiguration that was preventing a workstation from resolving domain names. Ran nslookup to confirm the failure, used ipconfig /all to find the incorrect DNS server address, manually updated the network adapter settings to point to the correct internal DNS server at 192.168.56.10, and flushed the cache with ipconfig /flushdns. Confirmed resolution was restored.

**Skills:** DNS troubleshooting, command line networking tools, network adapter configuration

---

### 5. Remote Support Simulation
Used Remote Desktop to connect to CLIENT01 and diagnose a missing mapped network drive. Verified network connectivity with ping, confirmed the drive was missing from This PC, and remapped it to the shared folder on the domain controller. Resolved without needing to be physically at the machine.

**Skills:** Remote Desktop Protocol, network drive management, remote troubleshooting workflow

---

### 6. Help Desk Ticket Workflow Simulation
Documented a full ticket lifecycle from open to close. Ticket HD-1024 came in from the Accounting department reporting they couldn't access the shared company drive. I investigated remotely, identified the issue, remapped the drive, confirmed access was restored, and closed the ticket with full documentation.

**Skills:** Ticket documentation, incident response workflow, help desk communication procedures

---

## Tools and Technologies

- Windows Server 2022 with Active Directory Domain Services
- Group Policy Management Console (GPMC)
- Active Directory Users and Computers (ADUC)
- Remote Desktop Protocol (RDP)
- Command line tools including nslookup, ipconfig, ping, and gpresult
- Oracle VirtualBox
- Ubuntu Linux

---

## Currently Building

- [ ] Nmap Network Reconnaissance Lab
- [ ] Linux Fundamentals Lab
- [ ] Splunk Log Analysis Lab
- [ ] Azure Active Directory Lab

---

This lab is something I actively work on and expand as I build toward a career in cybersecurity. If you want to see the full write-ups with screenshots for each lab, check out my Notion portfolio linked above.
