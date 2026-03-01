---
tags: [table]
---

# Timetable Slot Table

The core scheduling record mapping academics to time.

| Field | Type | Nullable | Description |
| --- | --- | --- | --- |
| id | INTEGER (PK) | No | Unique ID |
| section_id | INTEGER (FK) | No | Link to [[Section Table]] |
| period_id | INTEGER (FK) | No | Link to [[Period Table]] |
| day_of_week | TEXT | No | Monday-Saturday |
| subject_mapping_id | INTEGER (FK) | No | Link to [[Subject Mapping Table]] |

---
**Relations**:
- [[Section Table|For Section]]
- [[Period Table|At Time]]
- [[Subject Mapping Table|Teacher + Subject]]

**Technical Schema**: [[Data Dictionary]]
**Functional Requirements**: [[Timetable Management]]
