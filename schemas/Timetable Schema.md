---
tags: [schema]
---

# Timetable Schema

This document provides a high-level index of the **Timetable and Scheduling** domain.

```mermaid
erDiagram
    SECTION ||--o{ TIMETABLE_SLOT : "scheduled_for"
    PERIOD ||--o{ TIMETABLE_SLOT : "defines_time"
    SUBJECT_MAPPING ||--o{ TIMETABLE_SLOT : "teaches_what"
    ACADEMIC_YEAR ||--o{ HOLIDAY : "context"
```

## Atomic Tables
- [[Period Table]]
- [[Timetable Slot Table]]
- [[Holiday Table]]

---
**Core Documentation**: [[Product Perspective]], [[Data Dictionary]]
**Functional Requirements**: [[Timetable Management]]
