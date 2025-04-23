#testing #manual
## 🔍 **Core Manual Testing Questions**

---

### 1. **What is the difference between verification and validation?**

- **Verification** ensures the product is being built **correctly** (as per requirements/specifications).
- **Validation** ensures the **right product** is being built (meeting user needs).

|Verification|Validation|
|---|---|
|Static process|Dynamic process|
|Done during development|Done after development|
|E.g., reviews, inspections|E.g., actual testing|

---

### 2. **What is the Software Testing Life Cycle (STLC)?**

The STLC defines the **phases involved in testing a software**. Typical phases:

1. **Requirement Analysis**
2. **Test Planning**
3. **Test Case Design**
4. **Test Environment Setup**
5. **Test Execution**
6. **Test Cycle Closure**
    

Each phase has entry and exit criteria, deliverables, and responsibilities.

---

### 3. **Explain the difference between severity and priority.**

- **Severity**: Impact of the bug on functionality.
- **Priority**: Urgency to fix the bug.

| Severity                        | Priority                                      |
| ------------------------------- | --------------------------------------------- |
| Decided by tester               | Decided by developer/manager                  |
| E.g., app crash = High severity | E.g., spelling error in title = High priority |

---

### 4. **What is exploratory testing? When is it used?**

Exploratory testing is an **informal and unscripted testing approach** where testers explore the app freely and use domain knowledge to find bugs.

✅ **Used when**:

- No formal test cases exist
- Time is limited
- Experienced testers want to uncover hidden issues

---

### 5. **What are test cases, test scripts, and test scenarios?**

- **Test Case**: A detailed set of steps, input, expected result.
- **Test Scenario**: A high-level idea of what to test.
- **Test Script**: Typically refers to automated test steps/code.

✅ Example:
- **Scenario**: Login functionality
- **Test Case**: Enter valid email/password → Click Login → Verify dashboard
- **Test Script**: Automated code to execute login steps

---

### 6. **What is the difference between retesting and regression testing?**

- **Retesting**: Testing **again** after a defect is fixed.
- **Regression Testing**: Testing existing features to ensure **new changes didn't break anything**.

|Retesting|Regression Testing|
|---|---|
|Focused on specific bug fix|Broad scope|
|Done on failed test cases|Done on passed test cases too|

---

### 7. **What is a bug life cycle?**

The **Bug Life Cycle** defines the stages a defect goes through:

1. New
2. Assigned
3. Open
4. Fixed
5. Retested
6. Verified
7. Closed    

💡 If the bug is rejected or not reproducible, it may go into **Rejected**, **Deferred**, or **Duplicate** states.

---

### 8. **What are different levels of testing?**

1. **Unit Testing** – Individual code units (done by developers)
2. **Integration Testing** – Interfaces between components
3. **System Testing** – Entire system as a whole
4. **Acceptance Testing** – Testing from user/business point of view

---

### 9. **What is black-box testing? Give an example.**

Black-box testing focuses on **functionality** without looking into the internal code.
✅ Example: Testing login functionality by entering email and password, without knowing how the backend is implemented.

---

### 10. **What is white-box testing? How is it different from black-box testing?**

White-box testing involves **looking into the code** and testing internal logic, loops, conditions, etc.

| Black-box                | White-box                                           |
| ------------------------ | --------------------------------------------------- |
| No code knowledge needed | Code knowledge required                             |
| Focus on functionality   | Focus on internal structure                         |
| Performed by testers     | Usually by developers/testers with coding knowledge |

## ✅ **Test Documentation & Techniques**

---

### 1️⃣ **What are the key components of a test plan?**

A **Test Plan** is a detailed document that outlines the testing strategy, scope, and activities. Key components include:

- **Test Plan ID**
- **Objective & Scope**
- **Testing Types** (functional, regression, etc.)
- **Test Deliverables**
- **Test Environment**
- **Roles & Responsibilities**
- **Entry & Exit Criteria**
- **Schedule & Milestones**
- **Risks & Mitigation**
- **Tools to be used**

---

### 2️⃣ **How do you write a good test case?**

A good test case should be **clear, concise, and repeatable**. It typically includes:
- **Test Case ID**
- **Title / Description**
- **Preconditions**
- **Test Steps**
- **Test Data**
- **Expected Result**
- **Actual Result**
- **Pass/Fail Status**
- **Comments or Attachments (if needed)**

🧠 Tip: Keep it simple, cover both positive and negative scenarios.

---

### 3️⃣ **What is boundary value analysis (BVA)?**

BVA is a **black-box test design technique** focusing on the **edge values** of input ranges.
🧪 If valid input is `1 to 100`, test cases would be:  
`0`, `1`, `2`, `99`, `100`, `101`

✅ Why? Most defects occur at boundaries due to incorrect conditions.

---

### 4️⃣ **What is equivalence partitioning?**

A **black-box testing** technique where input data is divided into **valid and invalid partitions**. You test **one value from each partition**, assuming others will behave similarly.

🧪 For a field that accepts values 1–100:
- Valid Partition: `1 to 100` → Test with `50`
- Invalid Partitions: `< 1` (e.g. `0`), `> 100` (e.g. `101`)    

---

### 5️⃣ **What is decision table testing?**

A technique used to test **different combinations of inputs and their corresponding outputs**.
📋 Looks like a **table of conditions vs actions**. Great for complex business rules.
🧪 Example: Login with combinations of:
- Correct/Incorrect username
- Correct/Incorrect password

---

### 6️⃣ **What is state transition testing?**

Used to test the **system's behavior based on state changes**.

🌀 Involves:
- States (e.g., Logged Out, Logged In)
- Transitions (e.g., Click "Login" → move to "Logged In")

✅ Useful for testing apps with workflows, screens, or stages.

---

### 7️⃣ **What is a traceability matrix?**

A **Requirement Traceability Matrix (RTM)** maps **requirements to test cases** to ensure full coverage.
📌 Helps to:
- Track test coverage
- Ensure no requirement is missed
- Trace failed test cases back to requirements
    

---

### 8️⃣ **What is a use case and how do you test it?**

A **use case** describes how a user interacts with the system to achieve a goal.
🧪 Use Case Testing involves:
- Understanding actor actions and system responses
- Writing test cases for each possible scenario, including alternate flows

📋 Example: Use case for “Place an Order” → includes login, add to cart, checkout.

---

### 9️⃣ **What is acceptance testing?**

**Final level of testing** before release, done to validate the system **meets business needs**.

✅ Types:
- **User Acceptance Testing (UAT)** – done by end users
- **Business Acceptance Testing (BAT)** – done by business team

---

### 🔟 **Explain the V-model in software testing.**

The **V-Model (Validation & Verification model)** is an extension of the waterfall model where each development phase has a corresponding testing phase.
```
Requirements     →     Acceptance Testing  
Design           →     System Testing  
Architecture     →     Integration Testing  
Coding           →     Unit Testing
```

📌 Emphasizes **early test planning**, and testing is done in parallel with development stages.

## **Bug Reporting & Tools**

---

### 1️⃣ **How do you report a bug effectively?**

To report a bug effectively:
- Be **clear and concise**
- Provide **step-by-step reproduction steps**
- Include **expected vs. actual result**
- Attach **screenshots/logs/videos** if possible
- Assign the right **severity/priority**
- Mention **environment details** (device, OS, build)

💡 Goal: Make it easy for developers to **understand and fix** the issue without back-and-forth.

---

### 2️⃣ **What are the fields in a bug report?**

Common fields in a bug report:

|Field|Description|
|---|---|
|Bug ID|Unique identifier|
|Title/Summary|Short description of the issue|
|Description|Detailed explanation|
|Steps to Reproduce|Exact steps to trigger the issue|
|Expected Result|What should happen|
|Actual Result|What actually happens|
|Severity|Impact level (Critical, Major, Minor)|
|Priority|Fix urgency (High, Medium, Low)|
|Status|New, Open, Fixed, Closed, etc.|
|Environment|OS, browser, app version, etc.|
|Reporter|Name of tester|
|Attachments|Screenshots, logs, videos, etc.|

---

### 3️⃣ **What defect tracking tools have you used?**

Some commonly used tools:

- **JIRA** 
- Bugzilla
- Mantis
- HP ALM / Quality Center
- Azure DevOps
- Asana / Trello (lightweight tracking)

You can say:

> "I have used **JIRA** extensively for logging and tracking bugs with custom fields, filters, dashboards, and workflow status updates."

---

### 4️⃣ **How do you differentiate between a defect, bug, and error?**

|Term|Description|
|---|---|
|**Error**|A mistake made by a developer (e.g., wrong syntax or logic)|
|**Bug/Defect**|A flaw or issue found during testing that causes incorrect behavior|
|**Failure**|When the system behaves incorrectly during execution due to a bug|

💡 **Error → Bug → Failure**

---

### 5️⃣ **What is the difference between alpha testing and beta testing?**

|Feature|**Alpha Testing**|**Beta Testing**|
|---|---|---|
|Performed by|Internal testers|Real users|
|Environment|In-house|Real-world|
|Stage|Before release|After alpha, before final release|
|Purpose|Identify bugs early|Get user feedback|


### **6️⃣ What is Bug Leakage?**

**Definition:**  
Bug Leakage occurs when a **bug is missed during the testing phase** and is later **found by the end user or customer after the product is released**.

**Example:**  
Let’s say you tested a messaging feature thoroughly but missed a scenario where messages with emojis crash the app. After release, a user reports this issue. This is **bug leakage**.

**Why it happens:**
- Incomplete test coverage
- Unclear requirements
- Environment differences (dev vs prod)
- Lack of regression testing

**Impact:**  
Damages client trust, increases rework, and may affect reputation.

---

### **7️⃣ What is Bug Release?**

**Definition:**  
Bug Release refers to **intentionally releasing a software version with known bugs**, often **minor or low-priority ones**, with a clear note that these bugs will be fixed in future releases.

**Example:**  
A new version of the app is released with a known bug that causes a UI alignment issue in dark mode. Since it doesn't affect functionality and deadlines are tight, it’s noted and postponed.

**Reasons for Bug Release:**
- Deadlines and business pressure
- Bug has low severity or impact
- Fix is already planned for the next sprint/release

**Best Practice:**  
Document the known bugs clearly in the release notes.
---

## 🛠 **Testing Process and Best Practices**

---

### 6️⃣ **How do you decide when to stop testing?**

You can stop testing when:
- All **major test cases** have passed    
- **Bug rate** drops significantly
- **Deadlines/release dates** are reached
- **Code coverage** goals are met
- **Risk is acceptable**
- **Stakeholder approval** is received

💡 Use **Exit Criteria** defined in the Test Plan.

---

### 7️⃣ **What is risk-based testing?**

Testing based on **risk assessment** – prioritizing features/modules that are:
- **Business critical**    
- **Highly used**
- **Likely to break**
- **Technically complex**

🎯 Focus is on **maximizing value** with limited time/resources.

---

### 8️⃣ **How do you prioritize test cases?**

Prioritize based on:

- **Business impact**
- **Critical functionality**
- **Failure probability**
- **Usage frequency**
- **Regulatory/compliance importance**

✅ Examples:
- Login, payment, and data protection test cases get **High Priority**
    

---

### 9️⃣ **What are test deliverables?**

Artifacts/documents produced during the testing process:
- **Test Plan**
- **Test Cases / Scenarios**
- **RTM (Traceability Matrix)**
- **Test Data**
- **Bug Reports**
- **Test Summary Report**
- **Test Closure Report**

---

### 🔟 **What is sanity vs. smoke testing?**

|Feature|**Smoke Testing**|**Sanity Testing**|
|---|---|---|
|Purpose|To verify if the build is stable|To verify a specific fix or functionality|
|Performed on|Initial builds|After minor changes or bug fixes|
|Coverage|Broad, shallow|Narrow, deep|
|Example|Can I access homepage, login, dashboard?|Is the login bug really fixed?|

## 🔁 **Agile & Real-Time Scenarios**

---

### 1️⃣ **How does testing work in Agile?**

- Testing is done **continuously and collaboratively**.    
- QA works closely with developers and product owners during each sprint.
- Testing types: **Exploratory, Acceptance, Regression, Integration**.
- Testers participate in **daily stand-ups**, **sprint planning**, **reviews**, and **retrospectives**.

> 💡 “Test early, test often” is the Agile way.

---

### 2️⃣ **What is a sprint and what is your role in it?**

- A **Sprint** is a time-boxed iteration (usually 1–4 weeks).
- As a tester, I:
    - Attend sprint planning to understand user stories
    - Write and execute test cases for each story
    - Perform regression testing
    - Raise and track bugs
    - Contribute in sprint demo and retrospective

---

### 3️⃣ **What is the difference between a story, epic, and task in JIRA?**

| Term      | Description                                                                 |
| --------- | --------------------------------------------------------------------------- |
| **Epic**  | Large feature or business goal (e.g., “User Profile Management”)            |
| **Story** | Specific functionality under an epic (e.g., “Update Profile Info”)          |
| **Task**  | Small unit of work, technical or testing-related (e.g., “Write test cases”) |

---

### 4️⃣ **How do you perform testing when requirements are incomplete?**

- Ask clarifying questions to PO or BA    
- Refer to similar existing features
- Perform **exploratory testing**
- Validate based on user experience and business logic
- Document assumptions made

---

### 5️⃣ **Have you worked in CI/CD environments?**

> Yes. While I haven’t set up pipelines myself, I’ve worked in teams where builds were automated using **CI/CD tools like Jenkins and Git**.

- I test builds as soon as they’re deployed
- Perform smoke/sanity/regression based on changes
- Raise blockers if deployment fails

---

## 🔎 **Interview-Style Scenario Questions**

---

### 6️⃣ **What would you do if a developer disagrees with your bug?**

- Reproduce the issue with clear steps, data, and evidence
- Show logs/screenshots
- Refer to requirements if available
- Escalate to BA/lead if needed
- Stay collaborative, not confrontational

---

### 7️⃣ **How do you test an application with no documentation?**

- Explore the application and identify major modules
- Use **exploratory testing** techniques
- Talk to developers/PO for understanding
- Reverse-engineer UI behavior into test cases

---

### 8️⃣ **What if a critical bug is found just before release?**

- Immediately communicate to QA Lead/PO/Dev team
- Assess impact, risk, and possible workaround
- If fixable: prioritize and test it quickly
- If not: escalate and advise release block

---

### 9️⃣ **How do you ensure test coverage?**

- Use **RTM** to map requirements to test cases
- Use checklists to cover UI, functionality, boundary, negative cases
- Perform **peer reviews**
- Do regular gap analysis

---

### 🔟 **How do you handle frequently changing requirements?**

- Keep test cases modular and reusable
- Focus on exploratory and session-based testing
- Stay aligned with product team through daily syncs
- Update test cases and data incrementally

---

## 💬 **Behavioral & Miscellaneous**

---

### 1️⃣1️⃣ **Describe a challenging bug you found and how you handled it.**

> On one release, I found an **intermittent crash issue** only on Android 11 during long usage sessions. I reproduced it using screen recording, logs, and narrowed it to a memory leak. The devs were able to fix it before release, and I got a spot award for that.

---

### 1️⃣2️⃣ **What motivates you to be in QA?**

- I enjoy **finding gaps**, thinking from the **user’s perspective**, and contributing to **building quality products**.
- The constant learning and variety in QA keeps me motivated.

---

### 1️⃣3️⃣ **How do you stay updated with testing trends?**

- Follow blogs: Ministry of Testing, Test Automation University
- LinkedIn QA communities
- Take online courses (e.g., Udemy, Coursera)
- Attend QA webinars or bugathons

---

### 1️⃣4️⃣ **How do you deal with repetitive testing tasks?**

- Use checklists or spreadsheets for faster tracking
- Group related test cases to streamline flow
- Suggest automation if applicable
- Keep exploratory sessions to stay engaged

---

### 1️⃣5️⃣ **How do you ensure quality in a fast-paced development environment?**

- Prioritize **critical flows**
- Do **risk-based** and **impact-based testing**
- Focus on **early involvement** in sprint discussions
- Ensure quick feedback loops and clear communication

---

## 🌐 **Web & Mobile Testing Focus**

---

### 1️⃣6️⃣ **What are some challenges in mobile app testing?**

- Device fragmentation (screen sizes, OS versions)
- Network conditions (slow, offline)
- App permissions
- Battery/memory usage
- OS-specific bugs (iOS vs Android)

---

### 1️⃣7️⃣ **How do you test a responsive website?**

- Resize browser or use developer tools
- Test on real devices/emulators
- Use tools like **BrowserStack, Responsinator*
- Check layout, alignment, font sizes, navigation

---

### 1️⃣8️⃣ **What is cross-browser testing?**

Testing how a web app behaves across **different browsers** (Chrome, Firefox, Safari, Edge) and versions.

🔍 Focus areas:
- UI rendering
- CSS compatibility
- JS behavior
- Form/input issues

---

### 1️⃣9️⃣ **What are key considerations in API testing (even manually)?**

- Validate **request/response** structure (JSON/XML)
- Status codes (200, 400, 500)
- Authentication (tokens, headers)
- Positive & negative scenarios
- Tools: **Postman**, **cURL**

---

### 2️⃣0️⃣ **What is localization and internationalization testing?**

|Type|Description|
|---|---|
|**Localization**|Testing app in **specific languages**, regions, date/currency formats|
|**Internationalization**|Testing app's ability to support **multiple languages/cultures** without code changes|

✅ Focus on:
- Text alignment
- Special characters
- Translations
- Language switch behavior