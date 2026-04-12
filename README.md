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
## Information Security Risk Management Project

**`Banking & Financial Services`** &nbsp;|&nbsp; **`Leanrning Goal`** &nbsp;|&nbsp; **`Simulated Environment`**

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
├── 📂 logos/                                             # Project logos (SANS, NCA, New Nile Bank)
│
├── 📂 Policies/                                          # Governance & policy documents
│
├── 📄 New-Nile-Bank-Asset-Inventory.xlsx                 # IT asset inventory — 25 assets across Tier 1/2/3
├── 📄 NCB-PCI-DSS-Checklist.xlsx                         # PCI DSS v4.0 — 68-control compliance checklist
├── 📄 New-Nile-Risk-Register1.xlsx                       # Cybersecurity risk register — threats, vulnerabilities, residual risks
├── 📄 Risk-Treatment-Plan-Full.xlsx                      # Risk treatment plan — controls mapped to NIST CSF / ISO 27002
├── 📄 Stakeholder_Register_Template_Excel_ProjectM.xlsx  # Stakeholder register — 27 internal & external stakeholders
├── 📄 POLICY_Cybersecurity_Risk_Management_Template.docx # Cybersecurity risk management policy (CISO-approved)
├── 📄 Scope.docx                                         # ISMS scope document (ISO 27001 §4.3)
└── 📄 README.md
```

---

## 🛠️ Frameworks & Regulations Applied

| Framework / Regulation | Domain | Application in This Project |
|---|---|---|
| **ISO/IEC 27005:2022** | Risk Management | Core methodology for risk identification, analysis, evaluation, and treatment — explicitly referenced in the Risk Treatment Plan and Cybersecurity Risk Policy |
| **ISO 31000** | Risk Management Principles | Underpins the overall risk management approach; referenced alongside ISO 27005 in the Cybersecurity Risk Policy |
| **CBE Cybersecurity Framework** | National Banking Regulation | Mandatory requirement embedded in policy — all cybersecurity risk management procedures must align with CBE directives |
| **PCI DSS v4.0** | Payment Card Security | Full 12-requirement compliance checklist covering all NCB ATM, Base24, and card payment environments |
| **SWIFT CSP (CSCF v2024)** | Interbank Messaging Security | CSCF v2024 mandatory controls applied to SWIFT SAG — including payment transaction signing, anomaly detection, and MFA on operator accounts (RR-09) |
| **NIST** | Control Guidance | Referenced in the Cybersecurity Risk Policy as a supplementary international guideline alongside ISO 27005 and ISO 31000 |

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

<sub>© 2026 Samara Risha/sub>

</div>
