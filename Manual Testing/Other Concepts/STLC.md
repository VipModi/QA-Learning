## ✅ **What is STLC?**

**STLC (Software Testing Life Cycle)** is a **systematic process** followed by QA teams to ensure **quality and completeness of testing**.  
It defines **specific steps** to perform **effective and organized testing** of the software.

> 📌 While SDLC is about building software, **STLC is about testing it**.

---

## 🔄 **Phases of STLC (With QA Role & Examples)**

|Phase|Description|Key QA Activities|Example|
|---|---|---|---|
|1. **Requirement Analysis**|Understand what needs to be tested.|- Analyze functional & non-functional requirements  <br>- Identify testable items  <br>- Clarify doubts with stakeholders|You check if “unsend message” feature is testable on both mobile and web.|
|2. **Test Planning**|Decide the strategy, resources, and timelines.|- Create Test Plan  <br>- Identify required tools & resources  <br>- Estimate effort|You plan to test messaging feature on Android, iOS, Web, and VR.|
|3. **Test Case Design**|Write detailed test cases and test data.|- Write functional, UI, regression, edge-case test cases  <br>- Prepare test data|You write test cases for “Message delivery,” “Delete message,” “Edit message.”|
|4. **Test Environment Setup**|Prepare where testing will be done.|- Set up devices/emulators  <br>- Configure backend, APIs, builds  <br>- Verify environment readiness|Set up Facebook Messenger on iOS + Android + Desktop with debug logs.|
|5. **Test Execution**|Run tests and log bugs.|- Execute test cases  <br>- Log defects in JIRA  <br>- Track defects with dev team|You run tests on all platforms. Bug: Typing indicator not showing in group chats.|
|6. **Test Closure**|Final review and wrap-up.|- Prepare Test Summary Report  <br>- Assess test coverage  <br>- Retrospective meeting|You prepare a report on “Mute chat” feature testing and lessons learned.|

---

## 🔁 **STLC Flow (Simplified)**

+---------------------------+
|   Requirement Analysis     |
+---------------------------+
|          Test Planning           |
+---------------------------+
|       Test Case Design        |
+---------------------------+
|   Test Environment Setup |
+---------------------------+
|          Test Execution         |
+---------------------------+
|           Test Closure            |
+---------------------------+

---

## 🎯 Difference Between SDLC & STLC

|Aspect|SDLC|STLC|
|---|---|---|
|Focus|Software development process|Software testing process|
|Starts With|Requirement gathering|Test requirement analysis|
|Ends With|Software deployment & maintenance|Test closure and summary|
|Who|Developers, Designers, QA|QA/Test Engineers|

---

## 🧪 Real-World Example From Your Project

Let’s say you are testing a **privacy toggle feature**:

- 📄 **Requirement Analysis:** Understand that toggle must hide "last seen" across all platforms.
    
- 📋 **Test Planning:** Estimate 2 QA engineers, 3 days, tools = TestRail + JIRA.
    
- 🧾 **Test Case Design:** Write test cases for toggle ON, OFF, across mobile/web.
    
- 🔧 **Environment Setup:** Set up Android, iOS, and web logins with test users.
    
- ✅ **Execution:** Run tests, report bugs like "Toggle doesn’t sync across devices."
    
- 📊 **Closure:** Document that all test cases passed post-bug fix, prepare closure report.
    

---
### 📄 **Other Key Documents in the Testing Lifecycle**

|Document|Purpose|When It's Used|
|---|---|---|
|**Test Plan**|Strategy, scope, resources, schedule, risks, and deliverables for testing|At the start of the testing cycle|
|**Test Scenarios**|High-level ideas of what to test|During test design|
|**Test Cases**|Step-by-step instructions to validate functionality|During test execution|
|**RTM (Requirement Traceability Matrix)**|Maps requirements ↔ test cases|Throughout (design, execution, reporting)|
|**Test Data**|Input data used for testing scenarios|During test execution|
|**Test Summary Report**|Summary of overall testing activities, results, defect status|At the end of testing|
|**Bug/Defect Reports**|Details of defects found during testing|As bugs are found|