---
tags: [table]
---

# Student Table

The master record for all students enrolled in the institution.

| Field | Type | Nullable | Description |
| --- | --- | --- | --- |
| id | INTEGER (PK) | No | Unique internal ID |
| gr_number | TEXT | No | Unique Permanent ID |
| full_name | TEXT | No | Legal name |
| academic_year_id | INTEGER (FK) | No | Link to [[Academic Year Table]] |
| class_id | INTEGER (FK) | No | Link to [[Class Table]] |
| section_id | INTEGER (FK) | No | Link to [[Section Table]] |
| dob | TEXT | No | Date of birth |
| gender | TEXT | No | Male / Female / Other |
| father_name | TEXT | No | Guardian name |
| admission_date | TEXT | No | ISO Date |
| status | TEXT | No | Active / Alumnus / Left |

---
**Relations**:
- [[Academic Year Table|Admission Year]]
- [[Class Table|Current Class]]
- [[Section Table|Current Section批次]]
- [[Student Attendance Table|Attendance Records]]
- [[Student Ledger Table|Financial Records]]
- [[Marks Table|Achieved Marks]]
- [[Student Document Table|Uploaded Files]]

**Technical Schema**: [[Data Dictionary]]
**Functional Requirements**: [[Student Master Record]], [[Student Lifecycle]]
**User Flow**: [[Admission Flow]]
