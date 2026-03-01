---
tags: [schema]
---

# Student Schema

This document provides a high-level index of the **Student** domain.

```mermaid
erDiagram
    STUDENT ||--o{ STUDENT_ATTENDANCE : "has"
    STUDENT ||--o{ MARKS : "obtains"
    STUDENT ||--o{ STUDENT_LEDGER : "billed_to"
    STUDENT }|--|| CLASS : "enrolled_in"
```

## Atomic Tables
- [[Student Table]]
- [[Student Attendance Table]]

---
**Core Documentation**: [[Product Perspective]], [[Data Dictionary]]
**Functional Requirements**: [[Student Master Record]], [[Student Lifecycle]]
**User Flows**: [[Admission Flow]]
