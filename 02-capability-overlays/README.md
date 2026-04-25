# Capability Overlays

Overlays are cross-cutting deployment patterns that materially change control expectations, evidence needs, or approval conditions.

## Current overlays
- RAG
- Agentic Workflow Execution
- Self-Hosted / Private Deployment
- Regulated Data
- Integration / Connector Exposure
- Output Liability / Public-Facing Use

## Framework references triggered by overlays

Overlays often trigger specific framework references during scoping. Common patterns:

| Overlay | Framework references typically triggered |
|---|---|
| RAG | OWASP LLM01 (Prompt Injection), LLM06 (Sensitive Information Disclosure); NIST AI RMF Map function for retrieval source classification |
| Agentic Workflow Execution | OWASP LLM01, LLM02, LLM08 (Excessive Agency); NIST CSF 2.0 Detect and Respond functions for agent action monitoring |
| Self-Hosted / Private Deployment | NIST CSF 2.0 Protect and Recover functions for infrastructure control |
| Regulated Data | EU AI Act high-risk classification triggers; SR 11-7 for regulated financial services; NIST CSF 2.0 Govern function |
| Integration / Connector Exposure | OWASP LLM06, LLM08; NIST CSF 2.0 Identify function for connector inventory |
| Output Liability / Public-Facing Use | OWASP LLM02 (Insecure Output Handling); EU AI Act transparency obligations |

See `../00-core-framework/framework-alignment.md` for the full methodology-to-framework mapping.
