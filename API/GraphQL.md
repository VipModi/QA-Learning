## 🔍 **What is GraphQL?**

**GraphQL** is a **query language** and **runtime** for APIs, developed by **Facebook** (now Meta).  
It’s an alternative to REST APIs — more flexible and efficient.

---

### ✅ **In Simple Terms:**

> With GraphQL, the **client decides** what data it needs — no more, no less.

Instead of multiple REST endpoints, you have **just one endpoint**, and you send a query specifying exactly what you want.

---

### 🧠 **Key Difference from REST:**

|Feature|REST|GraphQL|
|---|---|---|
|Data Fetching|Multiple endpoints|Single endpoint|
|Over-fetching|Common (gets extra data)|No|
|Under-fetching|Needs multiple calls|No|
|Versioning|Often needed|Not required|
|Query structure|Fixed by server|Defined by client|

---

## 🧪 **GraphQL Example**

Let’s say you want user info.

### 🧱 REST:

You might need:
- `GET /users/123` → gives all user info
- `GET /users/123/posts` → to get their posts
- `GET /users/123/friends` → to get their friends

### ⚙️ GraphQL (Single request):
```
{
  user(id: 123) {
    name
    email
    posts {
      title
    }
    friends {
      name
    }
  }
}
```
### ✅ Response:
```
{
  "data": {
    "user": {
      "name": "Vipul Modi",
      "email": "vipul@example.com",
      "posts": [
        { "title": "Hello World" }
      ],
      "friends": [
        { "name": "Raj" }
      ]
    }
  }
}
```
---

## 🔧 **Core Components of GraphQL:**

|Term|Meaning|
|---|---|
|**Query**|Read data|
|**Mutation**|Modify data (create, update, delete)|
|**Subscription**|Real-time updates|
|**Schema**|Defines what data is available and how it’s structured|
|**Resolver**|Backend logic that fetches the requested data|

---

## 📌 **Why Use GraphQL?**

- 🚀 Faster apps — get only what you need
- 🧹 Cleaner code — no chaining multiple REST calls
- 🔁 Real-time support via Subscriptions
- 🔒 Strongly typed system (great for error catching)
- 📲 Better for mobile — reduces data load
    

---

## ⚠️ When Not to Use:

- If you're working with **simple APIs** that don’t need flexibility
- If you don’t need **custom queries**
- When the team isn’t comfortable learning new syntax