# Vendor Oversight Framework — Methodology & Usage

## Purpose

This document explains how the vendor oversight sheets in this repository were built, what each section means, and how a firm or consultant should use and maintain them over time.

These sheets are designed to satisfy the third-party oversight requirements of the IRS Written Information Security Plan (WISP) under the FTC Safeguards Rule (16 CFR Part 314), which applies to tax professionals and other financial service providers handling sensitive client data (NPI, PII).

---

## Regulatory Background

The FTC Safeguards Rule requires covered firms to:

- Select and retain service providers that maintain appropriate safeguards for customer information
- Require service providers by contract to implement and maintain appropriate safeguards
- Monitor service providers to ensure they are meeting those obligations

The IRS operationalizes this in WISP guidance by requiring practitioners to document which third-party vendors handle taxpayer data and what safeguards those vendors have in place.

This framework provides a structured, auditable way to meet that obligation.

---

## How Vendors Were Selected for Review

Every platform that touches, stores, transmits, or processes any of the following data types was included:

| Data Type | Description |
|---|---|
| NPI | Nonpublic Personal Information (taxpayer data, SSNs, financial records) |
| PII | Personally Identifiable Information more broadly (names, addresses, contact info) |
| Financial | Bank account data, transaction records, invoicing data |
| Cardholder | Payment card data subject to PCI DSS |
| Credentials | Passwords and authentication data (managed indirectly through password managers) |
| System Telemetry | Device/endpoint data captured by security tools |


---

## Vendor Sheet Structure

Each vendor sheet follows the same format for consistency and auditability.

### Service Provided
A plain-language description of what the vendor does and how the firm uses it.

### Data Types Involved
Which of the data categories above the vendor handles. This drives the risk level and determines whether PCI DSS scoping applies.

### Assurance & Certifications
Third-party verified security attestations the vendor holds. Priority certifications:

- **SOC 2 Type II** — Audited controls over security, availability, confidentiality. Type II covers a period of time (vs. point-in-time Type I), making it more meaningful.
- **ISO/IEC 27001** — International standard for information security management systems.
- **PCI DSS** — Payment Card Industry Data Security Standard. Relevant when the vendor processes, stores, or transmits cardholder data.
- **HIPAA alignment** — Not required for tax practices but noted where vendors publish HIPAA-aligned controls (Bitwarden), as it signals a strong compliance posture.

Where certifications are available on request (vs. public), this is noted. Firms should request and retain evidence during annual reviews.

### Security Controls
Key technical and operational controls the vendor maintains. Reviewed against what the Safeguards Rule and IRS WISP guidance identify as expected controls:

- Multi-factor authentication (MFA)
- Encryption in transit and at rest
- Access controls (role-based, least privilege)
- Logging and monitoring
- Incident response and breach notification

### Contractual Safeguards
Whether the firm's agreement with the vendor (terms of service, business agreement) obligates the vendor to safeguard data and notify the firm of a breach. Weakness here is flagged for follow-up.

### PCI DSS Considerations
Applicable only to vendors in the payment flow. Notes whether the payment environment is provider-hosted (reducing the firm's PCI scope) and identifies which SAQ (Self-Assessment Questionnaire) the merchant may be required to complete.

### Oversight & Review
Specifies the recommended review schedule for each vendor (annual vs. quarterly for higher-risk platforms like password managers) and any specific tasks to complete during review (access provisioning audit, certificate renewal, attestation retrieval).

---

## Review Schedule

| Schedule | Vendors |
|---|---|
| Quarterly | Bitwarden (vault user access review) |
| Annual | All others |

Annual reviews should confirm:
1. Vendor certifications are current (request updated SOC 2 or ISO cert)
2. No significant changes to vendor security posture or data handling
3. User access has been reviewed and deprovisioned where appropriate
4. Contractual terms still include required safeguarding and breach notification clauses

---

## Maintaining the Sheets

These sheets are living documents. They should be updated when:

- A new vendor is onboarded
- An existing vendor is offboarded
- A vendor's certification status changes
- The firm's use of a vendor changes (e.g., enabling a payments module that adds PCI scope)
- A vendor experiences a breach or issues a security notice

Version and date each update. Retain prior versions for audit purposes.

---

## A Note on Merchant PCI Responsibility

Several vendors in this engagement offer integrated payments (TaxDome, QuickBooks Online). Even when the payment environment is provider-hosted (meaning cardholder data flows through the vendor's infrastructure, not the firm's), the firm is still considered a merchant under PCI DSS and must complete an appropriate SAQ.

For most small firms using fully hosted payment pages, **SAQ A** applies, a short self-assessment. This is distinct from the vendor's own PCI DSS certification. Both obligations exist independently.

---

## How to Use This Framework for a New Client

1. Inventory all platforms the client uses that touch NPI, PII, financial, or cardholder data
2. For each vendor, complete a sheet using the template structure in this repository
3. Research certifications via the vendor's trust center, security page, or direct request
4. Review the client's existing agreements with each vendor for safeguarding and breach notification language
5. Flag gaps (missing MFA enforcement, no contractual safeguarding clause, no available SOC 2)
6. Incorporate the completed sheets as an appendix to the client's WISP
7. Schedule the review routine into the client's security calendar
