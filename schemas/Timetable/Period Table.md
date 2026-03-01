---
tags: [table]
---

# Period Table

Defines the time slots (bells) for a school day.

| Field | Type | Nullable | Description |
| --- | --- | --- | --- |
| id | INTEGER (PK) | No | Unique ID |
| name | TEXT | No | e.g., "Period 1", "Lunch Break" |
| start_time | TEXT | No | HH:MM |
| end_time | TEXT | No | HH:MM |
| is_break | BOOLEAN | No | Flag for non-academic slots |

---
**Relations**:
- [[Timetable Slot Table|Used in Timetable]]

**Technical Schema**: [[Data Dictionary]]
**Functional Requirements**: [[Timetable Management]]
