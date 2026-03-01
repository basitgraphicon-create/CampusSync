---
tags: [table]
---

# Fee Collection Table

Records individual payment transactions from parents/students.

| Field | Type | Nullable | Description |
| --- | --- | --- | --- |
| id | INTEGER (PK) | No | Unique ID |
| ledger_id | INTEGER (FK) | No | Link to [[Student Ledger Table]] |
| transaction_id | TEXT | No | e.g., TXN-2025-0001 |
| amount | REAL | No | Paid amount |
| payment_mode | TEXT | No | Cash/Cheque/Online/UPI |
| collector_id | INTEGER (FK) | No | Link to [[Staff Table]] (Accountant) |
| transaction_date | TEXT | No | ISO Date |

---
**Relations**:
- [[Student Ledger Table|Updates Balance]]
- [[Staff Table|Received by Accountant]]

**Technical Schema**: [[Data Dictionary]]
**Functional Requirements**: [[Receipt and Collection]], [[Financial Reporting]]
**User Flow**: [[Admission Flow]] (Payment Stage)
