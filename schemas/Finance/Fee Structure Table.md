---
tags: [table]
---

# Fee Structure Table

Configures the total fee liability for a class for an academic year.

| Field | Type | Nullable | Description |
| --- | --- | --- | --- |
| id | INTEGER (PK) | No | Unique ID |
| class_id | INTEGER (FK) | No | Link to [[Class Table]] |
| total_amount | REAL | No | Total annual liability |
| academic_year_id | INTEGER (FK) | No | Link to [[Academic Year Table]] |

---
**Relations**:
- [[Fee Head Table|Contains components]]
- [[Class Table|Applied to Class]]

**Technical Schema**: [[Data Dictionary]]
**Functional Requirements**: [[Fee Structure Engine]]
