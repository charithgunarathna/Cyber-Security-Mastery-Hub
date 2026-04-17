# 🛡️ Module 01: Advanced Security Fundamentals

![Level](https://img.shields.io/badge/Level-Advanced-red)
![Focus](https://img.shields.io/badge/Focus-Theory_%26_Architecture-blue)

Welcome to the foundation of Enterprise Cyber Security. In this module, we move beyond basic definitions and explore enterprise-grade security architectures, threat modeling, and risk assessment methodologies.

---

## 🏛️ Enterprise Security Architecture

Modern cyber security relies on multiple layers of defense. The traditional "castle and moat" perimeter defense is no longer sufficient.

### 1. Defense in Depth (DiD)
A strategy that employs multiple security measures to protect the integrity of information. If one line of defense is compromised, additional layers exist as a backup.
* **Physical Controls:** Biometric scanners, security guards, CCTV.
* **Technical Controls:** Firewalls, Intrusion Prevention Systems (IPS), Endpoint Detection and Response (EDR).
* **Administrative Controls:** Security policies, user awareness training, incident response plans.

### 2. Zero Trust Architecture (ZTA)
The core principle of Zero Trust is **"Never Trust, Always Verify."** Unlike traditional networks where internal users are trusted by default, ZTA assumes the network is already compromised. Every access request must be strictly authenticated and authorized, regardless of whether it originates from inside or outside the network perimeter.

---

## 📊 Threat Modeling: The STRIDE Methodology

Developed by Microsoft, STRIDE is a framework used by security architects to identify structural vulnerabilities in an application or system design.

| Threat | Definition | Security Property Violated | Mitigation |
| :--- | :--- | :--- | :--- |
| **S**poofing | Pretending to be something or someone else. | Authentication | Multi-Factor Authentication (MFA), Digital Certificates. |
| **T**ampering | Modifying data or code maliciously. | Integrity | Hashing (SHA-256), Digital Signatures. |
| **R**epudiation | Claiming to have not performed an action. | Non-repudiation | Secure Logging, Audit Trails. |
| **I**nformation Disclosure | Exposing information to unauthorized users. | Confidentiality | AES-256 Encryption, Strict Access Controls. |
| **D**enial of Service | Denying or degrading service to users. | Availability | Load Balancing, Rate Limiting, Cloudflare. |
| **E**levation of Privilege | Gaining capabilities without proper authorization. | Authorization | Principle of Least Privilege (PoLP), Role-Based Access. |

---

## 📐 Risk Management Formula

To manage security effectively, you must quantify risk. The standard quantitative formula is:

> **ALE = SLE × ARO**

* **SLE (Single Loss Expectancy):** The financial loss from a single security incident.
* **ARO (Annualized Rate of Occurrence):** How many times this incident is expected to happen per year.
* **ALE (Annualized Loss Expectancy):** The total expected loss per year, which dictates your security budget.

---
➡️ **[Proceed to Module 02: Network Security](../02-Network-Security/README.md)**
