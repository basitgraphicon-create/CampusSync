---
tags: [table]
---

# Academic Year Table

Defines the highest level of temporal partitioning in CampusSync.

| Field | Type | Nullable | Description |
| --- | --- | --- | --- |
| id | INTEGER (PK) | No | Unique ID |
| name | TEXT | No | e.g., "2025-26" |
| start_date | TEXT | No | ISO Date |
| end_date | TEXT | No | ISO Date |
| is_active | BOOLEAN | No | Current active year |

---
**Relations**:
- [[Class Table|Has many Classes]]

**Technical Schema**: [[Data Dictionary]]
