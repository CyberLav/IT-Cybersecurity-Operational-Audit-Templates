# Vulnerability Risk Assessment Form (RAF)

This matrix evaluates identified IT operational threat profiles to calculate Inherent Risk, Control Effectiveness Ratings, and resulting Scoping Priorities.

## Calculated Risk Scope Matrix

| Process / ID | Core Operational Risk Target | Inherent Impact | Inherent Likelihood | Inherent Rating | Existing Mitigating Controls | Control Rating (CE) | Residual Rating | Scoping Priority |
| :--- | :--- | :---: | :---: | :---: | :--- | :---: | :---: | :--- |
| **RSK-01**<br>Governance | Inadequate or misaligned Vulnerability Governance (strategy, policies, exceptions, and SLAs) | 5 | 4 | **20** | Monthly Security Steering Committee reviews backlog; Vulnerability Management Policy drafted in 2023. | 3 | **12** | **High Priority** |
| **RSK-02**<br>Asset Discovery | Inaccurate asset visibility and boundary definition (Shadow IT, rogue devices, and missing inventory) | 4 | 5 | **20** | CMDB updated monthly via manual spreadsheet consolidation; Active Directory sync occurs weekly. | 4 | **16** | **High Priority** |
| **RSK-03**<br>Scanning Quality | Ineffective or blind vulnerability scanning practices (frequency, scope, credentialed scanning, and accuracy) | 5 | 3 | **15** | Automatic scanner scheduled for external networks weekly. Internal scans are uncredentialed. | 3 | **9** | *Medium Priority* |
| **RSK-04**<br>Patch Deployment | Slow or inconsistent patch deployment and remediation backlog management | 5 | 5 | **25** | Patching is centralized via SCCM; critical patches are manually pushed when resources permit. | 4 | **20** | **High Priority** |
| **RSK-05**<br>Testing Validation | Lack of patch testing, validation, and rollback resilience (operational disruptions) | 4 | 3 | **12** | Emergency changes bypass standard testing; routine patches are deployed directly after a 24hr staging window. | 2 | **4.8** | Low Priority |
| **RSK-06**<br>Legacy Systems | Insufficient management of Legacy and End-of-Life (EOL) systems (compensating controls) | 4 | 4 | **16** | System decommissioning list updated during budgeting. No isolated VLAN mapping implemented. | 5 | **16** | **High Priority** |
