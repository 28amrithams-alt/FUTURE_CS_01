Cyber Security Internship – Task 1

Nmap Service Version Detection Scan

---

Project Overview

This project demonstrates a basic network reconnaissance and service version detection scan conducted using **Nmap** as part of my Cyber Security Internship Task 1.

The objective of this task was to:

* Identify open ports
* Detect running services
* Determine service versions
* Perform basic security analysis
* Document findings professionally

---

Target Information

* **Target Domain:** `testphp.vulnweb.com`
* **IP Address:** 44.228.249.3
* **Scan Type:** Service Version Detection (`-sV`)
* **Tool Used:** Nmap 7.98
* **Operating System:** Windows

> Note: The target is an intentionally vulnerable test website used for security learning purposes.

---

Tools Used

* **Nmap** – Network scanning and service detection tool
* Command Prompt (Windows)

---

Scan Command Used

Basic scan:

```
nmap testphp.vulnweb.com
```

Service version detection scan:

```
nmap -sV testphp.vulnweb.com
```

---

Scan Results Summary

| Port | Protocol | Service | Version      | Status |
| ---- | -------- | ------- | ------------ | ------ |
| 21   | TCP      | FTP     | Not detected | Open   |
| 80   | TCP      | HTTP    | nginx 1.19.0 | Open   |
| 554  | TCP      | RTSP    | Not detected | Open   |
| 1723 | TCP      | PPTP    | Not detected | Open   |

---

Key Observations

* The web server is running **nginx 1.19.0**
* FTP service is enabled
* PPTP VPN service is active (outdated protocol)
* Majority of other ports are filtered by firewall
* Multiple exposed services increase attack surface

---

Security Considerations

* Outdated software versions should be verified and updated
* FTP and PPTP protocols are considered insecure if not properly configured
* Regular vulnerability assessments are recommended
* Firewall filtering indicates some defensive configuration

---

Scan Limitations

* No authentication testing performed
* No exploitation attempted
* No vulnerability database correlation conducted
* Results limited to service detection only

 Conclusion

This task demonstrates foundational network reconnaissance skills using Nmap. The scan successfully identified active services and provided insights into potential security considerations.

This project reflects my practical understanding of basic cybersecurity assessment techniques as a Computer Science student.

---
