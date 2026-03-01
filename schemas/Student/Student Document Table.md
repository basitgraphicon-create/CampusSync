---
tags: [table]
---

# Student Document Table

Tracks physical file uploads and digital verifications for students.

| Field | Type | Nullable | Description |
| --- | --- | --- | --- |
| id | INTEGER (PK) | No | Unique ID |
| student_id | INTEGER (FK) | No | Link to [[Student Table]] |
| document_type | TEXT | No | e.g., "Aadhaar Card", "TC" |
| file_path | TEXT | No | Path on local storage |
| verification_status | TEXT | No | Verified / Pending / Rejected |

---
**Relations**:
- [[Student Table|Belongs to Student]]

**Technical Schema**: [[Data Dictionary]]
**Functional Requirements**: [[Student Master Record]]
**User Flow**: [[Admission Flow]] (Document Stage)
