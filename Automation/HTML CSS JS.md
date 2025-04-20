## ✅ **1. HTML (HyperText Markup Language)**

HTML is the **structure** of a web page.  
As a test engineer, you’ll need to inspect and interact with HTML elements.

### 🔹 Common HTML Elements:

```
<input type="text" id="username" />
<button class="login-btn">Login</button>
<a href="/profile">Profile</a>
```
### 🔹 Important Attributes for Automation:

|Attribute|Use in Automation|
|---|---|
|`id`|Best for locating elements|
|`class`|Often used but less unique|
|`name`|Common in forms|
|`type`|Identifies input types|
|`placeholder`|Helpful for visible hints|
|`value`|Holds element's value|
|`href`, `src`|Link and image sources|

---

## ✅ **2. CSS (Cascading Style Sheets)**

CSS is used for **styling** web pages, but in automation, you use CSS **selectors** to find elements.

### 🔹 Examples of CSS Selectors:

```
#username           → Selects element with id="username"
.login-btn          → Selects element with class="login-btn"
input[type="text"]  → Selects input fields of type text
```
These are very helpful when writing locators in tools like Selenium.

---

## ✅ **3. JavaScript (JS)**

JavaScript adds **functionality/behavior** to a web page.  
In test automation, JS is important for:

- Waiting for JS to load content (e.g., dynamic lists)
- Handling alerts, pop-ups, modals
- Executing custom JS via WebDriver (if needed)
    

### 🔹 Common JavaScript Behaviors You’ll See:

- Dynamic buttons (enabled/disabled)
- AJAX calls (content loads without page refresh)
- On-click or on-hover actions
    

### 🔹 Example:

```
document.getElementById('username').value = 'Vipul';
```

This sets the value of an input box using JS — sometimes used in automation to inject values.

---

### 🧪 How This Helps in Automation:

|Task|Related Tech Used|
|---|---|
|Finding elements|HTML & CSS selectors|
|Waiting for content load|JavaScript (AJAX)|
|Handling dynamic elements|JavaScript|
|Writing locators|HTML attributes|

---

### 🔍 Real Example (Login Page):

```
<form id="loginForm">
  <input type="text" id="username" name="user" />
  <input type="password" id="password" name="pass" />
  <button class="login-btn" type="submit">Login</button>
</form>
```

In Selenium:
```
driver.find_element(By.ID, "username").send_keys("vipul")
driver.find_element(By.ID, "password").send_keys("password123")
driver.find_element(By.CLASS_NAME, "login-btn").click()
```