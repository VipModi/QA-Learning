### 🔍 **What is REST?**

**REST** stands for **Representational State Transfer**.  
It is an **architectural style** used for designing **networked applications**, especially **web services**.

When people say **REST API**, they mean an API (Application Programming Interface) that follows REST principles, usually using **HTTP** to access and manipulate data.

---

### 📦 **Key Concepts of REST:**

|Concept|Description|
|---|---|
|**Client-Server**|Client (like Postman or a mobile app) sends requests, server handles logic and data|
|**Stateless**|Every request is independent; server doesn’t remember previous requests|
|**Cacheable**|Responses can be cached to improve performance|
|**Uniform Interface**|Uses standard methods like `GET`, `POST`, `PUT`, `DELETE`|
|**Resources**|Everything is treated as a resource (e.g., `users`, `orders`, `messages`)|
|**Representation**|Resources are sent as representations (usually **JSON** or **XML**)|

---

### 🧪 **Example REST API Request:**

```
GET /users/123
```

- **Method**: `GET` → Fetch data
- **Endpoint**: `/users/123` → Specific user with ID 123
- **Response**:
```
{
  "id": 123,
  "name": "Vipul Modi",
  "email": "vipul@example.com"
}
```

---

### 🔁 **Common HTTP Methods in REST:**

|Method|Usage|
|---|---|
|`GET`|Retrieve data (read-only)|
|`POST`|Create new resource|
|`PUT`|Update existing resource (entire)|
|`PATCH`|Update part of a resource|
|`DELETE`|Remove a resource|

---

### ✅ **Why REST is Popular:**

- Easy to understand
- Lightweight
- Works over HTTP
- Language-independent
- Supported by tools like Postman, Swagger, etc.