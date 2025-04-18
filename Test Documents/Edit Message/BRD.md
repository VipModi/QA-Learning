# Business Requirement Document (BRD)  
## Feature: Edit Message Functionality  

---

### 1. Document Control  
| Version | Date       | Author       | Description             |
|---------|------------|--------------|-------------------------|
| 1.0     | 2025-04-15 | Vipul Modi   | Initial draft           |

---

### 2. Purpose  
Enable users to edit sent text messages within a limited time to correct mistakes or update content.

---

### 3. Scope  
- Applies to 1:1 and group chats.
- Text messages only.
- Platforms: iOS, Android, Web, Desktop.
- Editing allowed within 15 minutes.

---

### 4. Business Objectives  
- Reduce friction due to typos or incorrect messages.
- Increase user satisfaction and app engagement.
- Align with competitor offerings.

---

### 5. Stakeholders  
| Role               | Name/Team           |
|--------------------|---------------------|
| Product Manager    | [Product Owner]     |
| QA Team            | [Quality Team]      |
| Engineering Lead   | [Dev Lead]          |
| Legal/Compliance   | [Compliance Team]   |

---

### 6. Assumptions  
- Only the sender can edit their messages.
- Users are online and authenticated.
- Edit timestamps are tracked.

---

### 7. Constraints  
- Editing allowed for 15 minutes after send time.
- Max 5 edits per message.
- No media message editing.
- "Edited" label shown in UI.

---

### 8. High-Level Requirements  
| ID     | Requirement                                                                 |
|--------|------------------------------------------------------------------------------|
| BR-001 | Users can edit text messages within 15 minutes.                             |
| BR-002 | Edited message appears across all devices.                                  |
| BR-003 | UI indicates the message has been edited.                                   |
| BR-004 | Backend stores edit logs for compliance.                                    |
| BR-005 | No further edits allowed after time or edit limit is exceeded.              |

---

### 9. Out of Scope  
- Multimedia edits (image/video).
- Viewing previous versions (not MVP).
- Message deletion (covered separately).

---

### 10. Dependencies  
- Backend APIs.
- Frontend platform implementations.
- Real-time message delivery (WebSocket).

---

### 11. Risks & Mitigations  
| Risk                                      | Mitigation                                  |
|-------------------------------------------|---------------------------------------------|
| Misuse of edit for deception              | Limit edit window and track versions        |
| Platform inconsistency                    | Use shared design guidelines and testing    |
