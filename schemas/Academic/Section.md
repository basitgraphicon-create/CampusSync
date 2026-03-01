---
tags: [table]
---

# Section Table

Divides classes into manageable batches.

| Field | Type | Nullable | Description |
| --- | --- | --- | --- |
| id | INTEGER (PK) | No | Unique ID |
| class_id | INTEGER (FK) | No | Link to [[Class Table]] |
| name | TEXT | No | e.g., "A", "Batch-1" |
| strength_limit | INTEGER | Yes | Max capacity |

---
**Relations**:
- [[Class Table|Belongs to Class]]
- [[Student Table|Enrolled Students]]

**Technical Schema**: [[Data Dictionary]]
