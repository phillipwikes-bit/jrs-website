# Security and Data-Handling Evidence Index

**This is an index of evidence, not a security claim.** Items are marked GAP or NOT
AUDITABLE where evidence is absent, and absence is not softened.

| Control | Evidence located | Classification |
|---|---|---|
| TLS and transport | Live HTTPS on `www.jrsstandard.com`; HSTS header observed (`strict-transport-security: max-age=63072000`) | **VERIFIED (transport only)**. Not evidence of application security |
| Authentication | Bearer token compared against an allow-list; 401 on non-match; the public 401 deliberately names no environment variable | **VERIFIED (source)** |
| Authorization | No role or scope model located. Access is binary: a valid token or none | **VERIFIED (source)**, and a design limitation to disclose |
| Secrets management | Provider key read from `process.env` server-side; no client-side reference located; no secret located in committed files | **VERIFIED (source)**. Vault, rotation policy and access audit: **GAP** |
| Provider API-key custody | Held in the hosting environment | **NOT AUDITABLE** from the repository |
| Logging and telemetry | `logReview()` writes result fields only | **VERIFIED (source)** |
| Record-text retention | Deliberately not stored, not echoed, not logged | **VERIFIED (source)**; independent confirmation **NOT AUDITABLE** (test CT-6) |
| Result retention | Result rows are written and retained. **No retention period or deletion schedule located** | **GAP** |
| Subprocessors | Anthropic (model inference), Vercel (hosting and edge execution), Supabase (data storage). All three evidenced in code. **None disclosed on `terms.html` or `security.html`** | **VERIFIED in code / GAP as published** |
| Data residency | No residency commitment located; provider-determined | **GAP** |
| Deletion | No deletion endpoint, policy or schedule located | **GAP** |
| Incident response | No documented process, contact, or severity model located | **GAP** |
| Vulnerability management | No policy or scanning evidence located | **GAP** |
| Penetration testing | None located | **GAP**. Do not represent the system as tested |
| Availability and recovery | No SLA, uptime record, backup policy or RTO/RPO located | **GAP** |
| Certifications or attestations | No SOC 2, ISO 27001 or ISO/IEC 42001 attestation located | **GAP**. Do not represent the system as certified |
| Rate limiting as a control | Best-effort and per-instance by the source's own description, with a `TODO` for a shared store | **VERIFIED as limitation** |
| Private owner surfaces | Secured by opaque unlinked slugs with `noindex,nofollow` and no analytics tag. **No token control** | **VERIFIED (source and policy)**. Security rests on URL secrecy, which should be stated plainly to any evaluator |

## The three findings an enterprise reviewer will raise first

**INFERENCE**, from the rows above:

1. **No published subprocessor disclosure.** Three processors are evidenced in code and
   none appears on the public privacy or security pages. This is the cheapest gap to
   close and the most likely to be noticed.
2. **No retention or deletion policy for result telemetry.** Non-retention of record
   text is well documented; what *is* kept, and for how long, is not.
3. **No independent security assurance of any kind.** No penetration test, no
   attestation, no external review. Expected at this stage, and it must be stated
   rather than left to inference.

None of these is a defect in the engine. All three are documentation and policy gaps,
which is the same conclusion this package reaches overall.
