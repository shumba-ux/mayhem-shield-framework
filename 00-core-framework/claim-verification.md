# Claim Verification

## Where this sits in the framework

The implementation categories, overlays, and review phases in this framework
assess how an AI system operates **in your environment**: your identities, your
data paths, your integrations. Claim verification is the upstream module. It
assesses what the vendor asserted **before you signed**: the sentences on the
product page, in the security documentation, and in the contract that caused
someone to believe the product was safe to buy.

The two questions are different and both precede a defensible approval:

- **Before you sign:** does the product do what the vendor claims?
- **Before you go live:** does the deployment behave acceptably in your
  environment?

A review that answers only the second question inherits the vendor's claims as
assumptions. This module exists so they are inputs instead.

## The unit of work is the claim, quoted verbatim

A claim is a specific sentence the vendor published or contracted, captured
word for word from an identified source, with the source archived and dated.
Paraphrases are not claims: a paraphrase can be narrower or broader than what
the vendor said, and the difference between the sentence and its paraphrase is
frequently where the risk lives.

Every claim record carries: the verbatim text, the source and its capture
date, an operational interpretation (what would be true about the product's
behavior if this sentence is true), with the interpretation explicitly
labelled as the reviewer's.

## Evidence classes

Every finding about a claim states what class of evidence supports it. The
classes are ordered by what they can establish, and the class travels with the
finding wherever the finding goes: a finding may never be quoted without its
class.

| Class | What it is | What it can establish |
|---|---|---|
| **Behavioral** | The reviewer operated the product and observed the result | What the product actually did, under stated conditions, at a point in time |
| **Configuration** | Settings, policy exports, architecture documentation | What the product is set up to do |
| **Log** | Records of the product having done something | That an event occurred, as recorded by the system that recorded it |
| **Contractual** | Terms, DPA/BAA language, vendor attestation | What the vendor has committed to, and what recourse exists |
| **Unverified** | No evidence obtained, or the claim is not assessable | Nothing. Stated so the gap is visible rather than absent |

These classes organize the typical evidence listed in `evidence-model.md`:
architecture diagrams, configuration screenshots, and workflow definitions are
configuration-class; logging samples are log-class; policy references and
contract language are contractual-class; and validation or test results reach
behavioral class only when the reviewer performed the validation. The
principle is the same one `evidence-model.md` states for deployments: a claim
is not treated as satisfied because someone says it is.

**Two rules that hold everywhere:**

1. **Vendor-supplied material caps below behavioral.** A vendor's exported
   log is log-class evidence: it establishes what their system recorded, not
   what a reviewer observed. No answer, artifact, or demonstration supplied by
   the vendor can produce a behavioral-class finding, because behavioral means
   the reviewer ran it. This cap is structural, not a comment on any vendor's
   honesty.
2. **A certificate is evidence about a program, not a product.** SOC 2, ISO
   certifications, and comparable attestations establish that an auditor
   examined the vendor's controls over a period. They do not test whether the
   specific claimed behavior occurs. In this model they are contractual-class
   evidence for the claim under review.

## The four answers a claim can receive in scoping

Before any evidence is gathered, each claim is sorted by what could settle it.
This sorting is itself a deliverable: it tells a buyer where their exposure is
checkable and where it is a matter of trust, before anything is spent.

1. **Checkable.** A test could observe the answer. Retention behavior, what
   leaves a tenant, accuracy on a defined set.
2. **Verifiable by artifact.** Not observable from outside, but a
   configuration export, policy, or log can evidence it.
3. **Contractual only.** The claim lives in terms and commitments, or only on
   the marketing page. The verification is whether the contract says what the
   website says; the gap between those two documents is a finding.
4. **Not locatable.** No testable sentence exists under the language.
   Superlatives and category marketing. Recorded as such, because a claim that
   cannot be located cannot later be enforced.

## Vendor answers, when interrogation is part of the review

Where the buyer's process allows questions to the vendor, each answer is
recorded with two separate judgments, because they fail differently:

- **Form** (mechanical): what came back. An artifact, a described specific
  instance, a statement of intent or policy, a refusal, or nothing. Form sets
  the ceiling on the evidence class the answer can support: an artifact can
  reach configuration or log class; a statement of intent caps at contractual;
  a refusal or an unasked question caps at unverified.
- **Substantiation** (reviewer judgment): whether what came back actually
  supports the claim it was offered for, recorded with a reason. A polished
  artifact that answers a different question is recorded exactly that way,
  because a review that collected impressive documents and established nothing
  must be distinguishable from a review that established something.

Contractual-class findings require a document. A commitment stated in a
meeting is a statement of intent and caps at unverified until it appears in
terms someone can later hold.

## Point in time, stated as scope

For products without a version pin, every behavioral and configuration finding
is a statement about the product on the date of assessment. The vendor can
change behavior afterward without notice. Claim verification therefore
records, for each claim, whether it is **exposed to change** (behavioral
properties of an unversioned service) or **durable** (contractual commitments,
architectural facts). That distinction usually outlives any individual result,
and it is stated in the deliverable rather than left for the reader to infer.

## Inconclusive is a finding

Some claims cannot be settled at the scale anyone can test them. When that is
the result, it is reported as the result, with the reason: what was tested,
what the design could and could not have detected, and what remains unproven.
A claim known to be unproven at testable scale is materially different from a
claim known to be true, and different again from a claim nobody examined. The
deliverable preserves all three states.

## What this module deliberately excludes

Consistent with this repository's public scope: the testing instrument,
fixtures, capture and integrity tooling, and engagement-specific artifacts are
not published here. The method above lets a reader evaluate whether the
reasoning in a claim-verification deliverable is sound, and lets a competent
reader reconstruct any published test from its stated conditions. It does not
include the internal tooling that produces the evidence.
