# Vendor Oversight Sheet — TaxDome

**Service Provided:** Practice management, client portal, payments  
**Data Types Involved:** NPI, PII, Financial, Cardholder (if payments enabled)  
**Review Schedule:** Annual

---

## Assurance & Certifications

| Certification | Status | Evidence |
|---|---|---|
| SOC 2 Type II | Publicly attested | Available on request from vendor |
| PCI DSS Level 2 | Attested (payments module) | PCI AOC available from provider |

## Security Controls

| Control | Status | Notes |
|---|---|---|
| MFA | Available | Must be enforced via admin settings |
| Encryption in transit | ✓ | |
| Encryption at rest | ✓ | |
| Client portal | ✓ | Reduces reliance on unencrypted email |
| Incident response | ✓ | Documented in vendor agreements |
| Breach notification | ✓ | Confirm clause in current agreement |

## Contractual Safeguards

Service agreements cover data safeguarding obligations. Before signing or renewing, confirm the agreement explicitly includes:
- Data safeguarding obligations
- Incident and breach notification requirements (timeframe and method)

## PCI DSS Considerations

- Payment flow is **provider-hosted** (Stripe/TaxDome infrastructure)
- Firm's direct PCI exposure is reduced but not eliminated
- Firm is still classified as a **merchant** and must complete an applicable SAQ
- For fully hosted payment pages with no direct card handling: **SAQ A** typically applies
- Consult a QSA if unsure which SAQ applies to your specific configuration

## Oversight & Review Checklist

**Annual Review Tasks:**
- [ ] Request updated SOC 2 report or confirm public attestation is current
- [ ] Confirm PCI AOC is current (request from TaxDome if needed)
- [ ] Review all active admin and staff users; remove access for any separated personnel
- [ ] Confirm MFA is enforced for all user accounts
- [ ] Review current service agreement — confirm safeguarding and breach notification clauses are present
- [ ] Complete or confirm merchant SAQ if payments module is in use

**Immediate Action Triggers (outside annual schedule):**
- Staff separation → Deprovision access same day
- Vendor security notice or breach → Document receipt, assess impact, update WISP if needed
- Changes to payment configuration → Reassess PCI SAQ applicability

---

*Sheet last reviewed: [Date]*  
*Reviewed by: [Name / Role]*  
*Next review due: [Date + 1 year]*
