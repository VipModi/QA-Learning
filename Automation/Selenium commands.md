## ✅ 1. **Browser Setup & Navigation**

|Function|Purpose|Example|
|---|---|---|
|`webdriver.Chrome()`|Launch Chrome browser|`driver = webdriver.Chrome()`|
|`get(url)`|Open a URL|`driver.get("https://example.com")`|
|`maximize_window()`|Maximize browser window|`driver.maximize_window()`|
|`refresh()`|Refresh current page|`driver.refresh()`|
|`back()`|Navigate to previous page|`driver.back()`|
|`forward()`|Go forward to next page|`driver.forward()`|
|`quit()`|Close entire browser session|`driver.quit()`|
|`close()`|Close current browser tab|`driver.close()`|

---

## ✅ 2. **Element Interaction**

|Function|Purpose|Example|
|---|---|---|
|`find_element(By, value)`|Locate a single element|`driver.find_element(By.ID, "username")`|
|`find_elements(By, value)`|Locate multiple elements|`driver.find_elements(By.TAG_NAME, "a")`|
|`send_keys()`|Type into input field|`element.send_keys("Vipul")`|
|`click()`|Click on element|`element.click()`|
|`clear()`|Clear text input|`element.clear()`|
|`submit()`|Submit a form|`element.submit()`|

---

## ✅ 3. **Element State Check**

|Function|Purpose|Example|
|---|---|---|
|`is_displayed()`|Is element visible?|`element.is_displayed()`|
|`is_enabled()`|Is element enabled?|`element.is_enabled()`|
|`is_selected()`|Is checkbox/radio selected?|`element.is_selected()`|

---

## ✅ 4. **Waits (Explicit Wait)**

> Used to wait for elements to load or become clickable.

```
from selenium.webdriver.support.ui import WebDriverWait
from selenium.webdriver.support import expected_conditions as EC

wait = WebDriverWait(driver, 10)
element = wait.until(EC.presence_of_element_located((By.ID, "email")))
```

|Common Expected Conditions|Use|
|---|---|
|`presence_of_element_located()`|Element exists in DOM|
|`visibility_of_element_located()`|Element is visible|
|`element_to_be_clickable()`|Element is clickable|
|`title_is()`|Page title is as expected|

---

## ✅ 5. **Dropdowns**

```
from selenium.webdriver.support.ui import Select
dropdown = Select(driver.find_element(By.ID, "country"))
dropdown.select_by_visible_text("India")
```

|Method|Use|
|---|---|
|`select_by_index()`|Select by index (0-based)|
|`select_by_value()`|Select by `value` attribute|
|`select_by_visible_text()`|Select by text shown in UI|

---

## ✅ 6. **Alerts / Popups**

```
alert = driver.switch_to.alert
print(alert.text)
alert.accept()  # or alert.dismiss()
```

---

## ✅ 7. **Frame Switching**

```
driver.switch_to.frame("frame_id_or_name")
driver.switch_to.default_content()  # To exit frame
```

---

## ✅ 8. **Window Handling**

```
windows = driver.window_handles
driver.switch_to.window(windows[1])  # Switch to new tab
```
---

## ✅ 9. **Taking Screenshot**

```
driver.save_screenshot("screenshot.png")
```

---

## ✅ 10. **Assertions in Python**

Useful for validations in test cases.

```
assert "Dashboard" in driver.title assert element.is_displayed()
```

---

## 🧪 Bonus: Full Example

```
from selenium import webdriver
from selenium.webdriver.common.by import By

driver = webdriver.Chrome()
driver.get("https://example.com")
driver.find_element(By.ID, "username").send_keys("Vipul")
driver.find_element(By.ID, "password").send_keys("123456")
driver.find_element(By.ID, "login").click()
assert "Dashboard" in driver.title
driver.quit()
```

## 🧾 **Scenario:**

You're automating a sample login form:

1. Open browser and navigate to the login page
2. Enter username and password
3. Click the login button
4. Validate login by checking the page title
5. Navigate to a dropdown and select an option
6. Handle an alert
7. Take a screenshot
8. Logout and close browser

---

## ✅ **Sample Code (Python + Selenium)**

```
from selenium import webdriver
from selenium.webdriver.common.by import By
from selenium.webdriver.support.ui import WebDriverWait, Select
from selenium.webdriver.support import expected_conditions as EC
import time

# 1. Launch the browser
driver = webdriver.Chrome()
driver.maximize_window()

# 2. Open a sample website (You can replace with any practice site)
driver.get("https://practicetestautomation.com/practice-test-login/")  # Sample site

# 3. Enter username and password
driver.find_element(By.ID, "username").send_keys("student")
driver.find_element(By.ID, "password").send_keys("Password123")

# 4. Click the login button
driver.find_element(By.ID, "submit").click()

# 5. Wait and verify successful login
WebDriverWait(driver, 10).until(EC.title_contains("Logged In"))
assert "Logged In Successfully" in driver.page_source

# 6. Handle a dropdown (simulate if not on this page)
# Example code:
# dropdown = Select(driver.find_element(By.ID, "country"))
# dropdown.select_by_visible_text("India")

# 7. Handle alert (simulate alert handling)
# Example:
# alert = driver.switch_to.alert
# alert.accept()

# 8. Take a screenshot
driver.save_screenshot("login_success.png")

# 9. Simulate logout (optional based on site)
driver.find_element(By.LINK_TEXT, "Log out").click()

# 10. Close browser
time.sleep(2)
driver.quit()
```

---

## ✅ Concepts Covered:

- Browser launch and navigation
- Element identification using `By.ID` and `By.LINK_TEXT`
- Input actions with `send_keys()`
- Click and assertion
- Explicit waits (`WebDriverWait`)
- Dropdown selection (commented for sites that have it)
- Alert handling (commented for sites that pop alerts)
- Screenshot
- Logout and close browser