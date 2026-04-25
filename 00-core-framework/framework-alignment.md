# Framework Alignment

Mayhem Shield's review methodology is built around implementation assurance, not certification. The methodology references established standards where they materially inform scoping, evidence rules, severity, or gate conditions.

This document describes how each referenced standard shows up in the methodology. It is not a certification claim and not a comprehensive mapping. It is a description of where each standard does work in a Mayhem Shield engagement.

## Standards referenced

The methodology references the following standards:

- NIST AI Risk Management Framework (AI RMF 1.0)
- ISO/IEC 42001:2023 Artificial Intelligence Management System
- EU AI Act (Regulation 2024/1689)
- OWASP Top 10 for LLM Applications
- NIST Cybersecurity Framework 2.0
- SR 11-7 Guidance on Model Risk Management

Each standard is summarized below with the part of the Mayhem Shield methodology where it shows up.

## NIST AI RMF

The Govern, Map, Measure, and Manage functions of the NIST AI RMF inform the structure of the methodology.

- Map informs intake classification (implementation category and applicable overlays)
- Measure informs evidence rules and the findings register
- Manage informs gate conditions for POC, pilot, and production
- Govern informs the review of organizational accountability for the deployment under review

The four-function structure is used as a reference for how a review covers risk identification, measurement, and management across the engagement, not as a checklist.

## ISO/IEC 42001

ISO/IEC 42001 is the management system standard for artificial intelligence. The standard's clauses on leadership, planning, support, operation, performance evaluation, and improvement are referenced when reviewing whether the deployment under review has the organizational governance to support it.

Specifically:

- Clause 5 (Leadership) informs how Mayhem Shield reviews accountability and ownership for the AI deployment
- Clause 6 (Planning) informs how risk assessment and treatment are evaluated
- Clause 8 (Operation) informs how operational controls are reviewed
- Clause 9 (Performance evaluation) informs evidence rules around monitoring and measurement

The standard is used as an alignment reference. Mayhem Shield is not certified to ISO/IEC 42001 and does not represent itself as such.

## EU AI Act

The EU AI Act's risk-tier classification informs platform classification at intake.

- Prohibited and high-risk systems trigger expanded review depth
- High-risk systems trigger specific control findings around data governance, transparency, human oversight, robustness, accuracy, and cybersecurity
- Limited-risk systems trigger specific findings on transparency obligations
- Minimal-risk systems trigger a lighter review aligned to the risk profile

For deployments where the EU AI Act applies (either by deployment location, by user base, or by client policy), the risk tier is documented as part of intake and informs review depth and findings.

## OWASP Top 10 for LLM Applications

The OWASP Top 10 for LLM Applications is referenced for any deployment that includes a large language model component. Findings related to the OWASP categories are mapped to specific LLM IDs in the findings register.

The mappings most commonly applied:

- LLM01 Prompt Injection
- LLM02 Insecure Output Handling
- LLM04 Model Denial of Service
- LLM05 Supply Chain Vulnerabilities
- LLM06 Sensitive Information Disclosure
- LLM07 Insecure Plugin Design
- LLM08 Excessive Agency
- LLM09 Overreliance
- LLM10 Model Theft

Mappings are applied where the finding falls clearly within the OWASP category. Findings that do not fit the OWASP categories are recorded under the Mayhem Shield gap categories without forced mapping.

## NIST CSF 2.0

The NIST Cybersecurity Framework 2.0 functions (Govern, Identify, Protect, Detect, Respond, Recover) provide a categorization layer for findings.

The categorization helps enterprise security teams map Mayhem Shield findings to their existing CSF-aligned programs. Each finding can be tagged with the CSF function it most clearly addresses, in addition to the Mayhem Shield gap category. This is not a primary classification axis. It is a cross-reference for clients whose internal risk and compliance programs are organized around CSF.

## SR 11-7

SR 11-7 is the Federal Reserve guidance on model risk management. It is referenced for AI-as-model deployments in regulated financial services where the AI component produces decisions that constitute model use under the institution's model risk policy.

Where SR 11-7 applies:

- Model identification and classification inform intake scoping
- Model validation expectations inform evidence rules
- Model risk tiering informs severity calibration
- Ongoing monitoring expectations inform gate conditions for production

SR 11-7 is not applied to every engagement. It is applied when the client is a regulated financial institution and the AI component meets their internal definition of a model.

## What this alignment is not

This document describes methodology references, not certifications. Specifically:

- Mayhem Shield is not certified under ISO/IEC 42001, ISO/IEC 27001, or any other standard listed here
- Mayhem Shield is not a NIST-recognized assessor for AI RMF or CSF
- Mayhem Shield is not authorized by the EU to issue conformity assessments under the EU AI Act
- Mayhem Shield does not perform regulatory examinations under SR 11-7

These standards inform how Mayhem Shield structures its review work. Specific framework mapping for any given engagement is confirmed during scoping based on tool category, deployment overlay, and applicable regulatory context.

## Cross-reference summary

| Standard | Where it shows up |
|---|---|
| NIST AI RMF | Gap structure, scoping classification, severity calibration, gate conditions |
| ISO/IEC 42001 | Organizational governance review, accountability evidence rules |
| EU AI Act | Platform classification at intake, high-risk tier findings |
| OWASP Top 10 for LLM | LLM-specific findings tagged with OWASP IDs |
| NIST CSF 2.0 | Cross-reference categorization layer for findings |
| SR 11-7 | Regulated finance engagements involving model use |
