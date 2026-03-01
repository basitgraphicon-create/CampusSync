---
tags: [documentation]
---

# System Constraints and Future Scope

This document tracks technical limitations and planned enhancements for CampusSync.

## System Constraints
- **Academic Model**: Must adhere to the Indian academic year cycle (typically April to March).
- **Financial Integrity**: Must maintain installment-based collections and immutable historical records.
- **Environment**: Optimized for low-bandwidth and offline desktop environments.
- **Local Storage**: Data persists primarily in a local SQLite database ([[student|Student Schema]]).

## Future Enhancements (Out of Scope for v1)
- **Transport Module**: Tracking school buses and routes.
- **Library Management**: Cataloging books and tracking issues/returns.
- **LMS Integration**: Digital learning management and online assessments.
- **Advanced Analytics**: Predictive modeling for student performance and fee collection.
- **Regulatory Exports**: Automated generation of government-mandated compliance reports.

---
**Related Schemas**: [[Academic Structure Schema]], [[Finance and Fee Schema]]
