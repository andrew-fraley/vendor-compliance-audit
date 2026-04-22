# Vendor Oversight Sheet — Bitwarden

**Service Provided:** Password manager  
**Data Types Involved:** Credentials; indirectly protects all NPI/PII systems  
**Review Schedule:** Quarterly (user access) / Annual (full vendor review)

---

## Assurance & Certifications

| Certification | Status | Evidence |
|---|---|---|
| ISO 27001 | Certified | Bitwarden Compliance page |
| SOC 2 Type II | Attested | Bitwarden Compliance page |
| SOC 3 | Attested | Bitwarden Compliance page |
| HIPAA alignment | Documented | Not a regulatory requirement for this firm; noted as positive compliance signal |

**Compliance page:** https://bitwarden.com/compliance/

## Security Controls

| Control | Status | Notes |
|---|---|---|
| MFA | ✓ Available | Must be enforced via admin policy for all users |
| SSO support | ✓ | Available on Business/Enterprise plans |
| Zero-knowledge encryption | ✓ | Bitwarden cannot access vault contents |
| Audit logging & reporting | ✓ | Available in admin console |
| Self-hosting option | Available | If firm requires on-premises control |

## Contractual Safeguards

Bitwarden Business subscription agreements include data safeguarding obligations. Review the current business agreement for confidentiality terms and breach notification requirements.

## PCI DSS Considerations

Not applicable. Bitwarden does not process, store, or transmit cardholder data directly. However, because the password manager holds credentials to systems that do process NPI and financial data, access control and MFA enforcement here are high priority.

## Risk Note

The password manager is a high-value target. Compromise of the vault would expose credentials for most or all firm systems. This elevated risk justifies:
- Mandatory MFA for all vault users (enforce via admin policy, not user discretion)
- Quarterly access reviews (vs. annual for lower-risk vendors)
- Same-day deprovisioning for separated staff — no exceptions

## Oversight & Review Checklist

**Quarterly Access Review:**
- [ ] Pull active user list from admin console
- [ ] Confirm all active users are current staff
- [ ] Confirm MFA is enforced for all accounts (check admin policy, not individual settings)
- [ ] Review any shared collections or items — confirm access is limited to those with legitimate need
- [ ] Check for any failed login alerts or unusual activity in audit log

**Annual Vendor Review (in addition to quarterly tasks):**
- [ ] Confirm ISO 27001 and SOC 2 certifications are current
- [ ] Review current Bitwarden Business agreement for safeguarding and breach notification clauses
- [ ] Assess whether self-hosting would be more appropriate given current firm size and risk profile
- [ ] Confirm Bitwarden client applications are up to date on all firm devices

**Immediate Action Triggers:**
- Staff separation → Revoke vault access same day; rotate any shared credentials the departing employee had access to
- Vendor security incident → Assess scope, rotate potentially exposed credentials, document in incident log

---

*Sheet last reviewed: [Date]*  
*Reviewed by: [Name / Role]*  
*Next quarterly access review due: [Date + 3 months]*  
*Next full vendor review due: [Date + 1 year]*
