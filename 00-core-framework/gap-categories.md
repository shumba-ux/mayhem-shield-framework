# Gap Categories

Core domains:
1. Vendor Assurance
2. Identity and Access
3. Network and Path Control
4. Data Protection Outbound
5. Data Protection Inbound / Output Validation
6. Admin / Endpoint / Operator Security
7. Supply Chain and Dependency Integrity
8. SDLC / Change Control
9. Governance / Acceptable Use
10. Monitoring / Audit / Response

Overlay-driven domains:
11. AI Governance / Model Controls
12. Agentic / Workflow Execution
13. Retrieval / Knowledge Security
14. Self-Hosted Infrastructure Control
15. Regulated Data Control
16. Output Liability / Public-Facing Safety
17. Integration / Connector Security

## Cross-references to established frameworks

Findings within these gap categories are typically cross-referenced to established frameworks during scoping and severity calibration. The mappings below describe the most common alignments. They are not exhaustive and individual findings may map to multiple framework references.

### NIST CSF 2.0 functions

| CSF Function | Gap Categories most commonly mapped |
|---|---|
| Govern | 1 Vendor Assurance, 9 Governance / Acceptable Use, 11 AI Governance / Model Controls, 15 Regulated Data Control |
| Identify | 4 Data Protection Outbound, 7 Supply Chain and Dependency Integrity, 13 Retrieval / Knowledge Security, 17 Integration / Connector Security |
| Protect | 2 Identity and Access, 3 Network and Path Control, 5 Data Protection Inbound / Output Validation, 6 Admin / Endpoint / Operator Security, 14 Self-Hosted Infrastructure Control |
| Detect | 10 Monitoring / Audit / Response, 12 Agentic / Workflow Execution, 13 Retrieval / Knowledge Security |
| Respond | 10 Monitoring / Audit / Response, 12 Agentic / Workflow Execution, 16 Output Liability / Public-Facing Safety |
| Recover | 8 SDLC / Change Control, 14 Self-Hosted Infrastructure Control |

The Recover function is a limited fit for the methodology. Mayhem Shield's review work focuses on prevention and detection. Recovery activities (rollback, remediation, infrastructure restoration) are noted where applicable but are not the primary review concern.

### OWASP Top 10 for LLM Applications

| OWASP LLM ID | Description | Gap Categories most commonly mapped |
|---|---|---|
| LLM01 | Prompt Injection | 5 Output Validation, 12 Agentic / Workflow Execution, 13 Retrieval / Knowledge Security |
| LLM02 | Insecure Output Handling | 5 Output Validation, 12 Agentic / Workflow Execution, 16 Output Liability / Public-Facing Safety |
| LLM05 | Supply Chain Vulnerabilities | 1 Vendor Assurance, 7 Supply Chain and Dependency Integrity, 8 SDLC / Change Control |
| LLM06 | Sensitive Information Disclosure | 4 Data Protection Outbound, 13 Retrieval / Knowledge Security, 15 Regulated Data Control, 17 Integration / Connector Security |
| LLM08 | Excessive Agency | 2 Identity and Access, 12 Agentic / Workflow Execution, 17 Integration / Connector Security |

OWASP LLM IDs not listed (LLM03, LLM04, LLM07, LLM09, LLM10) may apply per engagement based on deployment specifics. The mappings above are the most common patterns observed in practice.

For broader framework alignment beyond NIST CSF and OWASP LLM, see `framework-alignment.md`.
