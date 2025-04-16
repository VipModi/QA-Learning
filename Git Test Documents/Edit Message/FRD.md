# Functional Requirement Document (FRD)  
## Feature: Edit Message Functionality  

---

### 1. Functional Overview  
Allow users to modify text messages after sending, subject to constraints like time limit and number of edits.

---

### 2. Actors  
- **User (Sender)**: Can edit their own messages.
- **Receiver**: Sees the updated message with an "Edited" tag.
- **System**: Manages permissions, stores edit logs, updates clients.

---

### 3. Functional Requirements  
| ID     | Description                                                                 |
|--------|-----------------------------------------------------------------------------|
| FR-001 | System shall allow message edits within 15 minutes.                        |
| FR-002 | System shall restrict editing to the message sender.                       |
| FR-003 | System shall reflect updates in real-time across all clients.              |
| FR-004 | System shall maintain edit logs (for audit & compliance).                  |
| FR-005 | System shall display an "Edited" label in the UI.                          |
| FR-006 | System shall allow a maximum of 5 edits per message.                       |

---

### 4. User Interaction Flow  
1. User long-presses or right-clicks on their sent message.  
2. Selects "Edit" from the context menu.  
3. Updates the message text and submits.  
4. UI reflects the new text with an "Edited" indicator.  
5. Edit history logged in backend.

---

### 5. Non-Functional Requirements  
- Edit action should complete in < 300ms.
- Should not block message sync or delivery.
- Must support scalability to millions of concurrent users.

---

### 6. Error Handling  
| Scenario                              | System Behavior                             |
|--------------------------------------|---------------------------------------------|
| User tries to edit after 15 mins     | Show error: "Edit window expired."          |
| Message edit limit exceeded          | Show error: "Maximum edits reached."        |
| Edit fails due to network error      | Retry or prompt user                        |
