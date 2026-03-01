---
tags: [schema]
---

# Academic Structure Schema

This document provides a high-level index of the **Academic Structure** domain.

```mermaid
erDiagram
    ACADEMIC_YEAR ||--o{ CLASS : "contains"
    CLASS ||--o{ SECTION : "has"
    CLASS ||--o{ SUBJECT_MAPPING : "taught_in"
    TEACHER ||--o{ SUBJECT_MAPPING : "instructs"
    SUBJECT ||--o{ SUBJECT_MAPPING : "part_of"
```

## Atomic Tables
- [[Academic Year Table]]
- [[Class Table]]
- [[Section Table]]
- [[Subject Table]]
- [[Subject Mapping Table]]

---
**Core Documentation**: [[Product Perspective]], [[Data Dictionary]]
**Functional Requirements**: [[Academic Configuration]], [[Timetable Management]]
