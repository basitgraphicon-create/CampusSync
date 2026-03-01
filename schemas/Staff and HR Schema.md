---
tags: [schema]
---

# Staff and HR Schema

This document provides a high-level index of the **Staff and Human Resources** domain.

```mermaid
erDiagram
    STAFF ||--o{ SALARY_STRUCTURE : "has"
    STAFF ||--o{ LEAVE_BALANCE : "has"
    STAFF ||--o{ STAFF_ATTENDANCE : "records"
    DEPARTMENT ||--o{ STAFF : "contains"
```

## Atomic Tables
- [[Staff Table]]
- [[Salary Structure Table]]
- [[Leave Balance Table]]

---
**Core Documentation**: [[Product Perspective]], [[Data Dictionary]]
**Functional Requirements**: [[Staff Management]], [[Payroll Management]], [[Leave Management]]
