---
tags: [schema]
---

# Communication Schema

This document provides a high-level index of the **Communication & Messaging** domain.

```mermaid
erDiagram
    USER ||--o{ NOTIFICATION : "sends/receives"
    USER ||--o{ ANNOUNCEMENT : "creates"
    CLASS ||--o{ ANNOUNCEMENT : "targets"
    CLASS ||--o{ HOMEWORK : "assigned_to"
```

## Atomic Tables
- [[Notification Table]]
- [[Announcement Table]]
- [[Homework Table]]

---
**Core Documentation**: [[Product Perspective]], [[Data Dictionary]]
**Functional Requirements**: [[Communication Module]]
