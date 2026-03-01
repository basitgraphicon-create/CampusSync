---
tags: [schema]
---

# Detailed Data Dictionary

This document provides low-level technical specifications for critical fields across all schemas.

## 1. Shared Field Constraints
| Data Type | Validation / Pattern | Default |
| --- | --- | --- |
| **Email** | `^[a-zA-Z0-9._%+-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,}$` | NULL |
| **Mobile** | `^[6-9]\d{9}$` (Indian Standards) | NULL |
| **Currency** | Decimal(12,2) (Positive values only) | 0.00 |
| **Status** | Enum (Module specific) | 'Active' |

## 2. Module Specific Specs
### Student Module
- `gr_number`: **TEXT (Unique)**. Max 20 chars. Mandatory.
- `profile_image`: **TEXT (Path)**. Store as relative path.
- `blood_group`: **ENUM** (A+, A-, B+, B-, O+, O-, AB+, AB-).

### Finance Module
- `transaction_id`: **TEXT (Unique)**. e.g., `TXN-2025-00001`.
- `payment_mode`: **ENUM** (Cash, Cheque, Online, Transfer, UPI).

### Staff Module
- `aadhaar_number`: **TEXT (Masked)**. 12 digits.
- `uan_number`: **TEXT**. 12 digits (for PF).

---
**Technical Schemas**: [[student|Student Schema]], [[Finance and Fee Schema]], [[Staff and HR Schema]]
