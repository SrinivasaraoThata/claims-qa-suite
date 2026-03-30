# Healthcare Claims: Quality Engineering Strategy Hub

This repository serves as the **Master Test Strategy** and orchestration center for the Healthcare Claims Management system. Instead of a single monolithic repo, our quality strategy is divided into specialized, high-performance suites for UI, API, Data, and Performance.

## The Mission
The objective is to achieve **90%+ automated regression coverage** for the Claims lifecycle. By implementing a "Shift-Left" approach, we validate business logic at the API and Database levels before the UI is even rendered, significantly reducing the cost of defects found in UAT.

## Integrated Quality Architecture (Specialized Pillars)
This hub manages four high-performance repositories that validate the full claims lifecycle.

```mermaid
graph TD
    hub["<b>Quality Engineering Hub</b><br/>Strategy & Traceability"]
    
    hub --> UI["<b>UI Automation Pillar</b><br/><i>[Active] Selenium/Python</i>"]
    hub --> API["<b>API Validation</b><br/><i>[Upcoming] Requests</i>"]
    hub --> DATA["<b>Data Integrity</b><br/><i>[Upcoming] SQL/Pytest</i>"]
    hub --> PERF["<b>Performance Pillar</b><br/><i>[Upcoming] JMeter</i>"]
    
    classDef main fill:#f5f5f5,stroke:#333,stroke-width:2px,color:#000;
    classDef active fill:#e1f5fe,stroke:#01579b,stroke-width:2px,color:#01579b;
    classDef upcoming fill:#fff,stroke:#999,stroke-dasharray: 5 5,color:#666;
    
    class hub main;
    class UI active;
    class API,DATA,PERF upcoming;
```

For detailed strategy and execution on each pillar, refer to their respective hubs.

*   [UI Automation (Selenium)](https://github.com/SrinivasaraoThata/claims-ui-automation): End-to-end UX integrity.

## Technology Rationale
*   **Python Stack**: Chosen for its library support (Requests, Pytest) and ease of integration into modern CI/CD pipelines.
*   **ParaBank Proxy**: Used to simulate the "Claims" lifecycle. Financial transactions are mapped to Claim States (Pending -> Processed -> Approved).
*   **Centralized Traceability**: All tests are mapped to the **[Master RTM](docs/master-rtm.md)** found in this hub.

## Strategic Goals
*   **Reduce Manual Overhead**: Automating 15+ high-frequency manual claim checks.
*   **Feedback Loop**: Reducing the regression cycle from 3 days to 45 minutes via parallel execution.
*   **Security & Compliance**: Validating PII/PHII masking and RBAC early in the cycle (See **[Compliance Strategy](docs/compliance-security.md)**).

## Hub Structure
```text
claims-qa-suite/
├── docs/                 # Strategy, Master RTM, and Compliance documentation
│   ├── master-rtm.md     # Requirements Traceability
│   └── compliance-security.md # HIPAA/PHI Security Strategy
├── test-strategy/        # STLC phase definitions and Tooling rationale
└── README.md             # Strategy Overview
```

---
**Srinivasa Rao Thata** | Senior QA Automation Engineer
`Quality Engineering | Strategy & Orchestration`
