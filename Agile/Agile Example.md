#agile #example
### 🔁 Agile Flow with QA Involvement

| Sprint Phase         | QA Involvement                                                                                                                                                                                                                                              |
| -------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Backlog Grooming** | QA joins, reads the user story:  <br>“As a user, I want to unsend a message within 5 mins so I can delete messages I regret.”  <br>QA asks: What happens after 5 minutes? What if the user is offline?                                                      |
| **Sprint Planning**  | QA helps estimate the effort and defines Acceptance Criteria:  <br>✔ Message should disappear from sender and receiver chat.  <br>✔ Should not be unsendable after 5 mins.  <br>✔ Confirmation toast should appear: “Message unsent.”                       |
| **During Sprint**    | While dev is coding:  <br>🔹 QA writes test cases  <br>🔹 Discuss edge cases (group chats, media messages, etc.)  <br>🔹 Prepares for manual and regression testing                                                                                         |
| **Testing Begins**   | Dev commits code → QA starts testing:  <br>✔ Functional test (send → unsend within 5 mins)  <br>✔ Negative test (try after 6 mins → should fail)  <br>✔ Cross-platform (iOS, Android, Web)  <br>✔ Regression check: does this affect message deletion logs? |
| **Bug Found?**       | QA raises a JIRA ticket:  <br>“[BUG] Message unsends after 6 mins instead of 5 mins – timer not working properly.”                                                                                                                                          |
| **Sprint Review**    | QA shows working flow and testing coverage                                                                                                                                                                                                                  |
| **Retrospective**    | QA shares feedback:  <br>“Test cases were not finalized before dev started — let’s align better next time.”                                                                                                                                                 |

---

## 🗂️ 2. Simple Agile Board Layout

Here’s a typical **Agile board layout** with example tasks you might see during a sprint:

```
┌────────────┬───────────────┬──────────────┬────────────┬───────────┐
│   To Do    │ In Progress   │ In Review    │   Testing  │   Done    │
├────────────┼───────────────┼──────────────┼────────────┼───────────┤
│ Unsend Msg │ Unread Badge  │ Emoji React  │ Delete Chat│ Logout Bug│
│ Block User │               │              │            │           │
└────────────┴───────────────┴──────────────┴────────────┴───────────┘
```

### Column Meaning:

- **To Do:** Stories/tasks pulled for this sprint but not started yet.
- **In Progress:** Dev is actively working.
- **In Review:** Code complete, waiting for peer review or merge.
- **Testing:** QA is verifying the changes.
- **Done:** Fully tested and accepted.
    

---

### 🔍 Example QA Tasks on the Board:

| Story                | Task                          | Status        |
| -------------------- | ----------------------------- | ------------- |
| “Unsend Message”     | Functional testing (manual)   | 🟡 In Testing |
| “Block User”         | Write test cases              | 🔵 To Do      |
| “Unread Badge Count” | Regression test on Android    | 🟢 Done       |
| “Delete Chat”        | Verify deletion in group chat | 🟡 In Testing |