### 🔹 What is Database Testing?
Database Testing is the process of validating data stored in the database and ensuring the accuracy, integrity, and consistency of the data by executing queries.

It's mainly divided into:
1. **Data Validity Testing**
2. **Data Integrity Testing**
3. **Database Performance Testing**
4. **Database Security Testing**
5. **Testing of Stored Procedures, Triggers, and Views**

---
### 🔹 Why is it Important?
Let’s say your app (like a messaging or social media platform) displays a list of messages. These are fetched from a backend DB. Any discrepancy (e.g., a deleted message still showing) indicates a backend failure — and that’s where DB testing ensures frontend and backend data consistency.

---
### 🔹 Key Concepts to Learn

#### 1. **Database Schema Testing**
- Verifies:
    - Tables, columns, types, constraints (like NOT NULL, UNIQUE)
    - Primary key, foreign key constraints
- Example: If a `user_id` is a primary key in the `users` table, verify no duplicates exist.

#### 2. **Data Integrity Testing**
- Ensures relationships between tables are maintained.
- Example: A `message` table must not contain `sender_id` values that don’t exist in the `users` table.

#### 3. **CRUD Operation Testing (Create, Read, Update, Delete)**
- Create data ➝ check if it's correctly inserted.
- Update data ➝ verify changes reflect.
- Delete data ➝ ensure it's removed.
- Example: After sending a message, verify it appears in the `messages` table.

#### 4. **Stored Procedure / Trigger Testing**
- Write tests to validate the logic written in stored procedures.
- Use test data to call procedures and compare output.
- Example: A stored procedure auto-deletes messages older than 30 days. Validate if it works.

#### 5. **Data Validity Testing**
- Check for correct data types and value ranges.
- Example: A `phone_number` field should not accept letters.

#### 6. **Database Testing Tools**
- **SQL clients:** MySQL Workbench, pgAdmin, Oracle SQL Developer
- **Automation:** Selenium (for UI) + Python (for DB checks using `pyodbc`, `mysql.connector`, etc.)

---

### 🔹 Sample SQL Queries You Might Use

```
-- Check if the user exists
SELECT * FROM users WHERE username = 'vipulmodi';

-- Verify message is inserted after sending
SELECT * FROM messages WHERE sender_id = 101 AND content = 'Hello!';

-- Join check between messages and users
SELECT m.message_id, u.username 
FROM messages m 
JOIN users u ON m.sender_id = u.user_id;
```

---

### 🔹 Real-Time Scenario (Related to Your Domain)

📱 Let’s say on Messenger:
- A user blocks another user.
- You validate:
    - Block entry exists in `user_blocks` table
    - Blocked user can’t message again
    - Notification or alert is stored in `user_logs`

This would involve UI, API (if exposed), and DB validation — **end-to-end testing**.