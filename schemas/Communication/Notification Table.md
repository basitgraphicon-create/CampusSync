---
tags: [table]
---

# Notification Table

Tracks all system-generated and manual messages sent to users.

| Field | Type | Nullable | Description |
| --- | --- | --- | --- |
| id | INTEGER (PK) | No | Unique ID |
| sender_id | INTEGER (FK) | No | Link to [[User Table]] |
| receiver_id | INTEGER (FK) | No | Link to [[User Table]] |
| type | TEXT | No | SMS / Email / Push / WhatsApp |
| content | TEXT | No | Message text |
| status | TEXT | No | Sent / Delivered / Failed |
| sent_at | TEXT | No | ISO Timestamp |

---
**Relations**:
- [[User Table|Sent by User]]
- [[User Table|Received by User]]

**Technical Schema**: [[Data Dictionary]]
**Functional Requirements**: [[Communication Module]]
