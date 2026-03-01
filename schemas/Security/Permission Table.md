---
tags: [table]
---

# Permission Table

Defines granular access rights to individual modules or actions.

| Field | Type | Nullable | Description |
| --- | --- | --- | --- |
| id | INTEGER (PK) | No | Unique ID |
| role_id | INTEGER (FK) | No | Link to [[Role Table]] |
| module | TEXT | No | e.g., "Finance", "Attendance" |
| action | TEXT | No | "View", "Create", "Delete", "Print" |

---
**Relations**:
- [[Role Table|Belongs to Role]]

**Technical Schema**: [[Data Dictionary]]
