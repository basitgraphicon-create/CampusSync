---
tags: [documentation]
---

# Non-Functional Requirements

These requirements define the system's performance, security, and quality attributes.

## Performance
- **Capacity**: Support up to 5,000 students per institution.
- **Latency**: UI response time under 2 seconds for standard operations.
- **Optimization**: Minimal asset loading for low-bandwidth environments.

## Security
- **RBAC**: Strict role-based enforcement at the field and action levels ([[Role-Based Access Control]]).
- **Authentication**: Token-based security and password encryption.
- **Privacy**: Isolation of student data by school and academic year.
- **Logging**: Comprehensive [[Audit Log]] system for all sensitive data changes.

## Reliability
- **Soft Deletes**: Preventing unintentional data loss.
- **Recovery**: Automated daily local backups.
- **Integrity**: Transaction-based [[Ledger]] operations for financial accuracy.

## Scalability & Usability
- **Architecture**: Modular design for future feature expansion.
- **Offline-First**: Reliable local operation (Tauri Desktop) with optional cloud synchronization.
- **Accessibility**: Simple, intuitive UI designed for non-technical users.

---
**Related Schemas**: [[RBAC and Security Schema]]
