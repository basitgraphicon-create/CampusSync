---
tags: [table]
---

# Staff Attendance Table

Tracks the daily presence of employees for payroll and performance.

| Field | Type | Nullable | Description |
| --- | --- | --- | --- |
| id | INTEGER (PK) | No | Unique ID |
| staff_id | INTEGER (FK) | No | Link to [[Staff Table]] |
| status | TEXT | No | Present / Absent / On Leave / LOP |
| date | TEXT | No | ISO Date |
| in_time | TEXT | Yes | Check-in timestamp |
| out_time | TEXT | Yes | Check-out timestamp |

---
**Relations**:
- [[Staff Table|Employee Record]]

**Technical Schema**: [[Data Dictionary]]
**Functional Requirements**: [[Attendance Management]], [[Payroll Management]]
**User Flow**: [[Payroll Process]]
