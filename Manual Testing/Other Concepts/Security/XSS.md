**XSS (Cross-Site Scripting)** is a type of **security vulnerability** typically found in web applications. It allows attackers to **inject malicious scripts** into web pages viewed by other users. These scripts are usually written in JavaScript and can be used to **steal cookies, session tokens, or other sensitive information**, perform actions on behalf of a user, or deface websites.

---

### 🔐 **Why is XSS Dangerous?**

- Steals user data like cookies and tokens
- Impersonates users by hijacking sessions
- Spreads malware
- Performs unauthorized actions (like sending messages or transferring funds)

---

## ✅ **3 Main Types of XSS:**

### 1. **Stored XSS (Persistent XSS)**

#### 📌 Description:
Malicious script is **permanently stored** on the server (e.g., in a database, comment field, message board).
#### ⚠️ Impact:
Every time a user accesses the affected page, the malicious script executes.

#### 🧪 Example:

```
<!-- User submits a comment with malicious script -->
<input type="text" name="comment" value="<script>alert('XSS Attack!')</script>">

<!-- On page load, it is rendered like this -->
<div>
  <p>User Comment: <script>alert('XSS Attack!')</script></p>
</div>
```
💥 When another user views the comment section, they’ll see a pop-up.

---

## 2. **Reflected XSS (Non-persistent XSS)**

#### 📌 Description:
Malicious script is **reflected off the server** in an error message, search result, or other response — immediately executed in the browser **without storing it on the server**.
#### ⚠️ Impact:
Usually delivered via phishing or malicious links.
#### 🧪 Example:
```
https://example.com/search?q=<script>alert('XSS')</script>
```

💥 If the server includes the `q` parameter in the page response like this:
```
<p>You searched for: <script>alert('XSS')</script></p>
```

It causes an alert popup.

---

## 3. **DOM-Based XSS**

#### 📌 Description:
Happens on the **client-side**, where the script is executed due to insecure JavaScript code manipulating the DOM without sanitizing user input.

#### ⚠️ Impact:

The server might not even be involved; it’s all in the browser.

#### 🧪 Example:
```
<!-- index.html -->
<p id="output"></p>
<script>
  // Bad practice: directly injecting URL fragment into DOM
  var hash = location.hash.substring(1); // e.g., #<script>alert(1)</script>
  document.getElementById("output").innerHTML = hash;
</script>
```

💥 Visiting:
```
https://example.com/index.html#<script>alert(1)</script>
```

will cause the browser to execute the script.

---

### 🛡️ **How to Prevent XSS:**

1. **Input Validation & Sanitization**
    - Never trust user input. Use libraries like DOMPurify.
        
2. **Output Encoding**
    - Convert `<`, `>`, `&`, `"` to safe equivalents when outputting data.
        
3. **Use HTTPOnly Cookies**
    - Prevent access to cookies via JavaScript.
    
4. **Content Security Policy (CSP)**
    - Restrict what scripts can run on your page.
        
5. **Avoid `innerHTML` or `document.write`**
    - Use `textContent` or safer methods instead.