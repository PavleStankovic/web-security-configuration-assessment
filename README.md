# 🔐 Web Security Configuration Assessment — Public Case Study

**Author:** Pavle Stankovic  
**Date:** October 17, 2025  
**Location:** Serbia  
**Age:** 17  
**License:** CC BY-NC-ND 4.0  

---

## 🧭 Overview

This public case study analyzes the **SSL/TLS configuration** and **HTTP security headers** of a live production domain (`mundo-gol.com`), performed with explicit permission from the owner.  
The goal was to identify weaknesses, test against **modern web security standards**, and document the remediation process for educational purposes.

The assessment demonstrates professional-grade methodology using **OWASP**, **NIST**, and **PCI DSS v4.0** frameworks while keeping the scope non-intrusive and ethical.

---

## ⚙️ Scope & Methodology

**Scope:**  
- SSL/TLS configuration  
- Certificate validation and transparency  
- Supported protocols and cipher suites  
- HTTP security headers  

**Out of Scope:**  
- Internal network  
- Application logic  
- Authentication or intrusive testing  

**Tools Used:**  
- `sslyze` (TLS scanning)  
- `nmap` (port/service enumeration)  
- `curl`, `openssl` (handshake and header analysis)  
- Browser DevTools  

**Methodology References:**  
- NIST SP 800-115  
- OWASP Testing Guide v5  

---

## 🔎 Key Findings

| Issue | Severity | Recommendation |
|-------|-----------|----------------|
| Missing HSTS header | Medium | Add Strict-Transport-Security |
| Missing CSP header | Medium | Define restrictive Content-Security-Policy |
| Missing X-Frame-Options | Low | Add DENY directive |
| Missing X-Content-Type-Options | Low | Set to nosniff |
| OCSP Stapling not enabled | Low | Enable stapling in Apache/Nginx |
| Low SCT count (2) | Low | Reissue certificate with ≥3 SCTs |

✅ **TLS 1.2/1.3** supported  
✅ **Forward Secrecy** enabled  
✅ **Modern cipher suites** (AES-GCM, ChaCha20-Poly1305)  
✅ **No critical vulnerabilities** (e.g., Heartbleed, ROBOT)

---

## 🛠️ Recommended Fixes

Detailed Apache and Nginx configuration examples are included in the report PDF.  
Fixes prioritize **A+ SSL Labs rating** and compliance with **OWASP A05:2021 (Security Misconfiguration)**.

---

## 📊 Compliance Mapping

| Standard | Requirement | Status |
|-----------|-------------|--------|
| OWASP Top 10:2021 | A05: Security Misconfiguration | Addressed |
| NIST SP 800-52 Rev. 2 | TLS 1.3 priority, cipher strength | Compliant |
| PCI DSS v4.0 | Requirement 4: Secure transmission | Compliant |
| GDPR/HIPAA | Encryption for data protection | Compliant |

---

## 🧠 About the Author

👋 I’m **Pavle Stankovic**, a **17-year-old high school student from Serbia** passionate about **cybersecurity, web infrastructure, and network defense**.  
I enjoy learning through ethical testing, secure configuration, and documenting real-world assessments.  

- 🌍 Location: Serbia  
- 🎓 Student | Cybersecurity Enthusiast  
- 💡 Focus: TLS, HTTP security, Linux hardening, OWASP practices  
- 📧 Email: [stankovic.pavle16@gmail.com](mailto:stankovic.pavle16@gmail.com)  
- 💼 LinkedIn: [linkedin.com/in/pavle-stanković-914694386](https://linkedin.com/in/pavle-stanković-914694386)

---

## 📘 License

This work is shared under **[CC BY-NC-ND 4.0](https://creativecommons.org/licenses/by-nc-nd/4.0/)**  
You’re free to read and share it for educational purposes, but please **credit the author** and **don’t modify or use commercially**.

---

## 🧩 Files

- [`Web Security Configuration Assessment.pdf`](./Web%20Security%20Configuration%20Assessment.pdf) — Full detailed report  
- `README.md` — Summary and highlights  

---

Full detailed technical report available in the PDF below.

---

### ⭐ If you found this useful
Give this repo a star 🌟 and connect with me — I’m always learning and open to collaboration!

