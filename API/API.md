## 🔍 **What is an API?**

**API** stands for **Application Programming Interface**.

> It is a **set of rules and protocols** that allows two software applications to **communicate** with each other.

---

### ✅ **In simple terms:**

> **API = A waiter at a restaurant.**  
> You (the client) tell the waiter (API) what you want. The waiter takes your request to the kitchen (server) and brings back your food (response).

---

### 💡 **Real-Life Example:**

You’re using a **weather app** on your phone:
- The app (client) sends a request to a **weather API**
- The API talks to a weather server
- The server sends back the temperature, which the app shows you

---

## 🔧 **Technical Example:**

Let’s say there is a **User API** for an app like Instagram:
### Request:

```
GET https://api.example.com/users/123
```

- **GET** → Method (asking for data)
- **/users/123** → Resource (user with ID 123)
### Response:

```
{   
	"id": 123,   
	"name": "Vipul Modi",   
	"email": "vipul@example.com" 
}
```

This whole exchange is handled by the API.

---

## 🧱 **Why APIs are important:**

|Feature|Benefit|
|---|---|
|**Communication**|APIs connect frontend and backend (or app to app)|
|**Automation**|Enables apps to work without manual input|
|**Security**|Clients don’t access databases directly—only through secure APIs|
|**Integration**|APIs allow systems (e.g., Facebook login in 3rd-party apps) to work together|

---

## 🧪 Where APIs are Used:

- Mobile apps (e.g., WhatsApp using chat APIs)
- Web apps (e.g., Amazon showing product data)
- Payment systems (e.g., UPI, Stripe, Razorpay APIs)
- Messaging services
- Social media platforms (e.g., posting on Instagram using an API)

---

### 📌 Summary:

> **API is a bridge** between different software applications.  
> It lets one software **request something**, and another **respond with data or action**.


## ⚙️ **How API Works**

Think of an **API** as a **middleman** between a **client** (like an app) and a **server** (where data lives). Here's the basic flow:

---

### 🔁 **API Workflow (Step-by-Step)**

1. **Client sends a request**  
    → For example: “Get user data” or “Create new order”
    
2. **API receives the request**  
    → Checks if it’s valid, secure, and well-formed
    
3. **Server processes the request**  
    → Fetches data or performs logic (e.g., add user to database)
    
4. **API sends the response back**  
    → With a **status code** (200, 404, etc.) and optional data
    

---

## 🧠 **Analogy:**

Imagine ordering food at Zomato:

- You select your meal (Client)
- The app sends it to the restaurant (API Request)
- Restaurant confirms the order (Server)
- The app shows your delivery time (API Response)

---

## 📚 **Types of APIs**

There are multiple ways APIs can be designed and shared. Here’s a table for clarity:

|API Type|Description|Example|Protocol|
|---|---|---|---|
|**Open API (Public API)**|Available to everyone; no restrictions|Weather API, COVID stats API|Mostly HTTP/REST|
|**Internal API (Private API)**|Used within a company for internal systems|HR software talks to Payroll system|HTTP, REST, GraphQL, etc.|
|**Partner API**|Shared with specific partners with permission|Payment gateway shared with e-commerce app|Requires API key or authentication|
|**Composite API**|Combines multiple APIs into one call|A single API returns user info + posts + friends list|REST, GraphQL|
|**REST API**|Resource-based, uses HTTP methods|`GET /users`, `POST /login`|HTTP|
|**SOAP API**|XML-based, strict format, used in older systems|Banking & legacy enterprise systems|SOAP (XML over HTTP)|
|**GraphQL API**|Flexible queries; client defines structure|Ask for only needed fields: name + email|HTTP|
|**WebSocket API**|Two-way live communication (real-time)|Chat apps, stock tickers|WebSockets|

---

### 🔧 Common API Protocols

| Protocol       | Used in                                     |
| -------------- | ------------------------------------------- |
| **HTTP/HTTPS** | Most REST, GraphQL APIs                     |
| **WebSocket**  | Real-time communication                     |
| **SOAP**       | Enterprise systems (XML-heavy)              |
| **gRPC**       | High-performance APIs (e.g., microservices) |

---

## 🧪 In API Testing, You Focus On:

- Testing different **API types** (REST, GraphQL, etc.)
- Validating **requests/responses**
- Checking **error handling**
- Ensuring **security and authorization**
- Testing **performance** (latency, speed)