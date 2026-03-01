---
tags: [table]
---

# Class Table

Defines the educational levels supported by the institution.

| Field | Type | Nullable | Description |
| --- | --- | --- | --- |
| id | INTEGER (PK) | No | Unique ID |
| academic_year_id | INTEGER (FK) | No | Link to [[Academic Year Table]] |
| name | TEXT | No | e.g., "Class 10" |
| level | INTEGER | Yes | Numeric order for sorting |
| class_teacher_id | INTEGER (FK) | Yes | Link to [[Staff Table]] |

---
**Relations**:
- [[Academic Year Table|Belongs to Academic Year]]
- [[Section Table|Has many Sections]]
- [[Subject Mapping Table|Has many Subjects]]
- [[Student Table|Contains many Students]]

**Technical Schema**: [[Data Dictionary]]
