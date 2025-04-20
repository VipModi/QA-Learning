## ✅ 1. **Cookies**

### 🔹 What are Cookies?
Cookies are small pieces of data stored by the browser — used to remember **user sessions**, preferences, or login info.

### 🔹 Why are Cookies important in Automation?
- Used for **session management**
- Helps bypass login again and again
- Can verify if login/logout worked
- Can be deleted or added for specific test scenarios

### 🔧 Selenium Example (Python):

~~~
# Get all cookies
cookies = driver.get_cookies()

# Add a cookie
driver.add_cookie({"name": "session_id", "value": "123ABC"})

# Delete a cookie
driver.delete_cookie("session_id")
~~~
---

## ✅ 2. **Authentication**

### 🔹 What is Authentication?

Authentication is the process of verifying a **user’s identity** — commonly done via **login forms, tokens, or popups**.

### 🔹 Common Types:

- **Basic Auth** (username/password in URL or popup)
- **Form-based Auth** (standard login form)
- **OAuth** (Google/Facebook login)
- **Token-based Auth** (JWT)

### 🔧 Selenium – Basic Auth Example:

~~~
driver.get("https://username:password@yourapp.com/secure-page")
~~~

For more advanced flows like OAuth or JWT, you often need:

- API access (for token)
- Headless session injection (setting cookies or headers)

---

## ✅ 3. **Sessions**

### 🔹 A session is created after login and stays active for a period.

In automation, you often test:
- Session timeout
- Accessing pages without a session (should redirect to login)
- Session persistence across tabs/windows

---

## ✅ 4. **Locators**

These are **identifiers** used to find web elements. Common ones:

- ID
- Name
- Class Name
- Tag Name
- CSS Selector
- XPath

```
driver.find_element(By.ID, "username").send_keys("Vipul")
```

---

## ✅ 5. **Waits**

Waits handle **timing issues** when elements take time to load.

### Types:
- **Implicit Wait**
- **Explicit Wait**
- **Fluent Wait**

🔧 Explicit Wait Example:
```
from selenium.webdriver.support.ui import WebDriverWait
from selenium.webdriver.support import expected_conditions as EC

WebDriverWait(driver, 10).until(
    EC.presence_of_element_located((By.ID, "submit"))
)
```

---

## ✅ 6. **Alerts / Pop-ups / iFrames**

- **Alerts:** Browser messages you need to accept/dismiss
 ```
driver.switch_to.alert.accept()
```
    
- **iFrames:** HTML pages embedded in another page (you need to switch context)
    
 ```
driver.switch_to.frame("frame_id")
```
    

---

## ✅ 7. **CAPTCHA / OTP Handling**

⚠️ These are **not automatable** by default. Common solutions:

- Ask developers for **test bypass keys**
- Use **test environments** without CAPTCHA
- Mock OTP or auto-fill with fixed codes

---

## ✅ 8. **File Upload/Download**

Handled using input elements or OS-level tools:
```
driver.find_element(By.ID, "upload").send_keys("C:/path/to/file.txt")
```

---

## ✅ 9. **Headless Browsers**

Automation without opening a real browser window.
- Saves time and resources
- Often used in CI pipelines
    
```
from selenium.webdriver.chrome.options import Options
options = Options()
options.headless = True
driver = webdriver.Chrome(options=options)
```

---

## ✅ 10. **Test Data Handling**

- Static data (in code)
- Excel/CSV/JSON files
- Data from a database
- Faker libraries for dynamic data generation

---

## ✅ Summary Table:

|Concept|Purpose in Automation|
|---|---|
|Cookies|Session handling, login persistence|
|Authentication|Testing login methods (form, basic auth, tokens)|
|Sessions|Validate login/logout, access restrictions|
|Locators|Identify and interact with elements|
|Waits|Handle dynamic loading|
|Alerts/iFrames|Special UI elements requiring context switch|
|CAPTCHA/OTP|Need bypass/test hooks|
|File Upload|Test file-based features|
|Headless Mode|Faster, background testing|
|Test Data|Provide inputs, cover data-driven scenarios|