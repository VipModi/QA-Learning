# Bug Report – Edit Message

| ID      | Title                      | Steps to Reproduce                     | Expected Result              | Actual Result               | Severity |
| ------- | -------------------------- | -------------------------------------- | ---------------------------- | --------------------------- | -------- |
| BUG-001 | Edit option not visible    | Long-press sent message > Context menu | Edit option should be shown  | Edit option missing         | High     |
| BUG-002 | Edit allowed after 15 mins | Wait >15 mins > Try to edit            | Error: "Edit window expired" | Message edited successfully | Critical |
| BUG-003 | No "Edited" label in UI    | Edit a message                         | "Edited" label should appear | No label shown              | Medium   |

### **Bug Report – Edit Message: "Edit allowed after 15 mins"**

---
#### **Bug ID**: BUG-002
#### **Title**: Edit allowed after 15 minutes
#### **Reported By**: Vipul Modi
#### **Severity**: Critical
#### **Priority**: High
#### **Status**: Open
#### **Assignee**: Dev Team
---

### **Description**

When a user attempts to edit a message after the 15-minute window has expired, the system incorrectly allows the edit operation. This issue violates the feature's requirement to prevent edits beyond 15 minutes.

---

### **Steps to Reproduce**

1. **Login** to the app as `user123`.
2. **Send a text message** (e.g., "Hello, how are you?") at `12:00 PM`.
3. Wait for **16 minutes** (until `12:16 PM`).
4. **Tap on the sent message** to trigger the message options.
5. **Select "Edit"** from the options menu.
6. The system should show an error message: **"Edit window expired. You cannot edit this message after 15 minutes."**
    

**Expected Behavior**:  
The system should display an error message and prevent the user from editing the message after the 15-minute period.

**Actual Behavior**:  
The system allows the message to be edited even after 16 minutes, which violates the business rule.

---

### **Example Logs**

Here are the logs for the scenario where a user was able to edit the message after 15 minutes:

#### **Timestamp: 12:16 PM**

```
2025-04-15 12:16:05 [INFO] - User 'user123' initiated the 'Edit' operation for message ID 987654.
2025-04-15 12:16:06 [DEBUG] - Message ID 987654 was sent at 12:00 PM, current timestamp 12:16 PM.
2025-04-15 12:16:06 [DEBUG] - Time difference: 16 minutes. Edit time window exceeded (should be 15 minutes).
2025-04-15 12:16:07 [INFO] - Backend validation check for 'Edit Window Expiry' bypassed.
2025-04-15 12:16:08 [INFO] - Edit operation completed for message ID 987654.
2025-04-15 12:16:09 [DEBUG] - Edited message saved successfully with new content: "Hello, how are you doing?"
2025-04-15 12:16:10 [INFO] - 'Edited' label was added to the message ID 987654.
```

#### **Analysis of Logs**

- The system correctly checks the time difference between the message sent time (`12:00 PM`) and the current time (`12:16 PM`), which is 16 minutes.
- Despite the time exceeding the 15-minute window, the backend validation check for "Edit Window Expiry" is **bypassed**, and the edit operation is allowed.
- The message is edited successfully, and an "Edited" label is added, indicating that the functionality was executed without errors.
    
---
### **Root Cause**

The issue occurred because the backend logic responsible for validating the edit time window did not enforce the 15-minute constraint correctly. The validation check for the message edit expiration was bypassed due to a missing condition in the backend API, allowing edits after the allowed time.

---
### **Impact**

- **Policy Violation**: This issue directly violates the platform's messaging policy, which limits message editing to 15 minutes to ensure accountability.
- **User Trust**: Users may exploit this to alter messages even after significant delays, leading to potential misuse.
- **Reputation**: This issue can negatively impact the product's reliability and user experience if not fixed promptly.

---
### **Screenshots/Screen Recording**

(Optional – Add a screenshot of the app showing the 'Edit' option after the 15-minute time window, or a screen recording of the bug being reproduced.)

---

### **Suggested Fix**

1. **Backend Fix**:
    - Add a time validation check in the backend API to ensure that users can only edit messages within the 15-minute window.
    - The backend should return a response like: **"Edit window expired. You cannot edit this message after 15 minutes."** if the edit window has expired.
        
2. **Frontend Handling**:
    - The frontend should handle this error gracefully by showing the error message and disabling the edit option if the time constraint is violated.
        
3. **Testing**:
    - Test this fix across multiple devices (mobile, web) and edge cases (e.g., when the user attempts to edit exactly after 15 minutes, just before 15 minutes, and after 16 minutes).
        

---

### **Additional Notes**
- This issue was discovered during a routine QA regression test for the Edit Message feature.
- The bug is **critical** and needs to be resolved in the next release.