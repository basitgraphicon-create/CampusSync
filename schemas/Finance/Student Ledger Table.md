---
tags: [table]
---

# Student Ledger Table

The financial statement for an individual student's account.

| Field | Type | Nullable | Description |
| --- | --- | --- | --- |
| id | INTEGER (PK) | No | Unique ID |
| student_id | INTEGER (FK) | No | Link to [[Student Table]] |
| fee_head_id | INTEGER (FK) | No | Charge component |
| amount_due | REAL | No | Total billed |
| amount_paid | REAL | No | Total collected |
| balance | REAL | Derived | Net outstanding |

---
**Relations**:
- [[Student Table|Student Record]]
- [[Fee Head Table|Charged Component]]
- [[Fee Collection Table|Payments received]]

**Technical Schema**: [[Data Dictionary]]
**Functional Requirements**: [[Student Fee Application]]
