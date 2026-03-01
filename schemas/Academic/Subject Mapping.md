---
tags: [table]
---

# Subject Mapping Table

Assigns subjects and teachers to specific classes.

| Field | Type | Nullable | Description |
| --- | --- | --- | --- |
| id | INTEGER (PK) | No | Unique ID |
| class_id | INTEGER (FK) | No | Link to [[Class Table]] |
| subject_id | INTEGER (FK) | No | Link to [[Subject Table]] |
| teacher_id | INTEGER (FK) | Yes | Link to [[Staff Table]] |
| marks_weightage | REAL | Yes | Default % contrib to total |

---
**Relations**:
- [[Class Table|Belongs to Class]]
- [[Subject Table|Refers to Subject]]
- [[Staff Table|Taught by Teacher]]

**Technical Schema**: [[Data Dictionary]]
