## ✅ **1. Positive Test Cases**

These validate that the login works under correct conditions.

|Test Case ID|Description|
|---|---|
|TC_POS_01|Verify login with valid username and password.|
|TC_POS_02|Verify "Remember Me" functionality works as expected.|
|TC_POS_03|Verify successful login redirects user to the correct landing page/dashboard.|
|TC_POS_04|Verify user can log in using the "Enter" key after filling credentials.|
|TC_POS_05|Verify user is able to log out and redirected to the login page.|
|TC_POS_06|Verify login using username/email/mobile (if multiple options are supported).|
|TC_POS_07|Verify user session is maintained after login (until logout or timeout).|

---

## ❌ **2. Negative Test Cases**

These ensure that invalid inputs are properly handled.

|Test Case ID|Description|
|---|---|
|TC_NEG_01|Verify login fails with incorrect username.|
|TC_NEG_02|Verify login fails with incorrect password.|
|TC_NEG_03|Verify login fails with both username and password incorrect.|
|TC_NEG_04|Verify error when mandatory fields are left blank.|
|TC_NEG_05|Verify system behavior when SQL injection is attempted in input fields.|
|TC_NEG_06|Verify error messages are shown for invalid credentials.|
|TC_NEG_07|Verify account lock after multiple failed login attempts (e.g., 5 tries).|
|TC_NEG_08|Verify login fails with expired credentials.|
|TC_NEG_09|Verify login fails with deactivated or blocked account.|
|TC_NEG_10|Verify login fails with unsupported characters or emojis.|

---

## 🎨 **3. UI/UX Test Cases**

These test the design and behavior of the login interface.

|Test Case ID|Description|
|---|---|
|TC_UI_01|Verify the alignment and labels of input fields and buttons.|
|TC_UI_02|Verify placeholder texts are visible and meaningful.|
|TC_UI_03|Verify password field is masked (dots or asterisks).|
|TC_UI_04|Verify presence of "Forgot Password", "Sign Up", or "Create Account" links.|
|TC_UI_05|Verify login button is disabled until mandatory fields are filled (if applicable).|
|TC_UI_06|Verify responsiveness of login page on different screen sizes.|

---

## 🔒 **4. Security Test Cases**

Ensure that login is secure from basic threats.

|Test Case ID|Description|
|---|---|
|TC_SEC_01|Verify password is not stored or visible in browser autofill.|
|TC_SEC_02|Verify password is encrypted during transmission (check HTTPS).|
|TC_SEC_03|Verify session timeout after inactivity.|
|TC_SEC_04|Verify account is locked after repeated failed attempts (brute force prevention).|
|TC_SEC_05|Verify user is automatically logged out after closing the browser.|
|TC_SEC_06|Verify "Forgot Password" leads to a secure recovery process.|
|TC_SEC_07|Verify system is protected from XSS and SQL injection attacks.|

---

## ⚙️ **5. Functional Edge Cases**

These ensure edge behaviors are handled properly.

|Test Case ID|Description|
|---|---|
|TC_FUN_01|Verify behavior when entering credentials with leading/trailing spaces.|
|TC_FUN_02|Verify behavior with case sensitivity in username/email.|
|TC_FUN_03|Verify user is redirected back to intended page after login (if login was triggered mid-session).|
|TC_FUN_04|Verify login functionality when cookies are disabled.|

---

## 📱 **6. Compatibility Test Cases**

Test across browsers/devices/platforms.

|Test Case ID|Description|
|---|---|
|TC_COMP_01|Verify login works on Chrome, Firefox, Edge, Safari.|
|TC_COMP_02|Verify login on Android and iOS devices.|
|TC_COMP_03|Verify login works properly in incognito/private mode.|
|TC_COMP_04|Verify layout and fields on different resolutions and devices.|

---

## 🚀 **7. Performance Test Cases**

Check login under load or response behavior.

| Test Case ID | Description                                                                  |
| ------------ | ---------------------------------------------------------------------------- |
| TC_PERF_01   | Verify login response time under normal conditions (should be <3s).          |
| TC_PERF_02   | Verify login functionality when multiple users try to log in simultaneously. |
| TC_PERF_03   | Verify the system’s response to login attempts during peak hours.            |

## 🔍 **More Edge Cases for Login Functionality**

| Test Case ID     | Description                                                                                                    |
| ---------------- | -------------------------------------------------------------------------------------------------------------- |
| TC_LOGIN_EDGE_06 | Enter extremely long strings in username and password fields (e.g., 500+ characters).                          |
| TC_LOGIN_EDGE_07 | Enter HTML/JavaScript tags in input fields (e.g., `<script>alert(1)</script>`) to check for XSS vulnerability. |
| TC_LOGIN_EDGE_08 | Attempt login with valid credentials but incorrect case in password (to verify case sensitivity).              |
| TC_LOGIN_EDGE_09 | Attempt login while the account is locked but try with correct credentials.                                    |
| TC_LOGIN_EDGE_10 | Attempt login when the system clock is changed (e.g., future/past time) on the client side.                    |
| TC_LOGIN_EDGE_11 | Try logging in with network interruptions mid-request.                                                         |
| TC_LOGIN_EDGE_12 | Attempt login on two different devices at the same time (check session consistency).                           |
| TC_LOGIN_EDGE_13 | Attempt login using autofill data from browser when fields are programmatically renamed.                       |
| TC_LOGIN_EDGE_14 | Enter special language characters (e.g., Chinese, Arabic, emojis) in username/password.                        |
| TC_LOGIN_EDGE_15 | Attempt login with a copied-and-pasted password with extra white spaces (e.g., `"password "`).                 |