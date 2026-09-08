# Inbound Enterprise Diligence Package

For a serious inbound evaluator. Read this first; every claim here is traceable to a
row in `EVIDENCE_AND_LIMITATIONS_REGISTER.md`.

## 1. Executive asset brief

**What JRS is.** A documentation review methodology: a codebook of five conditions
against which an organisational record is assessed for whether its conclusion can be
reconstructed and defended from the record itself. It is accompanied by field guides,
training material, a simulation library, a public API implementing the review logic,
and a research programme testing whether the property it names is detectable.

**What Decision Reconstruction Risk (DRR) is.** The named construct: the risk that a
record cannot be reconstructed by a later independent reviewer, defined relative to a
stated reviewer standpoint.

**What the current verified assets are.**

- A canonical **Codebook** of five conditions with definitions and detection criteria (version 1.0).
- A **working token-gated API** at `/api/v1/review-engine`, server-side, with a published OpenAPI contract.
- A **detection study** with a positive, pre-registered primary result and a fully reported negative reliability result.
- A **field guide, training and simulation** asset suite.
- A **guard suite** of 126 automated checks gating changes to the repository.

**What JRS does not do.** It is not an e-discovery system. It has no chain of custody,
legal hold, privilege handling, native-file handling, evidence preservation, or
evidence-repository functionality. **These are identified gaps, not a roadmap
commitment**, and nothing in this package should be read as a plan to build them.

**Strongest current target categories.** Audit, advisory, investigations, enterprise
risk and compliance-methodology organisations; responsible-AI and AI-governance
organisations; GRC technology providers; HR technology providers; legal technology and
e-discovery platforms.

**Current validation stage.** Detection is measured and positive at group level.
Reliability was measured and **its pre-registered criterion was not met**. Construct
validity, real-world criterion validity, external validity, operational effectiveness
and legal sufficiency are **not established**.

**Current technical status.** Operational validation. The engine states this in its own
response payload on every call.

**Current commercial posture.** Passive, inbound-only. Founder-delivered engagements
are closed. No pricing, no licence template, no executed customer deployment.

**What remains unavailable or unverified.** An authorized live API test; a published
subprocessor list; retention and deletion policy; any security assurance; contributor
assignments; trademark filing evidence; a repository licence; publisher agreements.

> **Strategic assessment:** JRS appears materially more developed as a methodology and
> documentation asset suite than as a conventional enterprise software vendor. No formal
> IP grade is assigned because this exercise did not include valuation or a defined
> IP-quality rubric.

## 2. Research and validation status brief

See `RESEARCH_AND_VALIDATION_STATUS.md` for the full treatment. In summary:

| Concept | Status |
|---|---|
| Reproducibility | Disclosed as a contract feature; measured effect not audited |
| Human inter-rater reliability | Measured. **Criterion not met** |
| Accuracy against a key | 83.9%, 95% CI 72.7 to 95.1, n = 16, 384 judgments, data lock 2026-08-15 |
| Construct validity | Not established |
| Real-world criterion validity | Not established. Corpus is constructed |
| External validity | Not established |
| Operational effectiveness | Not established |
| Legal sufficiency | Not established, not claimed |
| Regulatory compliance | Not established, not claimed |

**Reliability is never summarised here as validation.**

## 3. Technical architecture brief

See `TECHNICAL_ARCHITECTURE_BRIEF.md`. Every item there is marked observed,
source-verified, operator-disclosed, owner-input dependent, or unaudited.

## 4. Security and data-handling evidence index

See `SECURITY_AND_DATA_HANDLING_EVIDENCE_INDEX.md`. It is an index, not a security
claim, and it marks GAP or NOT AUDITABLE without softening.

## 5. Current commercial posture

See `CURRENT_COMMERCIAL_POSTURE.md`.

## The honest summary

**INFERENCE**, from the whole package. The methodology, the research discipline and the
documentation quality are the assets. The engine is real, is token-gated, and says
accurately what it is. What is missing is almost entirely **evidence packaging and
legal hygiene**: assignments, filings, a licence, a subprocessor list, a retention
policy, and one authorized API test. None of those requires new product development,
and every one of them is a gap a buyer will price.
