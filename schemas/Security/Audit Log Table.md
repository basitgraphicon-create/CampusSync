---
tags: [table]
---

# Audit Log Table

Records a chronological trail of sensitive data modifications.

| Field | Type | Nullable | Description |
| --- | --- | --- | --- |
| id | INTEGER (PK) | No | Unique ID |
| user_id | INTEGER (FK) | No | Link to [[User Table]] |
| action | TEXT | No | e.g., "MARK_UPLOAD", "FEE_COLLECT" |
| table_name | TEXT | No | Affected table |
| record_id | INTEGER | No | Affected record |
| old_values | TEXT | Yes | JSON snapshot before change |
| new_values | TEXT | Yes | JSON snapshot after change |
| timestamp | TEXT | No | ISO Date Time |

---
**Relations**:
- [[User Table|Performed by User]]

**Technical Schema**: [[Data Dictionary]]
**Functional Requirements**: [[Financial Reporting|Audit Oversight]]
