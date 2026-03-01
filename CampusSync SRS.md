---
tags: [index]
---

# CampusSync

## Software Requirements Specification (SRS)

**Version:** 1.0  
**Prepared By:** Bilim Technologies  
**Product Type:** School Management Software (Indian Education System Focus)

---
# [[Introduction and Scope|1. Introduction]]

## [[Introduction and Scope|1.1 Purpose]]

This document defines the functional and non-functional requirements for CampusSync, a fully operational School Management Software designed primarily for Indian private and semi-private educational institutions.

The system aims to provide:

- Academic management
- Examination handling
- Fee and finance management
- HR & payroll management
- Communication infrastructure
- Role-based access control

This version excludes compliance reporting, transport, library, analytics, and digital learning modules.

---
## [[Introduction and Scope|1.2 Scope]]

CampusSync will:

- Manage student lifecycle from enquiry to alumni
- Handle academic structure and timetable
- Track attendance
- Manage examinations and results
- Operate a ledger-based fee system
- Process payroll and staff management
- Enable structured communication
- Provide multi-role access control
- Support multi-school architecture

---

## [[Glossary|1.3 Definitions]]

|Term|Description|
|---|---|
|Academic Year|A defined school session (e.g., 2025–26)|
|Fee Structure|Predefined rate configuration for fee heads|
|Ledger|Transaction-based accounting record|
|RBAC|Role-Based Access Control|
|School Admin|Administrative authority for a single school|

---

# [[Product Perspective|2. Overall Description]]

## [[Product Perspective|2.1 Product Perspective]]

CampusSync is a modular ERP system designed as:

- Desktop-first (optional cloud sync)
- Multi-tenant (multiple schools)
- Academic-year isolated
- Ledger-driven financial engine

Architecture assumptions:

- Backend: Rust / Node.js (API layer)
- Database: SQLite (local) / PostgreSQL (cloud optional)
- Frontend: Web-based UI / Tauri Desktop

---

## [[User Classes|2.2 User Classes]]

|User Type|Description|
|---|---|
|Super Admin|Global system controller|
|School Admin|Full control of one institution|
|Principal|Academic supervision|
|Accountant|Finance and fee operations|
|Teacher|Academic and attendance management|
|Staff|HR-linked operations|
|Parent|Student-related viewing and communication|

---

# 3. Functional Requirements

# 3.1 Student Management

## [[Student Lifecycle|3.1.1 Student Lifecycle]]

The system shall support:

- Enquiry entry
- Admission processing
- Enrollment confirmation
- Class promotion
- Transfer certificate generation
- Alumni status marking

## [[Student Master Record|3.1.2 Student Master Record]]

Each student record shall include:

- Personal details
- Guardian details (multiple guardians allowed)
- Contact information
- Category and demographic fields
- Document upload support
- Sibling linking
- Status tracking

## [[Academic Year Isolation|3.1.3 Academic Year Isolation]]

Student academic data shall be stored per academic year without overwriting historical data.

---

# 3.2 Academic Structure

## [[Academic Configuration|3.2.1 Configuration]]

The system shall allow:

- Academic year creation
- Class and section creation
- Stream definition
- Subject creation
- Class-subject mapping
- Teacher-subject allocation
- Class teacher assignment

---

## [[Timetable Management|3.2.2 Timetable Management]]

The system shall:

- Define periods
- Define working days
- Configure holidays
- Support manual timetable creation
- Detect teacher schedule conflicts

---

# [[Attendance Management|3.3 Attendance Management]]

The system shall support:

- Daily class attendance
- Period-wise attendance
- Teacher attendance
- Leave marking
- Monthly percentage calculation
- Printable attendance reports

Attendance records shall be academic-year specific.

---

# 3.4 Examination & Result Management

## [[Exam Configuration|3.4.1 Exam Configuration]]

The system shall support:

- Multiple exam types
- Term grouping
- Subject-wise weightage
- Practical and theory separation
- Internal assessment handling
- Passing rules configuration
    

---

## [[Marks Entry|3.4.2 Marks Entry]]

The system shall:

- Allow subject-wise entry
- Support grade or marks entry
- Provide submission locking
- Track modifications via audit logs

---

## [[Result Processing|3.4.3 Result Processing]]

The system shall:

- Calculate totals and percentages
- Generate grades
- Generate rank (optional)
- Produce printable report cards
- Generate consolidated annual results

The result engine shall be rule-driven and configurable.

---

# 3.5 Fee & Financial Management

## [[Fee Structure Engine|3.5.1 Fee Structure Engine]]

The system shall allow:

- Fee group creation
- Fee head creation
- Installment definition
- Late fine rule configuration
- Concession handling
- Academic-year-specific fee versions

---

## [[Student Fee Application|3.5.2 Student Fee Application]]

The system shall:

- Map fee structure during admission
- Generate student ledger
- Support partial payments
- Calculate outstanding balances
- Apply fine automatically

---

## [[Receipt and Collection|3.5.3 Receipt & Collection]]

The system shall:

- Generate receipts
- Support receipt cancellation with log
- Track daily collection
- Provide head-wise and class-wise reports

---

## [[Financial Reporting|3.5.4 Financial Reporting]]

The system shall provide:

- Student ledger statements
- Daily collection report
- Outstanding report
- Cashbook
- Income/Expense summary

Finance must be ledger-based and transaction-driven.

---

# 3.6 HR & Payroll Management

## [[Staff Management|3.6.1 Staff Management]]

The system shall maintain:

- Staff master records
- Designation and department mapping
- Qualification details
- Document storage
- Joining and exit tracking

---

## [[Payroll Management|3.6.2 Payroll]]

The system shall:

- Define salary structure
- Generate monthly payroll
- Calculate allowances and deductions
- Generate payslips
- Track salary payments
- Manage salary advances

---

## [[Leave Management|3.6.3 Leave Management]]

The system shall:

- Define leave types
- Allow leave application
- Allow leave approval
- Track leave balance

---

# [[Communication Module|3.7 Communication Module]]

The system shall support:

- Bulk messaging
- Class-wise messaging
- Individual messaging
- Announcement board
- Circular upload
- Homework publishing

All communication actions shall be logged.

---

# [[Role-Based Access Control|3.8 Role-Based Access Control]]

The system shall:

- Define roles and permissions
- Restrict module access by role
- Restrict action-level permissions
- Maintain audit logs for sensitive actions

---

# 4. Non-Functional Requirements

## [[Non-Functional Requirements|4.1 Performance]]

- System shall support up to 5000 students per school.
- Response time shall not exceed 2 seconds for common operations.

---

## 4.2 Security

- Role-based access enforcement
- Password encryption
- Token-based authentication
- Audit trail logging
- Secure backup mechanism

---

## 4.3 Reliability

- Soft delete implementation
- Data recovery support
- Academic-year archival
- Backup export functionality

---

## 4.4 Scalability

- Multi-school support
- Modular feature expansion capability
- Cloud sync optional

---

## 4.5 Usability

- Simple UI for non-technical users
- Logical workflow structure
- Minimal training required

---

# [[Constraints and Future|5. System Constraints]]

- Must support Indian academic year model.
- Must support installment-based fee collection.
- Must operate in low-bandwidth environments.
- Must maintain historical academic records.

---

# [[Constraints and Future|6. Future Enhancements (Out of Scope for v1)]]

- Regulatory compliance exports
- Transport module
- Library management
- Advanced analytics dashboard
- LMS integration

---

# 7. Conclusion

CampusSync is designed as a robust operational School ERP system focusing on:

- Academic integrity
- Financial discipline
- Administrative efficiency
- Structured communication
- Secure role management

This SRS defines the baseline architecture for a scalable, multi-school, ledger-driven School Management System tailored for the Indian education environment.