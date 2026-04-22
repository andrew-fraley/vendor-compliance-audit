# Vendor Oversight Sheet — Xero

**Service Provided:** Accounting platform  
**Data Types Involved:** NPI, PII, Financial  
**Review Schedule:** Annual

---

## Assurance & Certifications

| Certification | Status | Evidence |
|---|---|---|
| ISO/IEC 27001:2022 | Certified | Xero Trust Center |
| SOC 2 | Available on request | Request from Xero |

**Trust Center:** https://www.xero.com/us/security/

## Security Controls

| Control | Status | Notes |
|---|---|---|
| MFA | ✓ Enforced | |
| Encryption in transit | ✓ | |
| Encryption at rest | ✓ | |
| Role-based access controls | ✓ | Assign minimum necessary permissions per user |
| Activity logging | ✓ | |

## Contractual Safeguards

Xero's terms of service and trust center policies cover data processing and safeguarding obligations. Review the current subscriber agreement for breach notification requirements, including notification timeframe and responsible party.

A Data Processing Agreement (DPA) may be available depending on jurisdiction and account type. Request if applicable.

## PCI DSS Considerations

Not applicable in the standard accounting configuration. If the Xero payments module is activated, the firm enters the payment card data flow and PCI DSS considerations apply. Reassess PCI scope and applicable SAQ type if payments are enabled.

## Oversight & Review Checklist

**Annual Review Tasks:**
- [ ] Confirm ISO 27001 certificate is current via Trust Center
- [ ] Request updated SOC 2 report and retain in vendor file
- [ ] Review all active users; confirm role assignments follow least-privilege principle
- [ ] Remove access for any separated staff; confirm none remain active
- [ ] Review current Xero agreement for safeguarding and breach notification language
- [ ] Confirm MFA is active for all accounts

**Immediate Action Triggers:**
- Staff separation → Deprovision access same day
- Payments module activated → Reassess PCI scope
- Vendor security notice → Document, assess impact, update WISP if needed

---

*Sheet last reviewed: [Date]*  
*Reviewed by: [Name / Role]*  
*Next review due: [Date + 1 year]*
