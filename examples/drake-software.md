# Vendor Oversight Sheet — Drake Software

**Service Provided:** Tax preparation platform, secure portals, optional cloud hosting  
**Data Types Involved:** NPI, PII, Financial  
**Review Schedule:** Annual

---

## Assurance & Certifications

| Certification | Status | Evidence |
|---|---|---|
| SOC 1 Type II | Attested (Right Networks) | Attestation letter on request |
| SOC 2 Type II | Attested (Right Networks) | Attestation letter on request |
| SOC 3 | Attested (Right Networks) | Attestation letter on request |
| PCI DSS | Attested at data center level (Right Networks) | Attestation letter on request |
| MFA | Enforced across Drake products | Vendor documentation |

**Note:** Drake's cloud hosting is provided through Right Networks. Certifications listed above apply to the hosted environment. Request attestation letters directly from Right Networks and retain on file.

## Security Controls

| Control | Status | Notes |
|---|---|---|
| MFA | ✓ Mandatory | Enforced across all Drake products |
| Encryption in transit | ✓ | |
| Encryption at rest | ✓ | |
| Secure portals | ✓ | Use for all document exchange with clients |
| Incident notification | ✓ | Documented in support/service agreements |

## Contractual Safeguards

Drake customer agreements outline confidentiality and data safeguarding obligations. Review current agreement to confirm breach notification language is present, including timeframe for notification and method of delivery.

## PCI DSS Considerations

Not directly applicable in standard configuration. PCI DSS considerations arise only if third-party payment add-ons are integrated with Drake. If payments are added to the workflow, assess which payment infrastructure is used and determine applicable SAQ type.

## Oversight & Review Checklist

**Annual Review Tasks:**
- [ ] Request updated Right Networks attestation letters (SOC 2, PCI DSS) and retain in vendor file
- [ ] Confirm MFA is active for all Drake user accounts
- [ ] Review active user accounts; remove access for separated staff
- [ ] Review current Drake service agreement for safeguarding and breach notification clauses
- [ ] Confirm secure portal is being used for all document exchange (not unencrypted email)
- [ ] Note any changes to Drake's hosting environment or partner (Right Networks)

**Immediate Action Triggers:**
- Staff separation → Deprovision Drake and portal access same day
- Hosting environment change announcement → Reassess certifications for new infrastructure
- Addition of payment add-on → Reassess PCI scope and applicable SAQ

---

*Sheet last reviewed: [Date]*  
*Reviewed by: [Name / Role]*  
*Next review due: [Date + 1 year]*
