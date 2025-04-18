|Status Code|Category|Meaning|Usage Scenario|Example|
|---|---|---|---|---|
|**100**|1xx|Continue|Initial part of the request received; client can continue|Client sends request headers; server replies with `100 Continue` to signal readiness|
|**101**|1xx|Switching Protocols|Server is switching to another protocol (e.g., HTTP to WebSocket)|Client requests upgrade, server replies `101 Switching Protocols`|
|**200**|2xx|OK|Standard response for successful `GET`, `PUT`, `PATCH`, etc.|`GET /users/123` → returns user info|
|**201**|2xx|Created|Successful resource creation|`POST /users` → creates new user and returns new user ID|
|**202**|2xx|Accepted|Request accepted for processing, but not yet completed|`POST /jobs` → returns "Job submitted" while it's processed in the background|
|**204**|2xx|No Content|Successful operation with no response body (e.g., `DELETE`)|`DELETE /users/123` → deletes user, returns nothing|
|**301**|3xx|Moved Permanently|Resource has moved permanently; URL should be updated|`GET /old-path` → redirect to `/new-path`|
|**302**|3xx|Found (Previously “Moved Temporarily”)|Resource temporarily resides under a different URL|`GET /login` → redirect to `/dashboard` after login|
|**304**|3xx|Not Modified|Resource hasn't changed; client can use cached version|`GET /data` with `If-Modified-Since` → returns `304` if unchanged|
|**400**|4xx|Bad Request|Malformed request or validation error|`POST /users` with missing required fields → returns validation error|
|**401**|4xx|Unauthorized|Missing or invalid authentication|`GET /profile` without token → returns "Authentication required"|
|**403**|4xx|Forbidden|Authenticated but not authorized|Non-admin user accessing admin endpoint|
|**404**|4xx|Not Found|Resource does not exist|`GET /users/999` → returns "User not found"|
|**405**|4xx|Method Not Allowed|HTTP method not supported on this endpoint|`POST /users/123` (if only GET allowed) → returns method error|
|**409**|4xx|Conflict|Duplicate entry or conflicting operation|Creating a user with existing email → returns conflict error|
|**422**|4xx|Unprocessable Entity|Valid JSON but semantic/validation error|`POST /form` with weak password → returns validation error|
|**429**|4xx|Too Many Requests|Rate limit exceeded|Rapid requests to API → returns rate limit error|
|**500**|5xx|Internal Server Error|Generic server-side error|Unexpected exception while processing|
|**502**|5xx|Bad Gateway|Invalid response from upstream server|Proxy server receives invalid response from upstream server|
|**503**|5xx|Service Unavailable|Server temporarily overloaded or down|Maintenance mode or high load → returns "Service Unavailable"|
|**504**|5xx|Gateway Timeout|Timeout while waiting for upstream server response|API gateway timeout while contacting third-party service|

---

### 📌 Tips for API Testing:

- **2xx**: ✅ Success – Assert response body, status, schema.
    
- **3xx**: ↪️ Redirect – Follow or validate `Location` header.
    
- **4xx**: ❌ Client error – Validate error messages & input.
    
- **5xx**: 🚨 Server error – Validate system stability or report bug.