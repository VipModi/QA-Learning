## 🧪 What is **PyTest**?

**PyTest** is a **Python testing framework** that makes it easy to write **simple unit tests** as well as **complex functional tests**.  
It's known for:

- Simple syntax
- Powerful features (like fixtures, parametrization, markers)
- Great support for Selenium & API automation
    

---

## ✅ Why PyTest?

| Feature                      | Benefit                                            |
| ---------------------------- | -------------------------------------------------- |
| No need for boilerplate code | No need to extend classes or write main()          |
| Fixtures                     | Reusable setup and teardown logic                  |
| Parametrization              | Run the same test with multiple data inputs        |
| Plugins Support              | Allure reporting, HTML reports, parallel execution |
| Markers                      | Tag and selectively run tests                      |
| Easy integration             | Works with Selenium, requests, etc.                |

---

## 🧾 1. **Basic Test Case in PyTest**

```
# test_sample.py

def test_addition():
    assert 2 + 2 == 4
```

> ✅ Run it using:

```
pytest test_sample.py
```

---

## 🧪 2. **Setup & Teardown using Fixtures**
**Definition (Setup and Teardown :**  
This is used to define what should happen **before** and **after** each test (e.g., open and close the browser).  
This is done using `@pytest.fixture`.

**Definition (Fixtures):**  
Fixtures are reusable **setup blocks** that can be shared across tests. They help remove repetitive code.

```
import pytest

@pytest.fixture
def setup_browser():
    print("🚀 Launch browser")
    yield
    print("❌ Close browser")

def test_login(setup_browser):
    print("🔐 Running login test")
    assert True
```

> 🔹 The `yield` keyword splits setup and teardown parts.  
> 🔹 This is just like `@BeforeMethod` and `@AfterMethod` in TestNG.

---

## 🔁 3. **Parameterized Tests**
**Definition:**  
Run the **same test multiple times** with **different inputs** (like data-driven testing).

```
import pytest

@pytest.mark.parametrize("username, password", [
    ("user1", "pass1"),
    ("user2", "pass2"),
])
def test_login(username, password):
    print(f"Trying with {username}, {password}")
    assert username != "" and password != ""
```

> 🔄 Run the same test with multiple inputs!

---

## 🏷️ 4. **Markers (Grouping & Tagging)**
**Definition:**  
Markers are **labels** you add to tests to **group or categorize** them — such as `smoke`, `regression`, `sanity`, etc.

```
import pytest

@pytest.mark.smoke
def test_smoke_case():
    assert True

@pytest.mark.regression
def test_regression_case():
    assert True
```

> Run only smoke tests:

```
pytest -m smoke
```

---

## 📜 5. **Assertions**
**Definition:**  
Assertions are checks that verify if a condition is **true or false**. If the assertion fails, the test fails.

```
def test_string():
    assert "Hello" in "Hello World"

def test_numbers():
    assert 10 > 5
```

> All test functions **must start with `test_`**

**Use Cases:**
- Check if the correct page title is shown
- Verify that expected text exists
- Validate status codes in API tests
- Compare actual vs. expected results

---

## 🧾 6. **PyTest + Selenium Example**

```
from selenium import webdriver
import pytest

@pytest.fixture
def setup():
    driver = webdriver.Chrome()
    driver.get("https://example.com")
    yield driver
    driver.quit()

def test_title(setup):
    assert "Example Domain" in setup.title
```

---

## 📦 7. **How to Run Tests**

- Run all tests:
```
pytest
```

- Verbose output:
```
pytest -v
```

- Specific test file:
```
pytest test_login.py
```

- Marker filter:
```
pytest -m smoke
```

---

## 📂 8. **Recommended Folder Structure**

```
project/
│
├── tests/
│   ├── test_login.py
│   └── test_signup.py
│
├── conftest.py   ← (global fixtures)
├── requirements.txt
└── pytest.ini    ← (marker config, options)
```

---

## 🎁 Bonus: Useful Plugins

| Plugin          | Purpose                      |
| --------------- | ---------------------------- |
| `pytest-html`   | Generate HTML test reports   |
| `pytest-xdist`  | Run tests in parallel        |
| `allure-pytest` | Beautiful advanced reporting |

### **Test Discovery**

**Definition:**  
PyTest automatically finds files and functions to run based on naming.

**Rules:**
- Test files must start with `test_` (e.g., `test_login.py`)
- Test functions must start with `test_`

**Run All Tests:**
```
pytest
```

### **Skip & XFail (Expected Fail)**

#### Skip a test:
```
@pytest.mark.skip
def test_not_ready():
    assert False
````

#### Expected to fail:

```
@pytest.mark.xfail
def test_buggy_feature():
    assert 1 == 2
```

---

### **Test Report Plugins**

You can generate detailed test reports using:
- `pytest-html` → simple HTML report
- `allure-pytest` → beautiful, customizable reports
- `pytest-xdist` → for parallel execution    

Install example:
```
pip install pytest-html
pytest --html=report.html
```

---

### **Command Line Options (Common)**

|Command|Purpose|
|---|---|
|`pytest -v`|Verbose output|
|`pytest -k "login"`|Run tests that match name "login"|
|`pytest -m smoke`|Run only smoke-marked tests|
|`pytest --maxfail=1`|Stop after 1 failure|
|`pytest --html=report.html`|Generate HTML report|

---

### **PyTest.ini (Optional Config File)**

You can configure PyTest behavior here.

```
# pytest.ini
[pytest]
markers =
    smoke: smoke test
    regression: regression test
addopts = -v --maxfail=3
```