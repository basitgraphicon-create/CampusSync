---
tags: [process]
---

# Payroll Process

This document visualizes the monthly staff compensation lifecycle.

```mermaid
sequenceDiagram
    participant HR as Admin/HR
    participant ACC as Accountant
    participant S as System
    participant ST as Staff Member

    Note over HR, S: Monthly Cycle Start
    
    HR->>S: Verify [[Attendance Management|Staff Attendance]]
    S->>S: Calculate LOP (Loss of Pay) days
    
    HR->>S: Input variable adjustments (Incentives/Deductions)
    HR->>S: Trigger [[Payroll Management|Payroll Generation]]
    
    S->>S: Apply [[Staff and HR Schema|Salary Structure]]
    S->>S: Generate Employee Payslips
    
    ACC->>S: Review Payroll Summary
    ACC->>S: Approve & "Disburse Salaries"
    S->>S: Update [[Finance and Fee Schema|Expense Ledgers]]
    
    S-->>ST: Notify: "Salary Credited"
    ST->>S: View/Download Payslip
```

## Related Requirements
- [[Staff Management]]
- [[Payroll Management]]
- [[Attendance Management]]

## Related Schemas
- [[Staff and HR Schema]]
- [[Finance and Fee Schema]]
- [[Attendance Schema]]
