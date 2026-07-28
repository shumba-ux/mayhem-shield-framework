# Mayhem Shield Framework (Public)

## Enterprise AI Implementation Assurance

Mayhem Shield helps organizations evaluate whether AI controls are effective in real deployments, not only documented in policy or vendor claims.

This repository is the public version of the Mayhem Shield framework. It provides the method, classification model, and public-safe templates used to scope and assess enterprise AI implementations.

## What Mayhem Shield does
- Evaluates implementation-level risk in AI-enabled systems.
- Maps expected controls to concrete architecture and workflow patterns.
- Uses evidence-based review phases and approval gates.
- Verifies what vendors claim about AI products before contracts are signed.
- Highlights control gaps and readiness concerns before production or expansion.

## What this framework is
- A structured assurance model for enterprise AI implementations.
- A way to classify deployments by primary implementation category.
- An overlay model for capability patterns that materially change risk.
- A practical starting point for internal review and external due diligence conversations.

## Who this is for
- **Security, risk, and compliance teams** scoping AI assurance and control expectations.
- **Architecture and platform owners** aligning design choices with review structure and evidence needs.
- **Product and engineering leaders** preparing for governance, procurement, or customer due diligence on AI features.
- **Anyone** who needs a clear, repeatable way to talk about *how* an AI system is implemented, not only *what* vendor documentation claims.

## Six implementation categories
Every review starts with one primary implementation category:
1. Pure AI Services
2. AI-Native SaaS
3. Traditional SaaS with AI Features
4. SaaS with AI Enhancement
5. Infrastructure with AI
6. AI-Native Content Generation

## Capability overlays
Overlays are additive modifiers applied on top of the primary category when relevant:
- RAG
- Agentic Workflow Execution
- Self-Hosted / Private Deployment
- Regulated Data
- Integration / Connector Exposure
- Output Liability / Public-Facing Use

## Framework alignment
Mayhem Shield's methodology references established standards including NIST AI RMF, ISO/IEC 42001, EU AI Act, OWASP Top 10 for LLM Applications, NIST CSF 2.0, and SR 11-7. See `00-core-framework/framework-alignment.md` for where each standard appears in the methodology. Alignment refers to methodology reference, not certification.

## How to use this in 30 minutes
1. Skim `00-core-framework/methodology.md` for the review model and phases (about 10 minutes).
2. Open `03-guides/category-selection-guide.md` and pick **one** primary implementation category for your deployment (about 5 minutes).
3. Open `03-guides/overlay-selection-guide.md` and note **all** overlays that apply (about 5 minutes).
4. Read the matching files under `01-implementation-categories/` and `02-capability-overlays/` for definitions you selected (about 10 minutes).

You will leave with a labeled scope (category plus overlays) and vocabulary aligned with the rest of the framework. Deeper work lives under `00-core-framework/` (evidence, severity, gates) and `05-templates/` when you are ready to document architecture and flows.

## How to navigate this repository
- `00-core-framework/` - Core methodology, evidence model, claim verification, severity model, and review structure.
- `01-implementation-categories/` - Definitions and distinctions for the six primary categories.
- `02-capability-overlays/` - Overlay definitions and control-impact context.
- `03-guides/` - Public-safe guidance for category and overlay selection.
- `05-templates/` - Public-safe starter templates for diagrams and review artifacts.

Recommended path:
1. `00-core-framework/methodology.md`
2. `00-core-framework/claim-verification.md`
3. `01-implementation-categories/README.md`
4. `02-capability-overlays/README.md`
5. `03-guides/category-selection-guide.md`
6. `03-guides/overlay-selection-guide.md`
7. `00-core-framework/framework-alignment.md`

## What is intentionally not included in this public version
This repository intentionally excludes proprietary internal delivery artifacts. It is designed for framework transparency and public education, not for complete internal engagement execution.
