---
tags: [table]
---

# Fee Head Table

Defines specific components of a fee structure (e.g., Tuition, Lab).

| Field | Type | Nullable | Description |
| --- | --- | --- | --- |
| id | INTEGER (PK) | No | Unique ID |
| fee_structure_id | INTEGER (FK) | No | Link to [[Fee Structure Table]] |
| name | TEXT | No | e.g., "Quarterly Tuition" |
| amount | REAL | No | Specific head amount |
| priority | INTEGER | Yes | Order of payment application |

---
**Relations**:
- [[Fee Structure Table|Belongs to Structure]]
- [[Student Ledger Table|Invoiced to Students]]

**Technical Schema**: [[Data Dictionary]]
