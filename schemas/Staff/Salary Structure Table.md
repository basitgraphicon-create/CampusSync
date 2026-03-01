---
tags: [table]
---

# Salary Structure Table

Defines the compensation components for a staff member.

| Field | Type | Nullable | Description |
| --- | --- | --- | --- |
| id | INTEGER (PK) | No | Unique ID |
| staff_id | INTEGER (FK) | No | Link to [[Staff Table]] |
| basic_salary | REAL | No | Monthly base |
| hra | REAL | Yes | House Rent Allowance |
| da | REAL | Yes | Dearness Allowance |
| pf_deduction | REAL | Yes | Provident Fund contrib |

---
**Relations**:
- [[Staff Table|Belongs to Staff Member]]

**Technical Schema**: [[Data Dictionary]]
