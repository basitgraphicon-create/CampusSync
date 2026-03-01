---
tags: [table]
---

# Leave Balance Table

Tracks the annual leave entitlements and usage for staff.

| Field | Type | Nullable | Description |
| --- | --- | --- | --- |
| id | INTEGER (PK) | No | Unique ID |
| staff_id | INTEGER (FK) | No | Link to [[Staff Table]] |
| leave_type | TEXT | No | e.g., "CL", "SL", "EL" |
| total_entitled | INTEGER | No | Yearly quota |
| used_leaves | REAL | No | Count of leaves taken |
| balance | REAL | Derived | Remaining leaves |

---
**Relations**:
- [[Staff Table|Belongs to Staff Member]]

**Technical Schema**: [[Data Dictionary]]
**Functional Requirements**: [[Leave Management]]
