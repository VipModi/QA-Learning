### ✅ What is **Unit Testing**?

**Unit testing** is a type of software testing where **individual units or components** of a software application are tested **in isolation** to ensure they work as expected.

**Definition:**  
Unit testing is a **software testing technique** where **individual units/components of source code** are tested in isolation from the rest of the application. The purpose is to verify that each **function or method** performs as expected.

A **"unit"** is the smallest piece of testable software, typically a single function, method, or class

---

### 🔍 Key Points:

|Aspect|Description|
|---|---|
|**Unit**|The smallest testable part of an application (e.g., a function, method, or class)|
|**Goal**|To verify that each unit of code performs as designed|
|**Performed by**|Typically done by **developers** during the development phase|
|**Automation**|Usually automated using testing frameworks (e.g., JUnit, PyTest, NUnit)|
|**Scope**|Very narrow — focuses on a single piece of logic, not the system as a whole|

---

### 🧪 Example:

Let’s say you have a function:
```
def add(a, b):
    return a + b
```

A **unit test** for this function might look like:
```
def test_add():
    assert add(2, 3) == 5
```

This test checks if the `add` function works correctly when given specific inputs.

---

### 🔧 Common Unit Testing Tools:

|Language|Tools/Frameworks|
|---|---|
|Python|PyTest, unittest|
|Java|JUnit, TestNG|
|JavaScript|Jest, Mocha, Jasmine|
|C#|NUnit, MSTest|
|C++|Google Test (gtest)|

---

### ✅ Benefits:

- Catches bugs early
- Simplifies debugging (you know exactly which function failed)
- Helps with code refactoring
- Improves code quality and reliability
    

---

### 🚫 Limitations:

- Doesn’t catch integration or system-level issues
- Writing and maintaining lots of unit tests takes time
- Can give a false sense of security if not combined with other testing types

## 👀 How Unit Testing Affects Manual Testers

As a manual tester like you, even if you're **not writing unit tests**, understanding them helps in several ways:

| Benefit for Testers                | Description                                                                                                               |
| ---------------------------------- | ------------------------------------------------------------------------------------------------------------------------- |
| **Better Test Design**             | Knowing what's already covered in unit tests helps you focus on integration, UI, and edge cases.                          |
| **Improved Collaboration**         | You can speak the same language as developers and discuss coverage or failures meaningfully.                              |
| **Efficient Debugging**            | When a bug appears, you can check if a unit test exists for that function — it helps narrow down the root cause.          |
| **Validation of Developer Claims** | Sometimes devs claim, "It's already tested" — you can ask **which unit test covers it**.                                  |
| **Code Confidence**                | Knowing a feature has strong unit test coverage may reduce the need for exhaustive manual retesting during small updates. |

## ✅ Sub-types of Unit Testing (Based on Focus)

|Sub-Type|Description|Example|
|---|---|---|
|**Functional Unit Test**|Tests the function’s output based on inputs (black box approach). Focuses on what it does.|Test if `add(2, 3)` returns `5`|
|**Structural Unit Test**|Tests internal logic, paths, and branches inside the function (white box approach).|Check if both `if` and `else` blocks are tested|
|**Boundary Unit Test**|Focuses on boundary values (e.g., edge cases, limits).|Check behavior when input is `0` or `max int`|
|**Exception Unit Test**|Tests whether exceptions are properly raised and handled.|Check if `divide(4, 0)` raises `ZeroDivisionError`|
|**Parameterized Test**|The same unit test is run with multiple sets of inputs.|`add(a, b)` tested with many pairs of values|

---

## ⚙️ Sub-types (Based on Strategy/Approach)

|Strategy|Description|
|---|---|
|**Manual Unit Testing**|Rarely done, but can be manually invoked in simple scripts during early development.|
|**Automated Unit Testing**|Most common — uses frameworks like `unittest`, `pytest`, `JUnit` to automate execution.|
|**Mock-based Testing**|Uses mocks/fakes to simulate external dependencies like databases or APIs.|
|**Isolated Unit Testing**|Tests the unit independently by mocking all dependencies.|
|**Integrated Unit Testing**|Allows some real dependencies to work together, closer to integration testing.|

---

## 👀 From a Tester’s View: Why This Matters

Even if you're not writing unit tests yet, understanding sub-types helps you:

- **Ask better questions**: ("Do we cover boundary and exception cases in unit tests?")
- **Design better manual tests**: Based on what developers are already covering.
- **Plan regression scope**: Knowing unit test coverage reduces redundant manual testing.
- **Step into automation later**: Helps when you start writing test cases in Python.


## 📂 Types of Code Coverage Metrics

| **Coverage Type**                       | **What It Measures**                                                     | **Best Used For**                                      |
| --------------------------------------- | ------------------------------------------------------------------------ | ------------------------------------------------------ |
| **Line Coverage**                       | % of source code lines executed                                          | General testing completeness                           |
| **Statement Coverage**                  | % of individual executable statements run                                | Similar to line coverage, but logic-aware              |
| **Branch Coverage**                     | % of all branches from decision points (e.g., `if`, `else`, `switch`)    | Ensuring all code paths are hit                        |
| **Decision Coverage**                   | % of decisions (conditions as a whole) evaluated to both TRUE and FALSE  | Logical decision points and control structures         |
| **Condition Coverage**                  | % of individual boolean expressions evaluated both ways (TRUE and FALSE) | Detailed control flow, multiple boolean conditions     |
| **Function/Method Coverage**            | % of functions or methods called at least once                           | API and class-level testing                            |
| **Path Coverage**                       | % of all possible execution paths through the code                       | Very detailed testing (can grow exponentially)         |
| **Loop Coverage**                       | Checks if loops (`for`, `while`) execute 0, 1, and many times            | Iterative logic, input-dependent flows                 |
| **Finite State Machine (FSM) Coverage** | Tests system behavior based on defined states and transitions            | UI states, user flows, message delivery, auth sessions |
| → **State Coverage**                    | Whether all defined states were entered during tests                     | Ensures full state reachability                        |
| → **Transition Coverage**               | Whether all allowed state transitions were triggered                     | End-to-end flow testing                                |
| → **Transition Pair Coverage**          | Whether all sequences of state transitions were tested                   | Complex workflows and chaining logic                   |