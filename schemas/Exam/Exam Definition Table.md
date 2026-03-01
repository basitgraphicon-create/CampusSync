---
tags: [table]
---

# Exam Definition Table

Defines the structure and timing of an examination session.

| Field | Type | Nullable | Description |
| --- | --- | --- | --- |
| id | INTEGER (PK) | No | Unique ID |
| academic_year_id | INTEGER (FK) | No | Link to [[Academic Year Table]] |
| name | TEXT | No | e.g., "First Term Exam" |
| start_date | TEXT | No | ISO Date |
| end_date | TEXT | No | ISO Date |
| status | TEXT | No | Scheduled / Ongoing / Completed |

---
**Relations**:
- [[Marks Table|Contains Marks]]
- [[Academic Year Table|Belongs to Academic Year]]

**Technical Schema**: [[Data Dictionary]]
**Functional Requirements**: [[Exam Configuration]]
**User Flow**: [[Examination Cycle]]
