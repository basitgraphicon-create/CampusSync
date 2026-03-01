---
tags: [table]
---

# Role Table

Defines a group of permissions within the system.

| Field | Type | Nullable | Description |
| --- | --- | --- | --- |
| id | INTEGER (PK) | No | Unique ID |
| name | TEXT | No | e.g., "Teacher", "Accountant" |
| description | TEXT | Yes | Purpose of the role |

---
**Relations**:
- [[User Table|Assigned to Users]]
- [[Permission Table|Grants Permissions]]

**Technical Schema**: [[Data Dictionary]]
**Functional Requirements**: [[Role-Based Access Control]]
**User Documentation**: [[User Classes]]
