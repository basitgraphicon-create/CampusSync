---
tags: [table]
---

# User Table

Defines the credentials and identity for system access.

| Field | Type | Nullable | Description |
| --- | --- | --- | --- |
| id | INTEGER (PK) | No | Unique ID |
| username | TEXT | No | Unique login name |
| password_hash | TEXT | No | Encrypted secret |
| role_id | INTEGER (FK) | No | Link to [[Role Table]] |
| staff_id | INTEGER (FK) | Yes | Link to [[Staff Table]] (if employee) |
| student_id | INTEGER (FK) | Yes | Link to [[Student Table]] (if parent/student) |
| is_active | BOOLEAN | No | Access toggle |

---
**Relations**:
- [[Role Table|Assigned Role]]
- [[Staff Table|Linked Staff]]
- [[Student Table|Linked Student]]
- [[Audit Log Table|Triggers Actions]]

**Technical Schema**: [[Data Dictionary]]
**Functional Requirements**: [[Role-Based Access Control]]
