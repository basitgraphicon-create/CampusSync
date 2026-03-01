---
tags: [technical]
---

# Frontend Architecture

This document defines the UI/UX framework and design system for the CampusSync desktop application.

## 1. Design Tokens (Visual Identity)
| Token | Variable | Value/Description |
| --- | --- | --- |
| **Primary Color** | `--brand-blue` | `#2563EB` (Premium Professional) |
| **Secondary Color** | `--accent-slate`| `#64748B` |
| **Success** | `--success-green` | `#22C55E` |
| **Danger** | `--error-red` | `#EF4444` |
| **Typography** | `--font-main` | `Inter, system-ui` |

## 2. Core UI Components
- **`SidebarNavigation`**: Deep-linked role-based menu.
- **`DataTable`**: Reusable grid with multi-column filtering and export.
- **`StatCard`**: Overview metrics (e.g., Today's Collection, Absentee Count).
- **`ModalEngine`**: Unified handler for additions/edits (Admission, Fee Payment).

## 3. Tech Stack
- **Framework**: Vite + React
- **Styling**: Vanilla CSS (Premium Custom Design)
- **State Management**: Zustand / React Query (for API caching)
- **Desktop Bridge**: Tauri API (for file system and local storage)

---
**Core Documentation**: [[Product Perspective]], [[Non-Functional Requirements]]
