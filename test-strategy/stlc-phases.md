# 🔄 STLC Phase Definitions & Readiness Criteria

Our software testing life cycle (STLC) is designed to ensure quality is a **process**, not a final phase. This document defines our commitment to each phase of the lifecycle.

## 🔍 1. Test Analysis (Requirements Review)
- **Objective**: Review business requirements for testability.
- **Artifacts**: User Stories, Business Acceptance Criteria.
- **Exit Criteria**: All requirements are mapped to the **[Master RTM](../docs/master-rtm.md)**.

## 📝 2. Test Design (Scripting & Automation)
- **Objective**: Develop automated validation scenarios.
- **Layers**: UI (Selenium 4), API (Requests), Data (SQL), Performance (JMeter).
- **Standards**: Minimal hardcoded data; explicit wait strategies for UI; schema validation for API.

## 🚀 3. Test Execution & Reporting
- **Objective**: Execute automated regression suites and report results.
- **Mechanism**: Triggered by GitHub Actions on PR and Merge events.
- **Artifacts**: Allure Reports, JUnit results, and Failure Triage logs.

## 🏁 4. Test Closure & Evaluation
- **Objective**: Assess the quality of the release build based on automated feedback.
- **Exit Criteria**: 100% execution rate with a 95%+ pass rate for mainline builds.

# 🛠️ Tooling Rationale
- **Pytest**: Selected for its extensive plugin ecosystem and robust parallel execution capabilities.
- **Selenium 4**: Modern w3c-compliant browser automation; ideal for end-to-end UX validation.
- **Faker**: Used for dynamic test data generation to maintain clean, non-repetitive datasets.
