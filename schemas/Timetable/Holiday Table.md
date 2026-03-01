---
tags: [table]
---

# Holiday Table

Records school events, holidays, and non-working days.

| Field | Type | Nullable | Description |
| --- | --- | --- | --- |
| id | INTEGER (PK) | No | Unique ID |
| academic_year_id | INTEGER (FK) | No | Link to [[Academic Year Table]] |
| name | TEXT | No | e.g., "Diwali Break" |
| start_date | TEXT | No | ISO Date |
| end_date | TEXT | No | ISO Date |
| is_academic_holiday | BOOLEAN | No | Affects student attendance |
| is_staff_holiday | BOOLEAN | No | Affects payroll |

---
**Relations**:
- [[Academic Year Table|Academic Context]]

**Technical Schema**: [[Data Dictionary]]
**Functional Requirements**: [[Timetable Management]]
