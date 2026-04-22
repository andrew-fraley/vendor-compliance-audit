# Vendor Oversight Sheet — Bitdefender

**Service Provided:** Antivirus / Endpoint Detection and Response (EDR)  
**Data Types Involved:** System telemetry; indirectly protects all NPI/PII on covered endpoints  
**Review Schedule:** Annual

---

## Assurance & Certifications

| Certification | Status | Evidence |
|---|---|---|
| ISO 27001 | Certified | Bitdefender Enterprise certifications page |
| SOC 2 | Attested (product-line dependent) | Available from Bitdefender on request |

**Enterprise certifications:** https://www.bitdefender.com/business/enterprise-products/

## Security Controls

| Control | Status | Notes |
|---|---|---|
| Endpoint protection agent | ✓ | Deployed on all covered firm devices |
| Tamper protection | ✓ | Prevents users from disabling the agent |
| Logging & alerting | ✓ | Review management console regularly |
| Automatic signature updates | ✓ | Confirm auto-update is active |
| Engine updates | ✓ | Confirm update routine in admin settings |

## Contractual Safeguards

Bitdefender vendor documentation includes confidentiality obligations and security standards. Review current subscription or enterprise agreement for safeguarding terms and any data handling provisions related to telemetry collected from endpoints.

## PCI DSS Considerations

Not applicable. Bitdefender does not handle cardholder data directly. However, as the endpoint protection layer for devices that may access financial systems and NPI, maintaining current coverage and tamper protection is material to the firm's overall PCI and Safeguards Rule posture.

## Deployment Coverage Note

Bitdefender's value depends entirely on complete deployment. A single unprotected endpoint represents a gap in the firm's security posture. During each annual review, confirm:
- All firm-owned devices appear in the management console as active
- No devices are showing as inactive, out-of-date, or missing the agent
- Any new devices added since the last review are enrolled

## Oversight & Review Checklist

**Annual Review Tasks:**
- [ ] Confirm ISO 27001 certification is current
- [ ] Request updated SOC 2 attestation if applicable to current product/plan
- [ ] Review management console — confirm all firm devices are active and covered
- [ ] Confirm automatic signature and engine updates are enabled on all endpoints
- [ ] Verify tamper protection is active and no users have disabled agents
- [ ] Review any alerts or incidents logged since the last review; document if significant
- [ ] Review current Bitdefender agreement for safeguarding and confidentiality terms
- [ ] Confirm any devices retired since the last review have been removed from the console

**Immediate Action Triggers:**
- New device added to firm → Enroll in Bitdefender before use for firm business
- Device retired or repurposed → Remove from console; ensure device is wiped appropriately
- Alert or detection event → Document in incident log; assess whether WISP incident response procedures apply
- Agent reports as inactive or tampered → Investigate and remediate immediately

---

*Sheet last reviewed: [Date]*  
*Reviewed by: [Name / Role]*  
*Next review due: [Date + 1 year]*
