---
tags: [table]
---

# Marks Table

Records the scores achieved by students in specific exams and subjects.

| Field | Type | Nullable | Description |
| --- | --- | --- | --- |
| id | INTEGER (PK) | No | Unique ID |
| exam_id | INTEGER (FK) | No | Link to [[Exam Definition Table]] |
| student_id | INTEGER (FK) | No | Link to [[Student Table]] |
| subject_id | INTEGER (FK) | No | Link to [[Subject Table]] |
| marks_obtained | REAL | No | Raw score |
| out_of | REAL | No | Max possible marks |
| grade_id | INTEGER (FK) | Yes | Link to [[Grade Scale Table]] |

---
**Relations**:
- [[Exam Definition Table|Part of Exam]]
- [[Student Table|Student Achieved]]
- [[Subject Table|For Subject]]
- [[Grade Scale Table|Derived Grade]]

**Technical Schema**: [[Data Dictionary]]
**Functional Requirements**: [[Marks Entry]], [[Result Processing]]
