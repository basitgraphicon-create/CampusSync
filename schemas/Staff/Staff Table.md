---
tags: [table]
---

# Staff Table

The central repository for all employees of the institution.

| Field | Type | Nullable | Description |
| --- | --- | --- | --- |
| id | INTEGER (PK) | No | Unique employee ID |
| full_name | TEXT | No | Full legal name |
| designation | TEXT | No | e.g., "Principal", "Teacher" |
| department | TEXT | Yes | e.g., "Science", "Admin" |
| dob | TEXT | No | Date of birth |
| joining_date | TEXT | No | Date of joining |
| status | TEXT | No | Active / Resigned / Suspended |
| mobile_number | TEXT | No | Primary mobile |
| email | TEXT | Yes | Email address |

---
**Relations**:
- [[Class Table|May be a Class Teacher]]
- [[Subject Mapping Table|May be a Subject Teacher]]
- [[Salary Structure Table|Has a Salary Structure]]
- [[Leave Balance Table|Has Leave Balances]]

**Technical Schema**: [[Data Dictionary]]
