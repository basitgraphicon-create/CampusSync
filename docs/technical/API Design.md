---
tags: [technical]
---

# API Design

This document outlines the core API endpoint structure for CampusSync, bridging the Tauri frontend with the Rust/Laravel backend.

## 1. Student Management
| Endpoint | Method | Description | Schema Link |
| --- | --- | --- | --- |
| `/api/students/enquiry` | `POST` | Log new student enquiry | [[student|Student Schema]] |
| `/api/students/admission` | `POST` | Process admission | [[student|Student Schema]] |
| `/api/students/{id}` | `GET` | Get master record | [[student|Student Schema]] |
| `/api/students/{id}/documents`| `POST`| Upload binary docs | [[student|Student Schema]] |

## 2. Academics & Attendance
| Endpoint | Method | Description | Schema Link |
| --- | --- | --- | --- |
| `/api/academic/classes` | `GET` | List classes/sections | [[Academic Structure Schema]] |
| `/api/attendance/student` | `POST` | Batch mark attendance | [[Attendance Schema]] |
| `/api/exams/{id}/marks` | `PUT` | Batch update scores | [[Examination and Result Schema]] |

## 3. Finance
| Endpoint | Method | Description | Schema Link |
| --- | --- | --- | --- |
| `/api/finance/fee-structures`| `GET` | Get class fee rules | [[Finance and Fee Schema]] |
| `/api/finance/collect` | `POST` | Record payment | [[Finance and Fee Schema]] |
| `/api/finance/ledger/{sid}`| `GET` | Get student statement | [[Finance and Fee Schema]] |

## 4. Auth & RBAC
| Endpoint | Method | Description | Schema Link |
| --- | --- | --- | --- |
| `/api/auth/login` | `POST` | Get JWT token | [[RBAC and Security Schema]] |
| `/api/auth/profile` | `GET` | Current user context | [[RBAC and Security Schema]] |

---
**Core Documentation**: [[Product Perspective]]
