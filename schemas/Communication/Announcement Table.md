---
tags: [table]
---

# Announcement Table

Global or targeted notices displayed on the dashboard.

| Field | Type | Nullable | Description |
| --- | --- | --- | --- |
| id | INTEGER (PK) | No | Unique ID |
| title | TEXT | No | Notice heading |
| content | TEXT | No | Detailed body |
| target_type | TEXT | No | Global / Class / Staff / Parent |
| target_id | INTEGER | Yes | ID of specific Class or User |
| expiry_date | TEXT | Yes | ISO Date |
| creator_id | INTEGER (FK) | No | Link to [[User Table]] |

---
**Relations**:
- [[User Table|Created by User]]
- [[Class Table|May target specific Class]]

**Technical Schema**: [[Data Dictionary]]
**Functional Requirements**: [[Communication Module]]
