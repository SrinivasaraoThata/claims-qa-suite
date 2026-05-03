# Healthcare Claims Quality Engineering Platform

Built by [Srinivasa Rao Thata](https://www.linkedin.com/in/srinivasa-rao-thata/) — Senior QA Automation Engineer at Cigna Healthcare, five years building automation platforms for enterprise healthcare and financial systems.

Most QA portfolios are a single repository with a few test files and a README that says "automated testing project." This one is different — not because it is more complicated, but because it is structured the way automation actually has to work when the system under test handles financial transactions and regulatory compliance.

Claims processing has a specific problem. A defect does not just break a feature — it miscalculates a payment, denies a valid authorization, or exposes PHI data that should have been masked. So the test architecture here reflects that. Four separate pillars, each catching a different class of defect, all running in CI, all mapped back to requirements.

**UI** — Selenium, Python, Page Object Model. End-to-end claim submission and portal workflows. [View repo](https://github.com/SrinivasaraoThata/claims-ui-automation)

**API** — Python Requests, five test modules mapped to the RTM. Business logic, schema validation, payment service coverage. [View repo](https://github.com/SrinivasaraoThata/claims-api-automation)

**Data Integrity** — Pytest, SQL, HIPAA/PHI isolation. Payment calculation accuracy, state transitions, PII masking at the database layer. [View repo](https://github.com/SrinivasaraoThata/claims-data-integrity)

**Performance** — JMeter, Pytest, SLA threshold enforcement, JTL parsing. Load validation under realistic transaction volumes. [View repo](https://github.com/SrinivasaraoThata/claims-performance-testing)

ParaBank was used as the simulation layer because its financial transaction model — account states, transfers, loan processing — maps cleanly onto claims state transitions. Pending to processed to approved follows the same logic as a financial transaction moving through verification and settlement. The domain choice was deliberate because the same validation logic that catches a payment error in a claims system catches a reconciliation failure in any financial system.

GitHub Copilot was used throughout, mainly for generating edge cases in claim state transition logic — scenarios like concurrent authorization decisions and remittance records that do not reconcile with submission data. The kind of scenarios that are obvious in hindsight but rarely make it into a manual test plan.

Regression cycle runs in 45 minutes instead of three days. Coverage above 90% across all four pillars. Six compliance requirements traced across every layer — HIPAA/PHI, ICD-10, RBAC, Adjudication, PII Masking, and cross-system data integrity.

Full traceability: [Master RTM](https://github.com/SrinivasaraoThata/claims-qa-suite/blob/main/docs/master-rtm.md)
