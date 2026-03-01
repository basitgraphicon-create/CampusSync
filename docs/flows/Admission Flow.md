---
tags: [process]
---

# Admission Flow

This document visualizes the step-by-step process of admitting a new student into CampusSync.

```mermaid
sequenceDiagram
    participant P as Parent/Guardian
    participant A as Admin/Reception
    participant S as System
    participant F as Finance/Accountant

    P->>A: Enquiry (Walk-in/Phone)
    A->>S: Log enquiry in [[Student Lifecycle|Enquiry Module]]
    S-->>A: Generate Enquiry ID
    A->>P: Provide Information/Brochure
    
    Note over P, S: If Proceeding to Admission
    
    P->>A: Submit Admission Form & Documents
    A->>S: Create master record in [[Student Master Record]]
    S-->>A: Status: "Pending Verification"
    
    A->>S: Verify [[student|Documents]]
    S-->>A: Status: "Verified"
    
    A->>F: Request Fee Payment
    F->>P: Generate Invoice based on [[Fee Structure Engine]]
    P->>F: Make Payment (Cash/Online)
    F->>S: Record transaction in [[Receipt and Collection]]
    S-->>F: Generate Receipt
    
    S->>S: Auto-assign Roll Number
    S-->>A: Status: "Enrolled"
    A->>P: Provide Welcome Kit & Admission Receipt
```

## Related Requirements
- [[Student Lifecycle]]
- [[Student Master Record]]
- [[Receipt and Collection]]

## Related Schemas
- [[student|Student Schema]]
- [[Finance and Fee Schema]]
