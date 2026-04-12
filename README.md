<div align="center">

<!-- ═══════════════════════════ LOGO ROW ═══════════════════════════ -->
<table border="0" cellspacing="0" cellpadding="0">
  <tr>
    <td align="center" width="330">
      <!-- Replace src with your first partner/framework logo -->
      <img src="https://github.com/samararisha/Risk-Management-Project-Banking-Industry/blob/4dc8244d74cfbb342cf9cf772ae1e8e6e85fb079/logos/SANS-LOGO.png" alt="SANS" width="300"/><br/>
      <sub><b>SANS</b></sub>
    </td>
    <td align="center" width="330">
      <!-- ── CENTER: New Nile Bank ── -->
      <img src="https://github.com/samararisha/Risk-Management-Project-Banking-Industry/blob/d15b1c9733312df09c0393c7683028a26d332d32/Logo.jpeg" alt="New Nile Bank" width="220"/><br/>
      <sup><i>Bank</i></sup>
    </td>
    <td align="center" width="280">
      <!-- Replace src with your second partner/framework logo -->
      <img src="https://github.com/samararisha/Risk-Management-Project-Banking-Industry/blob/22291ecb6bafaccc5bb8f95fbadd6c6e586004c9/logos/NCA-Logo.jpeg" alt="NCA" /><br/>
      <sub><b>NCA</b></sub>
    </td>
  </tr>
</table>

<br/>

# 🏦 New Nile Bank
## GRC & Information Security Risk Management Project

**`Banking & Financial Services`** &nbsp;|&nbsp; **`Egypt 🇪🇬`** &nbsp;|&nbsp; **`Simulated Environment`**

<br/>

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=flat-square)](https://opensource.org/licenses/MIT)
[![ISO 27001](https://img.shields.io/badge/ISO%2FIEC-27001%3A2022-0057A8?style=flat-square)](https://www.iso.org/standard/27001)
[![ISO 27005](https://img.shields.io/badge/ISO%2FIEC-27005%3A2022-004A99?style=flat-square)](https://www.iso.org/standard/80585.html)
[![PCI DSS](https://img.shields.io/badge/PCI%20DSS-v4.0-003087?style=flat-square)](https://www.pcisecuritystandards.org/)
[![CBE](https://img.shields.io/badge/CBE-Cybersecurity%20Framework-006633?style=flat-square)](https://www.cbe.org.eg/)
[![Egypt PDPL](https://img.shields.io/badge/Egypt%20Law-No.151%2F2020-CC0000?style=flat-square)](https://itida.gov.eg/)
[![Status](https://img.shields.io/badge/Status-Active%20Development-brightgreen?style=flat-square)]()

---

</div>

## 📖 Project Overview

> **New Nile Bank** is a simulated mid-sized Egyptian commercial bank — the setting for a full-lifecycle **Information Security Risk Management (ISRM)** portfolio. This project demonstrates end-to-end GRC practice: from scoping and asset inventory through threat modelling, risk assessment, treatment planning, and executive reporting — aligned to both international standards and local **Central Bank of Egypt (CBE)** regulatory requirements.

The bank operates **47 branches**, processes **2.3 million transactions/day**, holds **EGP 85 billion** in assets, and serves **1.4 million retail customers** — complex enough to exercise every risk domain from PCI DSS card data to SWIFT messaging security to cloud migration risk.

---

## 🏗️ Architecture at a Glance

```
┌─────────────────────────── Internet-Facing Zone ──────────────────────────────┐
│   Mobile App (AWS)    │   Online Banking (Azure)   │   Open Banking API (REST) │
└────────────────────────────────────┬──────────────────────────────────────────┘
                                     │
                    ┌────────────────▼─────────────────┐
                    │   DMZ — WAF / Reverse Proxy       │
                    │        (Fortinet FortiGate)        │
                    └────────────────┬─────────────────┘
                                     │
┌────────────────────── Internal Network — Core Banking Zone ───────────────────┐
│  T24 Core Banking  │  Oracle GL  │  AML (Actimize)  │  Customer DB (Oracle)   │
│  SWIFT SAG (HSM)   │  Base24 PCI │  AD / Entra ID   │  SIEM (MS Sentinel)     │
└───────────────────────────────────────────────────────────────────────────────┘
```

---

## 📁 Repository Structure

```
New-Nile-Bank-GRC/
│
├── 📂 01_Methodology/
│   ├── Risk_Assessment_Criteria.xlsx       # Likelihood × Impact scoring matrix
│   └── Risk_Scoring_Methodology.md         # Qualitative & quantitative approach
│
├── 📂 02_Asset_Inventory/
│   ├── IT_Asset_Inventory.xlsx             # 25 assets across Tier 1/2/3
│   └── Crown_Jewels_Classification.md      # Critical asset justification
│
├── 📂 03_Risk_Register/
│   ├── Cybersecurity_Risk_Register.xlsx    # Threats, vulnerabilities, residual risks
│   └── Threat_Actor_Profiles.md            # APT38/Lazarus, ransomware groups, insiders
│
├── 📂 04_Treatment_Plan/
│   ├── Risk_Treatment_Plan.xlsx            # Controls mapped to NIST CSF / ISO 27002
│   └── PCI_DSS_v4_Checklist.xlsx          # 68-control compliance checklist
│
├── 📂 05_Stakeholders/
│   ├── Stakeholder_Register.xlsx           # 27 internal & external stakeholders
│   └── Communication_Plan.md              # Engagement strategy per stakeholder group
│
├── 📂 06_Governance/
│   ├── ISMS_Scope_Document.docx            # ISO 27001 §4.3 scoping document
│   └── Cybersecurity_Risk_Policy.docx      # Risk management policy (CISO-approved)
│
└── 📂 07_Reports/
    ├── Executive_Summary.pdf               # Board-level risk overview
    └── Risk_Heat_Map.xlsx                  # Visual risk matrix (5×5)
```

---

## 🛠️ Frameworks & Regulations Applied

| Framework / Regulation | Domain | Application in This Project |
|---|---|---|
| **ISO/IEC 27001:2022** | ISMS Governance | ISMS scope, policy structure, control objectives |
| **ISO/IEC 27005:2022** | Risk Management | Risk identification, analysis, evaluation methodology |
| **CBE Cybersecurity Framework** | National Banking | Mandatory controls for Egyptian banks, maturity levels |
| **PCI DSS v4.0** | Payment Card Security | 68-control checklist for ATM/card/payment environment |
| **SWIFT CSP (CSCF v2024)** | Interbank Messaging | SWIFT Alliance Gateway security controls |
| **Egypt Law No. 151/2020** | Data Privacy | Personal data protection, 72-hr breach notification, DPO |
| **Basel III / BCBS 239** | Operational Risk | Risk data aggregation, board-level risk reporting |
| **NIST CSF 2.0** | Control Mapping | Identify → Protect → Detect → Respond → Recover |

---

## 🎯 Key Risk Scenarios Covered

| # | Scenario | Threat Actor | Risk Level |
|---|---|---|---|
| 1 | **SWIFT Fraud / BEC Wire Transfer** | APT38 / Lazarus Group | 🔴 Critical |
| 2 | **Ransomware — CBS/GL Encryption** | Regional Cybercrime (RaaS) | 🔴 Critical |
| 3 | **Mobile Banking Account Takeover** | Opportunistic Fraudsters | 🟠 High |
| 4 | **Insider Threat — Privileged DB Access** | Malicious Insider | 🟠 High |
| 5 | **ATM Jackpotting / Skimming** | Criminal Groups | 🟡 Medium |

---

## 📊 Deliverables Summary

| Deliverable | Tool | Status |
|---|---|---|
| IT Asset Inventory (25 assets) | Excel | ✅ Complete |
| Stakeholder Register (27 stakeholders) | Excel | ✅ Complete |
| Cybersecurity Risk Register | Excel | ✅ Complete |
| ISMS Scope Document | Word | ✅ Complete |
| Cybersecurity Risk Policy | Word | ✅ Complete |
| PCI DSS v4.0 Checklist (68 controls) | Excel | ✅ Complete |
| Risk Heat Map | Excel | 🔄 In Progress |
| Executive Summary Report | PDF | 🔄 In Progress |

---

## 👤 Author

<div align="center">

**Samara Risha**
*Final-year Computer Science Student · Cybersecurity & GRC Enthusiast*

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=flat-square&logo=linkedin)](https://linkedin.com)
[![GitHub](https://img.shields.io/badge/GitHub-Follow-181717?style=flat-square&logo=github)](https://github.com/samararisha)

</div>

---

<div align="center">

**⚠️ Disclaimer**

<sub>This project is created entirely for educational and portfolio purposes.<br/>
New Nile Bank is a fictional entity. All data, systems, and scenarios are fully simulated.<br/>
No real customer data, financial information, or proprietary systems are involved.</sub>

<br/>

<sub>© 2026 Samara Risha · MIT License</sub>

</div>
