### 📋 Commonly Used HTTP Methods – Full Comparison

|**Method**|**Purpose**|**Safe**|**Idempotent**|**Cacheable**|**Usage Behavior**|**Example**|
|---|---|---|---|---|---|---|
|**GET**|Retrieve data from the server|✅ Yes|✅ Yes|✅ Yes|Doesn’t change anything on the server; only fetches data|`GET /users/123` → Fetch details of user with ID 123|
|**POST**|Send data to create a new resource|❌ No|❌ No|❌ No|Creates a new record; each call may result in a new resource|`POST /users` with `{ "name": "Vipul" }` → Creates a new user|
|**PUT**|Replace an existing resource|❌ No|✅ Yes|❌ No|Full update: replaces the entire resource with the data provided|`PUT /users/123` with full user details to update the entire user record|
|**PATCH**|Partially update a resource|❌ No|✅ Usually|❌ No|Partial update: modifies only the fields provided, not the whole resource|`PATCH /users/123` with `{ "email": "vipul@newmail.com" }`|
|**DELETE**|Remove a resource from the server|❌ No|✅ Yes|❌ No|Deletes the resource; repeat calls have no further effect once deleted|`DELETE /users/123` → Deletes user with ID 123|

---

### 🧠 Key Terms Explained

- **Safe:** The request doesn’t modify data on the server.
    
- **Idempotent:** Making the same request multiple times results in the same outcome.
    
- **Cacheable:** Can the response be stored and reused by the browser or intermediary?

### 🔄 PUT vs POST vs PATCH – Key Differences

| **Aspect**           | **POST** 🆕                                   | **PUT** 🔁                                | **PATCH** ✏️                              |
| -------------------- | --------------------------------------------- | ----------------------------------------- | ----------------------------------------- |
| **Purpose**          | Create a **new** resource                     | **Replace** an existing resource          | **Partially update** an existing resource |
| **Idempotent**       | ❌ No (multiple requests = multiple creations) | ✅ Yes (multiple requests = same result)   | ✅ Yes (generally)                         |
| **Creates Resource** | ✅ Yes                                         | ✅ Sometimes (if not already exists)       | ❌ No                                      |
| **Updates Resource** | ❌ No                                          | ✅ Yes (full update)                       | ✅ Yes (partial update)                    |
| **Request Body**     | Only the fields needed to create              | Full representation of the resource       | Only the fields to be updated             |
| **Typical Use Case** | Submit a form, create user/post               | Replace full user profile                 | Change a single field (e.g., email)       |
| **Example Endpoint** | `POST /users`                                 | `PUT /users/123`                          | `PATCH /users/123`                        |
| **Example Body**     | `{ "name": "Vipul" }`                         | `{ "name": "Vipul", "email": "v@x.com" }` | `{ "email": "v@x.com" }`                  |