## 🔍 **What is API Testing?**

**API Testing** is a type of software testing that focuses on testing **Application Programming Interfaces (APIs)** directly to:

- **Validate functionality**
- **Ensure reliability**
- **Check performance**
- **Enforce security**

---

### ✅ In simple terms:

> **API testing checks whether the backend services (APIs) work as expected when given certain inputs.**

Instead of testing the UI (buttons, screens), you test the **actual logic and data exchange** between software systems.

---

## 🚀 Example of What You Test in API:

- Is the API **returning the right response** for a request?    
- Does it handle **errors properly** (e.g., invalid ID)?
- Does it enforce **authentication** (401, 403)?
- Is it following **RESTful principles**?
- How fast is it? (performance)
    

---

## 📘 Common Terms Used in API Testing

| Term                                        | Explanation                                          | Example                                       |
| ------------------------------------------- | ---------------------------------------------------- | --------------------------------------------- |
| **API (Application Programming Interface)** | A set of rules that allow apps to talk to each other | REST API, GraphQL API                         |
| **Endpoint**                                | A specific path to access a resource in an API       | `/users/123`, `/login`                        |
| **URI (Uniform Resource Identifier)**       | Full address to access an endpoint                   | `https://api.example.com/users/123`           |
| **Base URL**                                | The common part of all endpoints                     | `https://api.example.com`                     |
| **Method (HTTP Verb)**                      | Type of operation you want to perform                | `GET`, `POST`, `PUT`, `DELETE`                |
| **Request**                                 | What the client sends to the server                  | Includes method, endpoint, headers, body      |
| **Response**                                | What the server sends back                           | Includes status code, headers, body           |
| **Status Code**                             | Numeric code indicating result of request            | `200 OK`, `404 Not Found`, `401 Unauthorized` |
| **Payload (Body)**                          | The actual data sent in a request (usually JSON)     | `{"name": "Vipul"}`                           |
| **Headers**                                 | Metadata sent along with the request or response     | `Content-Type`, `Authorization`               |
| **Authentication**                          | Verifying the identity of a user or app              | API key, Bearer Token, OAuth                  |
| **Assertions**                              | Conditions to validate test results                  | `Status code = 200`, `email != null`          |
| **Collection (in Postman)**                 | A group of saved API requests                        | Useful for organizing and sharing tests       |

---

## 🧪 Example Request Breakdown

Let's say you're testing the following API:

```
POST https://api.example.com/users
```

- **Base URL:** `https://api.example.com`
- **Endpoint:** `/users`
- **Method:** `POST`
- **Request Body (Payload):**
    
```
{   
	"name": "Vipul Modi",
	"email": "vipul@example.com" 
}
```

- **Expected Response:**

```
Status: 201 Created 
{
	"id": 123,
	"message": "User created successfully" 
}
```

---

## 🎯 Why is API Testing Important?

- Finds bugs early (before UI is built)
- Faster and more stable than UI tests
- Helps test logic, security, performance
- Crucial for microservices and backend-heavy apps