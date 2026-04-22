# Vendor Oversight Sheet — Proton (Mail & VPN)

**Service Provided:** Encrypted email, VPN  
**Data Types Involved:** NPI, PII, communications  
**Review Schedule:** Annual

---

## Assurance & Certifications

| Certification | Status | Evidence |
|---|---|---|
| ISO 27001 | Certified (2024) | Proton Trust Center |
| SOC 2 Type II | Attested (2025) | Proton Trust Center |

**Transparency & Trust:** https://proton.me/legal/transparency

## Security Controls

| Control | Status | Notes |
|---|---|---|
| End-to-end encryption | ✓ | Applies to Proton-to-Proton email only |
| TLS (external email) | ✓ | Applies when emailing non-Proton recipients |
| MFA | ✓ Enforced | |
| VPN | ✓ | Define firm policy for required use cases |

### Important Encryption Note

End-to-end encryption applies **only** when both sender and recipient are using Proton Mail. Email sent to or received from non-Proton addresses is encrypted in transit via TLS but is not end-to-end encrypted. For sensitive NPI transmissions to clients or third parties not on Proton, use the secure portal (TaxDome or Drake) rather than email.

## Contractual Safeguards

Proton Business agreements document security practices and data handling obligations. Review current subscription agreement for safeguarding terms and breach notification requirements.

## PCI DSS Considerations

Not applicable.

## VPN Use Policy

The VPN functionality should be governed by a documented use policy. At minimum, define the scenarios in which VPN use is required:

**Recommended required use cases:**
- Any public or untrusted Wi-Fi network (coffee shops, airports, hotels, client offices)
- Travel outside the primary office
- Remote work from networks not controlled by the firm
- Any access to NPI or client data outside the primary office environment

Document this policy in the firm's WISP or employee security policy and confirm all staff are aware of the requirement.

## Oversight & Review Checklist

**Annual Review Tasks:**
- [ ] Confirm ISO 27001 and SOC 2 certifications are current via Trust Center
- [ ] Review all active Proton accounts; confirm they correspond to current staff
- [ ] Remove accounts for separated staff
- [ ] Confirm MFA is enforced for all accounts
- [ ] Review and confirm the firm's VPN use policy is documented and communicated to staff
- [ ] Remind staff of encryption limitation for non-Proton recipients; confirm portal use for sensitive exchanges
- [ ] Review current Proton Business agreement for safeguarding terms

**Immediate Action Triggers:**
- Staff separation → Disable/remove Proton account same day
- Vendor security notice → Document, assess impact on firm communications, update WISP if needed

---

*Sheet last reviewed: [Date]*  
*Reviewed by: [Name / Role]*  
*Next review due: [Date + 1 year]*
