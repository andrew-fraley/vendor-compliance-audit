# Vendor Oversight Sheets — Combined Master Document

**Document Type:** IRS WISP Appendix — Third-Party Vendor Inventory  
**Scope:** All vendors handling NPI, PII, financial, or cardholder data  
**Review Schedule:** See individual vendor entries  
*Client-identifying information has been removed from this portfolio version.*

---

## Table of Contents

1. [TaxDome](#1-taxdome)
2. [QuickBooks Online (Intuit)](#2-quickbooks-online-intuit)
3. [Drake Software](#3-drake-software)
4. [Xero](#4-xero)
5. [Bitwarden](#5-bitwarden)
6. [Proton (Mail & VPN)](#6-proton-mail--vpn)
7. [Bitdefender](#7-bitdefender)

---

## 1. TaxDome

**Service Provided:** Practice management, client portal, payments  
**Data Types Involved:** NPI, PII, Financial, Cardholder (if payments enabled)

### Assurance & Certifications
- SOC 2 Type II (publicly attested)
- PCI DSS Level 2 (for payments module)
- Evidence: SOC 2 available on request; PCI AOC available from provider

### Security Controls
- MFA available (enforce via admin settings)
- Encryption in transit and at rest
- Client portal discourages use of unencrypted email for document exchange
- Incident response and breach notification documented in vendor agreements

### Contractual Safeguards
Service agreements cover data safeguarding obligations. Confirm incident notification clause is present in current agreement before signing or renewing.

### PCI DSS Considerations
Payment flow is provider-hosted (Stripe/TaxDome infrastructure). Firm is still classified as a merchant and must complete an applicable SAQ (typically SAQ A for fully hosted payment pages).

### Oversight & Review
- Access provisioning and deprovisioning managed through admin console
- Review active users annually; remove access for former staff immediately upon separation
- **Review Schedule: Annual**

---

## 2. QuickBooks Online (Intuit)

**Service Provided:** Accounting, QBO Payments  
**Data Types Involved:** NPI, PII, Financial, Cardholder (if QBO Payments enabled)

### Assurance & Certifications
- SOC 2 Type II
- ISO 27001
- PCI DSS attested for QBO Payments
- Intuit Security Trust Center: https://security.intuit.com

### Security Controls
- MFA enforced
- Encryption in transit and at rest
- Role-based access controls
- Logging and monitoring

### Contractual Safeguards
Intuit's terms of service require safeguarding of customer data. Security Trust Center documents available for review. Confirm current agreement version includes breach notification obligations.

### PCI DSS Considerations
Payment flow is provider-hosted. Merchant SAQ required regardless of hosted environment. SAQ A typically applies for firms using QBO's hosted payment pages without direct card handling.

### Oversight & Review
- Annual access review recommended; confirm active users match current staff
- **Review Schedule: Annual**

---

## 3. Drake Software

**Service Provided:** Tax preparation platform, secure portals, optional cloud hosting  
**Data Types Involved:** NPI, PII, Financial

### Assurance & Certifications
- Cloud hosting partner (Right Networks): SOC 1/2/3 Type II, PCI DSS at data center level
- MFA enforced across Drake products
- Attestation letters available from Right Networks upon request

### Security Controls
- Mandatory MFA across product suite
- Encryption in transit and at rest
- Secure portals for document transfer (reduces reliance on email)
- Incident notification procedures documented in support agreements

### Contractual Safeguards
Customer agreements outline confidentiality and data safeguarding obligations. Review current agreement to confirm breach notification language is present.

### PCI DSS Considerations
Not directly applicable unless third-party payment add-ons are integrated. If payments are added, reassess PCI scope accordingly.

### Oversight & Review
- Retain cloud hosting attestation letters from Right Networks as part of vendor file
- Request updated attestations annually during vendor review
- **Review Schedule: Annual**

---

## 4. Xero

**Service Provided:** Accounting platform  
**Data Types Involved:** NPI, PII, Financial

### Assurance & Certifications
- ISO/IEC 27001:2022 certified
- SOC 2 report available on request
- Xero Trust Center: https://www.xero.com/us/security/

### Security Controls
- MFA enforced
- Encryption in transit and at rest
- Role-based access controls
- Activity logging

### Contractual Safeguards
Data processing and safeguarding covered under Xero's terms of service and trust center policies. Review current agreement for breach notification obligations.

### PCI DSS Considerations
Not applicable unless the Xero payments module is enabled. If payments are activated, reassess PCI scope and applicable SAQ.

### Oversight & Review
- Request updated SOC 2 report or ISO certificate during annual review
- Confirm active user list matches current authorized staff
- **Review Schedule: Annual**

---

## 5. Bitwarden

**Service Provided:** Password manager  
**Data Types Involved:** Credentials (indirectly protects all NPI/PII systems)

### Assurance & Certifications
- ISO 27001 certified
- SOC 2 Type II and SOC 3 attested
- HIPAA aligned (signals strong compliance posture; not a regulatory requirement for this firm)
- Reports available at: https://bitwarden.com/compliance/

### Security Controls
- MFA and SSO support (enforce MFA for all vault users)
- Zero-knowledge encryption architecture (Bitwarden cannot access vault contents)
- Audit logging and reporting
- Self-hosting option available if required

### Contractual Safeguards
Bitwarden Business agreements include data safeguarding obligations. Review business subscription agreement for current terms.

### PCI DSS Considerations
Not applicable. Bitwarden does not process, store, or transmit cardholder data directly.

### Oversight & Review
- Higher review frequency warranted given the sensitive nature of credentials managed
- Review active vault users quarterly; remove access for separated staff immediately
- Confirm MFA is enforced for all users
- **Review Schedule: Quarterly (user access); Annual (full vendor review)**

---

## 6. Proton (Mail & VPN)

**Service Provided:** Encrypted email, VPN  
**Data Types Involved:** NPI, PII, communications

### Assurance & Certifications
- ISO 27001 (2024)
- SOC 2 Type II (2025)
- Proton Trust Center: https://proton.me/legal/transparency

### Security Controls
- End-to-end encryption for Proton-to-Proton email
- TLS encryption for external email (non-Proton recipients)
- MFA enforced
- VPN for secure connections on untrusted networks

### Contractual Safeguards
Proton Business agreements document security practices and obligations. Review current subscription agreement for safeguarding terms.

### PCI DSS Considerations
Not applicable.

### Oversight & Review
- Define and document the firm's VPN use policy: when is VPN required? (e.g., public Wi-Fi, travel, remote work outside the primary office)
- Annual review of active accounts
- **Review Schedule: Annual**

---

## 7. Bitdefender

**Service Provided:** Antivirus / Endpoint Detection and Response (EDR)  
**Data Types Involved:** System telemetry; indirectly protects all NPI/PII on covered endpoints

### Assurance & Certifications
- ISO 27001
- SOC 2 attestations available depending on product line
- Enterprise certifications published at: https://www.bitdefender.com/business/enterprise-products/

### Security Controls
- Endpoint protection agent deployed on all covered devices
- Tamper protection (prevents users from disabling agent)
- Logging and alerting to management console
- Regular signature and engine updates (confirm automatic updates are enabled)

### Contractual Safeguards
Vendor documentation includes confidentiality obligations and security standards. Review current agreement terms.

### PCI DSS Considerations
Not applicable. Bitdefender does not handle cardholder data directly; it protects the endpoints that may process it.

### Oversight & Review
- Confirm automatic signature/engine update routine is active
- Verify all firm-owned endpoints are covered (no gaps in agent deployment)
- **Review Schedule: Annual**

---

*Document last reviewed: [Date] | Next review due: [Date + 1 year]*  
*Maintained by: [Consultant / Firm Security Contact]*
