# Current Commercial Posture

**Controlling rule: legacy terms for pre-existing engagements are not a current API
licence agreement**, and are not presented as one here.

## What is actually available now

| Item | Status | Evidence | Classification |
|---|---|---|---|
| Founder-delivered engagements (advisory, audit, calibration) | **Closed and permanently retired** | `api/checkout.js` carries an explicit retired-offer guard: a retired offer is distinguished from an unknown offer and the arrival is recorded | **VERIFIED** |
| Pay screen / self-serve checkout | **Not configured.** Arrivals are recorded in a state of `unconfigured` or `retired` | `api/checkout.js:75,243,278`; live `/api/checkout-stats` reports `pay_screen_arrivals: 0` | **VERIFIED** |
| Current API licensing | **No executed licence located.** No pricing published. No contract template located | filesystem and repository search | **GAP** |
| Integration inquiries | **Accepted.** An inquiry endpoint exists and stores submissions for the owner | `api/enterprise-inquiry.js`; owner inbox endpoint | **VERIFIED (mechanism)** |
| Acquisition inquiries | **Accepted**, through the same inquiry mechanism | as above | **VERIFIED (mechanism)** |
| Pilot access | Offered as an inquiry pathway | `api/enterprise-inquiry.js` | **VERIFIED (mechanism)** |
| Pricing availability | **None published** | no pricing page or rate card located | **GAP** |
| Current contract availability | **None located**: no MSA, order form, licence template, DPA or SLA | filesystem | **GAP** |
| Executed customer deployments | **None located** | no contract or production-deployment evidence | **GAP** |
| Commercial traction to date | Live `/api/checkout-stats` reports `pay_screen_arrivals: 0`, `fallback_leads: 0`, `enterprise_inquiries: 0`, `lead_value_usd: 0` | observed live, 2026-09-08 | **VERIFIED** |

## The posture in one paragraph

**INFERENCE**, supported by every row above. JRS is currently a **passive-ownership,
inbound-only posture**. The founder-delivered service line is closed by deliberate
decision and the mechanism enforcing that closure is in the code, not merely in
intent. There is no self-serve purchase path, no published price, and no executed
customer agreement. Inbound licensing, integration and acquisition inquiries are
accepted through a working endpoint. **The asset is being held and evidenced, not
sold through a funnel.**

An evaluator should read the zeroes above as posture rather than as failure: there is
no active outbound motion to produce non-zero numbers, and the pay screen was
deliberately retired rather than left running.

## What must not be represented

- That an API licence is available for signature today. **No template exists.**
- That pricing exists. **None is published.**
- That any customer is deployed in production. **No such evidence exists.**
- That legacy founder-delivered terms extend to API licensing. They do not, and the
  engagements they belonged to are closed.

## Alert path limitation, disclosed

`api/_notify.js` requires `RESEND_API_KEY` or `SENDGRID_API_KEY`, and neither is set,
so inbound inquiries are **stored but do not generate an email alert**. Capture and
storage are sound; notification is not configured. **VERIFIED**, and relevant to any
evaluator judging inbound responsiveness.
