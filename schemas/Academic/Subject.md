---
tags: [table]
---

# Subject Table

The global library of subjects offered by the school.

| Field | Type | Nullable | Description |
| --- | --- | --- | --- |
| id | INTEGER (PK) | No | Unique ID |
| name | TEXT | No | e.g., "Mathematics" |
| code | TEXT | Yes | Short code (e.g., MATH101) |
| type | TEXT | No | Scholastic / Co-Scholastic |

---
**Relations**:
- [[Subject Mapping Table|Mapped to Classes]]

**Technical Schema**: [[Data Dictionary]]
