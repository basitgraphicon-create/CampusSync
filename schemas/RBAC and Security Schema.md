---
tags: [schema]
---

# RBAC and Security Schema

This document provides a high-level index of the **Role-Based Access Control and Security** domain.

```mermaid
erDiagram
    USER }|--|| ROLE : "assigned"
    ROLE ||--o{ PERMISSION : "grants"
    USER ||--o{ AUDIT_LOG : "triggers"
    USER }|--|| STAFF : "associated_with"
```

## Atomic Tables
- [[User Table]]
- [[Role Table]]
- [[Permission Table]]
- [[Audit Log Table]]

---
**Core Documentation**: [[Product Perspective]], [[Data Dictionary]]
**Functional Requirements**: [[Role-Based Access Control]]
