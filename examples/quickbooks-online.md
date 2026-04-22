# Vendor Oversight Sheet — QuickBooks Online (Intuit)

**Service Provided:** Accounting, QBO Payments  
**Data Types Involved:** NPI, PII, Financial, Cardholder (if QBO Payments enabled)  
**Review Schedule:** Annual

---

## Assurance & Certifications

| Certification | Status | Evidence |
|---|---|---|
| SOC 2 Type II | Attested | Intuit Security Trust Center |
| ISO 27001 | Certified | Intuit Security Trust Center |
| PCI DSS | Attested (QBO Payments) | Available via Intuit |

**Trust Center:** https://security.intuit.com

## Security Controls

| Control | Status | Notes |
|---|---|---|
| MFA | ✓ Enforced | |
| Encryption in transit | ✓ | |
| Encryption at rest | ✓ | |
| Role-based access controls | ✓ | Assign minimum necessary access per user |
| Logging & monitoring | ✓ | |
| Breach notification | ✓ | Confirm clause in current agreement |

## Contractual Safeguards

Intuit's terms of service include data safeguarding requirements. Documentation available via the Security Trust Center. Confirm the current agreement version explicitly includes breach notification obligations and review any Data Processing Addendum (DPA) if applicable.

## PCI DSS Considerations

- Payment flow is **provider-hosted** (QBO Payments / Intuit infrastructure)
- Firm remains a **merchant** for PCI DSS purposes regardless of hosted environment
- For hosted payment pages with no direct card handling: **SAQ A** typically applies
- If the firm accesses cardholder data in any other form, reassess applicable SAQ type

## Oversight & Review Checklist

**Annual Review Tasks:**
- [ ] Confirm SOC 2 and ISO 27001 certifications are current via Trust Center
- [ ] Review all active users; confirm role assignments reflect least-privilege principle
- [ ] Remove access for any separated staff immediately; confirm none remain
- [ ] Review current Intuit agreement for safeguarding and breach notification language
- [ ] If QBO Payments is active: complete or confirm merchant SAQ
- [ ] Confirm MFA is active for all accounts with access to financial or client data

**Immediate Action Triggers:**
- Staff separation → Deprovision access same day
- Vendor security notice → Document, assess, update WISP if needed
- Payment module activated or deactivated → Reassess PCI scope

---

*Sheet last reviewed: [Date]*  
*Reviewed by: [Name / Role]*  
*Next review due: [Date + 1 year]*
