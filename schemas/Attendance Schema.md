---
tags: [schema]
---

# Attendance Schema

This document provides a high-level index of the **Attendance** domain.

```mermaid
erDiagram
    STUDENT ||--o{ STUDENT_ATTENDANCE : "marks"
    STAFF ||--o{ STAFF_ATTENDANCE : "marks"
    ACADEMIC_YEAR ||--o{ STUDENT_ATTENDANCE : "context"
```

## Atomic Tables
- [[Student Attendance Table]]
- [[Staff Attendance Table]]

---
**Core Documentation**: [[Product Perspective]], [[Data Dictionary]]
**Functional Requirements**: [[Attendance Management]]
