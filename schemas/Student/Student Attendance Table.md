---
tags: [table]
---

# Student Attendance Table

Tracks the daily presence of students in their respective classes.

| Field | Type | Nullable | Description |
| --- | --- | --- | --- |
| id | INTEGER (PK) | No | Unique ID |
| student_id | INTEGER (FK) | No | Link to [[Student Table]] |
| status | TEXT | No | Present / Absent / Late / Sick |
| date | TEXT | No | ISO Date |
| remarks | TEXT | Yes | Optional note for absence |

---
**Relations**:
- [[Student Table|Student Record]]
- [[Academic Year Table|Academic Context]]

**Technical Schema**: [[Data Dictionary]]
**Functional Requirements**: [[Attendance Management]]
