---
tags: [implementation]
---

# Migration Guide

A guide for transitioning school data from legacy systems or manual registers into CampusSync.

## 1. Pre-Migration Checklist
- [ ] Export existing data to CSV/Excel.
- [ ] Normalize student names to title case.
- [ ] Map legacy "Classes" to [[Academic Structure Schema|CampusSync Class IDs]].
- [ ] Verify [[student|GR Numbers]] uniqueness.

## 2. Bulk Upload Templates
### Student Master Data
Columns: `gr_number`, `full_name`, `dob`, `gender`, `father_name`, `mobile_number`, `class_id`.

### Opening Balances (Finance)
Columns: `student_id`, `fee_head_id`, `balance_due`.

## 3. Validation Rules
- **Date Format**: Must be ISO 8601 (`YYYY-MM-DD`).
- **Mobile**: Strict 10-digit validation.
- **Enumerations**: Gender must be `Male`, `Female`, or `Other`.

## 4. Migration Steps
1. **Academic Setup**: Create the [[Academic Structure Schema|Academic Year]] and Classes first.
2. **Staff Setup**: Import [[Staff and HR Schema|Staff Records]] to assign class teachers.
3. **Student Import**: Upload the student master records.
4. **Fee Initialization**: Apply fee structures to the newly imported students.

---
**Core Documentation**: [[Product Perspective]], [[Introduction and Scope]]
