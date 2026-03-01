---
tags: [table]
---

# Grade Scale Table

Defines the conversion rules from numeric scores to letter grades.

| Field | Type | Nullable | Description |
| --- | --- | --- | --- |
| id | INTEGER (PK) | No | Unique ID |
| grade_name | TEXT | No | e.g., "A1", "A+" |
| min_percentage | REAL | No | Lower bound (inclusive) |
| max_percentage | REAL | No | Upper bound (inclusive) |
| grade_point | REAL | Yes | GPA equivalent |

---
**Relations**:
- [[Marks Table|Applied to Marks]]

**Technical Schema**: [[Data Dictionary]]
**Functional Requirements**: [[Result Processing]]
