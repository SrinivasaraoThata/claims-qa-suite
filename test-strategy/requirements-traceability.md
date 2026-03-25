# Requirements Traceability Matrix (RTM)

The following table maps core Healthcare User Stories to their corresponding automated test identifiers, ensuring comprehensive coverage and traceability.

| User Story ID | Description | Test ID(s) | Test Layer |
| :--- | :--- | :--- | :--- |
| **US-1001** | **Login**: As a member, I need to securely log into the portal. | `TC-UI-1001`, `TC-API-1001` | UI, API |
| **US-1002** | **Claim Search**: As a member, I want to search for claims. | `TC-UI-1002`, `TC-DB-1002` | UI, Data |
| **US-1003** | **Status Verification**: As a member, I must see the correct status of my claim. | `TC-API-1003`, `TC-UI-1003` | API, UI |
| **US-1004** | **Denial Reasons**: As a member, I need to view the specific reason codes if a claim is denied. | `TC-API-1004`, `TC-UI-1004` | API, UI |
| **US-1005** | **Claim History**: As a member, I want to view my historical claims. | `TC-UI-1005`, `TC-PERF-1005` | UI, Performance |

---
**Author:** Srinivasa Rao Thata  
**Year:** 2026
