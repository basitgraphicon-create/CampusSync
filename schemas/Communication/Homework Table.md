---
tags: [table]
---

# Homework Table

Daily academic assignments published by teachers.

| Field | Type | Nullable | Description |
| --- | --- | --- | --- |
| id | INTEGER (PK) | No | Unique ID |
| class_id | INTEGER (FK) | No | Link to [[Class Table]] |
| subject_id | INTEGER (FK) | No | Link to [[Subject Table]] |
| title | TEXT | No | Assignment title |
| description | TEXT | No | Detailed instructions |
| submission_date | TEXT | Yes | Deadline |
| teacher_id | INTEGER (FK) | No | Link to [[Staff Table]] |

---
**Relations**:
- [[Class Table|Assigned to Class]]
- [[Subject Table|For Subject]]
- [[Staff Table|Published by Teacher]]

**Technical Schema**: [[Data Dictionary]]
**Functional Requirements**: [[Communication Module]]
