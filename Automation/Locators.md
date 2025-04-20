## ✅ What are Locators?

Locators are **strategies** used to uniquely identify elements on a webpage's DOM.

> 🎯 They help automation tools simulate user actions: click, type, select, etc.

---

## ✅ Common Selenium Locator Types (with Examples)

| Locator Type           | Description                               | Example                                                                |
| ---------------------- | ----------------------------------------- | ---------------------------------------------------------------------- |
| `By.id`                | Finds element by unique `id` attribute    | `driver.find_element(By.ID, "username")`                               |
| `By.name`              | Finds element by `name` attribute         | `driver.find_element(By.NAME, "email")`                                |
| `By.class_name`        | Finds element by CSS class name           | `driver.find_element(By.CLASS_NAME, "btn")`                            |
| `By.tag_name`          | Finds element by tag (e.g. `input`, `a`)  | `driver.find_element(By.TAG_NAME, "h1")`                               |
| `By.link_text`         | Finds link by its exact text              | `driver.find_element(By.LINK_TEXT, "Login")`                           |
| `By.partial_link_text` | Finds link by partial match               | `driver.find_element(By.PARTIAL_LINK_TEXT, "Log")`                     |
| `By.css_selector`      | Uses CSS syntax to find complex elements  | `driver.find_element(By.CSS_SELECTOR, "div.login input[type='text']")` |
| `By.xpath`             | Uses XML-style path to target any element | `driver.find_element(By.XPATH, "//input[@type='password']")`           |

---

## 🔍 Sample HTML to Understand Locators

```
<form id="loginForm">
  <input id="username" name="user" type="text" />
  <input name="password" type="password" />
  <button class="btn submit">Login</button>
  <a href="/forgot" id="forgotLink">Forgot Password?</a>
</form>
```

### 🔹 Locators for Above HTML:

|What you want to find|Best locator example|
|---|---|
|Username field|`By.ID, "username"` or `By.NAME, "user"`|
|Password field|`By.NAME, "password"`|
|Login button|`By.CLASS_NAME, "submit"` or use CSS: `"button.submit"`|
|Forgot Password link|`By.ID, "forgotLink"` or `By.LINK_TEXT, "Forgot Password?"`|

---

## ✅ CSS Selector vs XPath — Quick Comparison

|Feature|CSS Selector|XPath|
|---|---|---|
|Speed|Faster|Slightly slower|
|Syntax|Clean, web dev friendly|Complex, powerful|
|Text search|❌ Not supported|✅ Supported with `text()`|
|Traverse backward|❌ Not supported|✅ Supported (parent, sibling, etc.)|
|Example|`div#main input[type='text']`|`//div[@id='main']//input[@type='text']`|

> 💡 Use **CSS for performance** and **XPath for flexibility**.

---

## 🛡️ Best Practices for Locators

- ✅ Prefer **ID** if available (most stable)
- ✅ Use **unique attributes** (`data-test`, `data-id`, etc.)
- ❌ Avoid long XPaths with indexes (e.g., `//div[3]/div[2]/input`)
- ✅ Create **custom attributes** for automation if working with devs
- ✅ Use **Explicit Waits** for dynamic elements

---

## 🚀 Bonus: Advanced XPath Examples

| Goal                     | XPath                                                         |
| ------------------------ | ------------------------------------------------------------- |
| Element with exact text  | `//button[text()='Login']`                                    |
| Input with type password | `//input[@type='password']`                                   |
| First input inside form  | `//form//input[1]`                                            |
| Label next to a field    | `//label[normalize-space()='Email']/following-sibling::input` |

## ✅ 1. **ID Locator**

### 📘 Description:

Selects an element by its **`id` attribute**, which should be **unique** on the page.

### 🧾 HTML:

```
<input type="text" id="username" />
```

### ✅ Selenium:

```
driver.find_element(By.ID, "username").send_keys("Vipul")
```

### ✅ Use When:
- The element has a unique, stable `id`.
- Fastest and most reliable method.

---

## ✅ 2. **Name Locator**

### 📘 Description:

Finds element by the **`name` attribute**. Common in forms.

### 🧾 HTML:

html

CopyEdit

`<input type="password" name="user_password" />`

### ✅ Selenium:

python

CopyEdit

`driver.find_element(By.NAME, "user_password").send_keys("123456")`

### 🔍 Notes:

- Less reliable than `id` — multiple elements might have the same name.
    

---

## ✅ 3. **Class Name Locator**

### 📘 Description:

Finds element(s) by the **CSS class** name.

### 🧾 HTML:

html

CopyEdit

`<button class="btn submit">Login</button>`

### ✅ Selenium:

python

CopyEdit

`driver.find_element(By.CLASS_NAME, "submit").click()`

### ⚠️ Caution:

- If there are **multiple classes**, it looks for exact match unless handled carefully.
    
- Can return the **first match only**.
    

---

## ✅ 4. **Tag Name Locator**

### 📘 Description:

Finds elements by HTML **tag** (like `input`, `a`, `h1`, etc.)

### 🧾 HTML:

html

CopyEdit

`<h1>Welcome</h1>`

### ✅ Selenium:

python

CopyEdit

`driver.find_element(By.TAG_NAME, "h1")`

### 🎯 Use For:

- Getting all links: `driver.find_elements(By.TAG_NAME, "a")`
    
- Titles, paragraphs, etc.
    

---

## ✅ 5. **Link Text Locator**

### 📘 Description:

Finds links using their **exact text**.

### 🧾 HTML:

html

CopyEdit

`<a href="/forgot">Forgot Password?</a>`

### ✅ Selenium:

python

CopyEdit

`driver.find_element(By.LINK_TEXT, "Forgot Password?").click()`

### ⚠️ Tips:

- Works only with `<a>` (anchor) tags.
    
- Text must match exactly.
    

---

## ✅ 6. **Partial Link Text Locator**

### 📘 Description:

Like `link_text` but allows **partial match**.

### ✅ Selenium:

python

CopyEdit

`driver.find_element(By.PARTIAL_LINK_TEXT, "Forgot").click()`

### 🎯 Use When:

- Link text is long or may change partially.
    

---

## ✅ 7. **CSS Selector**

### 📘 Description:

Most powerful and fast method. Uses **CSS rules** to find elements.

### 🧾 HTML:

html

CopyEdit

`<input type="email" class="form-control" id="email" />`

### ✅ Selenium:

python

CopyEdit

`driver.find_element(By.CSS_SELECTOR, "#email").send_keys("vipul@example.com")`

### 🔍 Examples:

|CSS Selector|Meaning|
|---|---|
|`#email`|ID = email|
|`.form-control`|Class = form-control|
|`input[type='email']`|Input tag with type=email|
|`form input:first-child`|First input inside a form|
|`div > span.highlight`|Child span with class highlight in div|

### 🎯 Advantages:

- Fast
    
- Clean syntax
    
- Good for most cases
    

---

## ✅ 8. **XPath**

### 📘 Description:

Very powerful — can traverse **forward and backward** in the DOM. Uses **XML-like path**.

### 🧾 HTML:

html

CopyEdit

`<input type="text" name="username" />`

### ✅ Selenium:

python

CopyEdit

`driver.find_element(By.XPATH, "//input[@name='username']").send_keys("Vipul")`

### 🔍 Examples:

|XPath|Meaning|
|---|---|
|`//input`|All input tags|
|`//input[@type='text']`|Input where type=text|
|`//form[@id='login']//input`|All input inside form with id='login'|
|`//label[text()='Email']/following::input[1]`|First input after the label "Email"|

### 🎯 When to Use:

- No unique ID or class
    
- Need to locate based on **text**, **hierarchy**, or **attributes**
    
- Need **dynamic** element handling
    

---

## ✅ Summary Table

|Locator Type|Use When...|Example Code Snippet|
|---|---|---|
|`By.ID`|Element has a unique `id`|`find_element(By.ID, "username")`|
|`By.NAME`|Form input fields with name|`find_element(By.NAME, "password")`|
|`By.CLASS_NAME`|Class is unique or you're finding groups|`find_element(By.CLASS_NAME, "submit")`|
|`By.TAG_NAME`|Working with headings, links, lists|`find_elements(By.TAG_NAME, "a")`|
|`By.LINK_TEXT`|Link text is **exact match**|`find_element(By.LINK_TEXT, "Forgot Password?")`|
|`By.PARTIAL_LINK_TEXT`|Only part of the link is stable|`find_element(By.PARTIAL_LINK_TEXT, "Forgot")`|
|`By.CSS_SELECTOR`|Preferable for speed, clean & efficient|`find_element(By.CSS_SELECTOR, "input#email")`|
|`By.XPATH`|Complex DOM, need flexible targeting|`find_element(By.XPATH, "//input[@name='user']")`|