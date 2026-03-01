---
tags: [process]
---

# Examination Cycle

This document outlines the end-to-end process of conducting exams and generating results.

```mermaid
sequenceDiagram
    participant AD as Admin/Principal
    participant T as Teacher
    participant S as System
    participant P as Parent/Student

    AD->>S: Configure [[Exam Configuration|Exam Schedule]]
    AD->>S: Define Passing Rules & [[Examination and Result Schema|Grade Scales]]
    S-->>T: Notify: "Marks Entry Open"
    
    Note over T, S: After Exam Completion
    
    T->>S: Enter scores in [[Marks Entry]]
    S->>S: Validate scores vs [[Academic Structure Schema|Max Marks]]
    T->>S: Submit & [[Role-Based Access Control|Lock Marks]]
    
    S->>S: Auto-calculate Totals & [[Result Processing|Grades]]
    AD->>S: Review Consolidated Results
    AD->>S: Verify & "Publish Results"
    
    S-->>P: Notify via [[Communication Module]]
    P->>S: View/Download Report Card
```

## Related Requirements
- [[Exam Configuration]]
- [[Marks Entry]]
- [[Result Processing]]

## Related Schemas
- [[Examination and Result Schema]]
- [[Academic Structure Schema]]
