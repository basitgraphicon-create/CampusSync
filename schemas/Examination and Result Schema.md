---
tags: [schema]
---

# Examination and Result Schema

This document provides a high-level index of the **Examination and Grading** domain.

```mermaid
erDiagram
    EXAM ||--o{ MARKS : "contains"
    STUDENT ||--o{ MARKS : "achieves"
    SUBJECT ||--o{ MARKS : "recorded_for"
    GRADE_SCALE ||--o{ MARKS : "evaluates"
```


# 3. GradeScale
Defines the mapping between percentage ranges and letter grades.

---

# Relations & Obsidian Links
---
**Technical Schema**: [[Data Dictionary]]
**Related Schemas**:
    - [[student|Student Schema]]
    - [[Academic Structure Schema]]
- **Functional Requirements**:
    - [[Exam Configuration]]
    - [[Marks Entry]]
    - [[Result Processing]]

---

# Suggested SQLite Table Structure
`exams`, `marks`, `grade_scales`
