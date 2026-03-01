---
tags: [documentation]
---

# Product Perspective

CampusSync is a modular ERP system designed for educational institutions. It is built as a **Desktop-first (optional cloud sync)** application using the **Tauri framework**.

## Architecture Overview
- **Backend**: Rust / Node.js (API layer)
- **Database**: SQLite (local) / PostgreSQL (cloud optional)
- **Frontend**: Web-based UI within a Tauri Desktop wrapper
- **Multi-tenant**: Supports multiple schools within a single system instance.
- **Academic Year Isolation**: Every piece of data is linked to an [[Academic Year Isolation|Academic Year]].

## Core Principles
1. **Ledger-driven Finance**: Every financial transaction must be traceable to a specific [[Student Ledger|Student]] or Institutional Ledger.
2. **Offline-first**: The system must operate reliably without constant internet connectivity.
3. **RBAC Security**: Access is strictly controlled via [[Role-Based Access Control|Roles and Permissions]].

## Technical Layers
- [[API Design|API Endpoint Structure]]
- [[Frontend Architecture|UI/UX Framework]]

---
**Core Documentation**: [[Glossary]], [[User Classes]], [[Non-Functional Requirements]]
