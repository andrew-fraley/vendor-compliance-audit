# vendor-compliance-audit
This is a vendor oversight that accompanies IRS Written Information Security Plan development (or other similar compliance based information security plans). It works as a complimentary deliverable document that acts as a vendor compliance audit, do the third-party vendors (SaaS, software, etc.) adhere to the necessary regulatory requirements. 

# Vendor Compliance Audit — IRS WISP Support

**Type:** Real-world consulting deliverable  
**Context:** Information security engagement for a small accounting firm  
**Scope:** Third-party vendor oversight documentation developed as a companion to the client's IRS Written Information Security Plan (WISP)

---

## What This Is

This repository contains the vendor oversight framework I developed for a client undergoing an IRS WISP compliance engagement. The deliverable inventories every third-party platform the firm uses, maps the data types each vendor touches, documents security certifications and contractual safeguards, and establishes a repeatable review cadence.

The output is a structured set of **Vendor Oversight Sheets** — one per vendor — plus a combined master sheet suitable for inclusion in the client's WISP appendix or provided to auditors on request.

Vendor names and platform details are real. Client-identifying information has been removed.

---

## Why It Matters

The IRS Safeguards Rule (FTC Safeguards Rule / GLBA) requires tax professionals to maintain a Written Information Security Plan that addresses how third-party service providers are selected, monitored, and held accountable for protecting Nonpublic Personal Information (NPI).

Most small firms have no formal vendor inventory. They use a dozen SaaS tools — practice management, accounting, email, password managers, endpoint protection — without any documented understanding of:

- What data each vendor holds
- Whether the vendor has verifiable security certifications (SOC 2, ISO 27001, PCI DSS)
- Whether the contractual relationship obligates the vendor to safeguard that data and notify the firm in the event of a breach
- Who at the firm has access, and whether that access is reviewed regularly

This work closes that gap.

---

## What It Demonstrates

- **Regulatory fluency** — Applied understanding of IRS WISP requirements, FTC Safeguards Rule, and PCI DSS scoping for small merchants
- **Vendor risk assessment** — Ability to evaluate SaaS vendors across certifications, controls, contractual posture, and data exposure
- **Client-ready documentation** — Structured, plain-language deliverables designed for practitioners, not security engineers
- **Consulting judgment** — Knowing what to include, what to flag, and how to frame findings for a non-technical audience
- **Repeatable framework** — The oversight sheet structure is reusable across clients and auditable over time

---

## Repository Structure

```
vendor-compliance-audit/
├── README.md                  
├── overview.md                
└── examples/
    ├── vendor-oversight-combined.md   
    └── vendors/
        ├── taxdome.md
        ├── quickbooks-online.md
        ├── drake-software.md
        ├── xero.md
        ├── bitwarden.md
        ├── proton.md
        └── bitdefender.md
```

---

## Engagement Context

This vendor audit was developed as part of a broader information security consulting engagement that included:

- IRS WISP drafting and review
- Risk assessment
- Incident response plan development
- Employee security policy templates

The vendor oversight sheets were designed to plug directly into the WISP as a living appendix, reviewed and updated routinely as specified.
