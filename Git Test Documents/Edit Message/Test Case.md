# Test Cases – Edit Message Feature  

| TC ID  | Scenario                       | Input                | Expected Result                                   | Priority |
| ------ | ------------------------------ | -------------------- | ------------------------------------------------- | -------- |
| TC-001 | Edit message within 15 minutes | Valid message text   | Message gets updated and shows "Edited" label     | High     |
| TC-002 | Edit after 15 minutes          | Expired message      | Error: "Edit window expired"                      | High     |
| TC-003 | Exceed max edit count          | 6th edit attempt     | Error: "Maximum edits reached"                    | High     |
| TC-004 | Edit by another user           | Non-owner tries edit | Error: "Permission denied"                        | High     |
| TC-005 | UI display after edit          | Edited message       | Message content updated, "Edited" tag is shown    | Medium   |
| TC-006 | Real-time sync across devices  | Edit on one device   | Updated message reflects on all logged-in devices | High     |

## Different Types of Testcase: 

### **1. Positive Test Cases**

Positive test cases validate that the system behaves as expected when everything works correctly.

| TC ID   | Description                                 | Input                            | Expected Result                                   | Priority |
|---------|---------------------------------------------|----------------------------------|---------------------------------------------------|----------|
| TC-001  | Edit message within allowed 15 minutes     | Edit message within 15 mins      | Message edited successfully                       | High     |
| TC-002  | Display 'Edited' label after editing        | Edit message after 10 mins       | 'Edited' label is displayed next to the message   | Medium   |
| TC-003  | Edit a message when the user is the sender | Valid message, within 15 minutes | Message edited successfully                       | High     |
| TC-004  | Edit a message in real-time across devices | Edit message on one device       | Message syncs and updates on other devices        | High     |

### **2. Negative Test Cases**

Negative test cases verify that the system behaves correctly when given invalid or incorrect input

| TC ID   | Description                                 | Input                            | Expected Result                                   | Priority |
|---------|---------------------------------------------|----------------------------------|---------------------------------------------------|----------|
| TC-005  | Attempt to edit a message after 15 minutes  | Edit message after 16 mins       | Error message: "Edit window expired"              | High     |
| TC-006  | Edit message by a non-sender user          | Non-sender tries to edit message | Error message: "You can only edit your own message" | High     |
| TC-007  | Edit a message when the edit limit exceeds | 6th edit attempt                 | Error message: "Maximum 5 edits allowed"          | High     |
| TC-008  | Attempt to edit a message with empty content | Empty message content            | Error message: "Message content cannot be empty"  | Medium   |

### **3. Accessibility Test Cases**

Accessibility test cases ensure that the feature is usable by all users, including those with disabilities

| TC ID   | Description                                    | Input                            | Expected Result                                    | Priority |
|---------|------------------------------------------------|----------------------------------|----------------------------------------------------|----------|
| TC-009  | Test screen reader functionality for message edit button | Edit button                     | Screen reader announces: "Edit message"            | Medium   |
| TC-010  | Ensure edit button is accessible by keyboard   | Tab through message options      | Focus should highlight the "Edit" option clearly   | High     |
| TC-011  | Verify color contrast for "Edited" label       | Edited message label             | "Edited" label should have sufficient contrast for readability | Medium   |
| TC-012  | Test for voice control and interaction        | Voice command "Edit"             | System should respond with the message edit option | High     |

### **4. Edge Case Test Cases**

Edge cases test the behavior of the system in unusual or extreme conditions.

| TC ID   | Description                                    | Input                            | Expected Result                                    | Priority |
|---------|------------------------------------------------|----------------------------------|----------------------------------------------------|----------|
| TC-013  | Edit a message exactly after 15 minutes       | Edit message exactly after 15 mins | Error message: "Edit window expired"              | High     |
| TC-014  | User tries to edit a message immediately after sending | Edit message immediately after sending | Message edited successfully                        | Medium   |
| TC-015  | User attempts to edit multiple messages in a row | Multiple consecutive edits       | Each edit should be successful up to 5 edits        | Medium   |
| TC-016  | Edit a message during a network disconnect    | Edit message while offline       | Error message: "You need to be online to edit the message" | High     |

### **5. Security Test Cases**

Security test cases ensure that the feature is secure and does not introduce vulnerabilities

| TC ID   | Description                                    | Input                            | Expected Result                                    | Priority |
|---------|------------------------------------------------|----------------------------------|----------------------------------------------------|----------|
| TC-017  | Validate that unauthorized users cannot edit messages | Non-sender attempts to edit message | Error message: "You can only edit your own message" | High     |
| TC-018  | Ensure messages are encrypted during editing   | Edit a message                   | Message content should be encrypted in transit      | High     |
| TC-019  | Verify role-based access control for message edit | Admin and non-admin user         | Admin should be able to edit any message; Non-admin only their own | High     |

### **6. Performance Test Cases**

Performance test cases verify the speed and responsiveness of the system under load

| TC ID   | Description                                    | Input                            | Expected Result                                    | Priority |
|---------|------------------------------------------------|----------------------------------|----------------------------------------------------|----------|
| TC-020  | Test editing a message under load conditions   | Edit message during peak usage  | Edit should still work within 1-2 seconds          | High     |
| TC-021  | Test editing multiple messages simultaneously  | Edit 10 messages at once         | System should handle the load without crashing     | High     |

### **7. Usability Test Cases**

Usability test cases ensure that the feature is user-friendly and easy to understand

| TC ID   | Description                                    | Input                            | Expected Result                                    | Priority |
|---------|------------------------------------------------|----------------------------------|----------------------------------------------------|----------|
| TC-022  | Ensure the Edit button is clearly visible      | View message options             | Edit button should be easy to locate and use       | High     |
| TC-023  | Ensure the "Edited" label is clearly visible   | Edit a message                   | The "Edited" label should be clearly visible next to the message | High     |

### **8. Regression Test Cases**

Regression test cases validate that the new changes haven't broken existing functionality.

| TC ID   | Description                                    | Input                            | Expected Result                                    | Priority |
|---------|------------------------------------------------|----------------------------------|----------------------------------------------------|----------|
| TC-024  | Ensure no other functionality is broken after fixing the bug | Send, edit, and delete messages | All message-related functionalities should work as expected | High     |
| TC-025  | Verify that messages can still be sent after editing | Send and edit a message          | Message should send and edit without errors        | High     |

---

### **9. Localization Test Cases**

Localization test cases ensure that the feature works correctly in different languages and regions.

| TC ID   | Description                                    | Input                            | Expected Result                                    | Priority |
|---------|------------------------------------------------|----------------------------------|----------------------------------------------------|----------|
| TC-026  | Ensure proper translation of "Edit" button     | View message options in French   | Button should be translated as "Modifier" in French | Medium   |
| TC-027  | Verify "Edited" label is localized correctly   | Edit message in Spanish          | "Edited" label should appear as "Editado" in Spanish | Medium   |
