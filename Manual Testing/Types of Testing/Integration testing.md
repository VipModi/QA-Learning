## 🔗 What is Integration Testing?

**Definition:**  
**Integration Testing** is a level of software testing where **individual units or components** are combined and tested **as a group** to ensure they work **together correctly**.

It checks the **interfaces**, **data flow**, and **interactions** between modules — not just that individual functions work, but that they communicate and behave properly when integrated.

---

## 🎯 Goal of Integration Testing

- ✅ To verify **data flow between modules**
- ✅ To identify **interface issues** (e.g., mismatched input/output, broken API calls)
- ✅ To catch **logic errors** when components interact
- ✅ To validate **end-to-end scenarios across modules**
    

---

## 🔄 Types of Integration Testing

|Type|Description|
|---|---|
|**Top-down**|Testing starts from the top modules and moves downward using **stubs** for lower modules.|
|**Bottom-up**|Testing starts from lower modules using **drivers** for higher modules.|
|**Big Bang**|All modules are combined and tested together (high risk, often used late).|
|**Incremental**|Modules are integrated and tested one by one to isolate defects early.|

---

## 🧠 Why Integration Testing is Important

|Reason|Description|
|---|---|
|**Catch communication issues**|Modules may work fine independently, but fail when combined.|
|**Prevent system bugs early**|Errors caught here are cheaper than catching them during system testing.|
|**Validates contracts**|Ensures APIs, database calls, and services are working as expected.|
|**Improves confidence**|Helps teams ensure that combining tested units won’t cause failures.|

---

## 👀 How Integration Testing Affects You (Manual Tester)

Even if you're not writing integration test scripts, this level of testing **directly overlaps with your role**, Vipul. Here's how:

|Impact on Testers|Description|
|---|---|
|✅ **Core testing area**|Manual testers often perform integration testing by combining features across screens or services.|
|🛠 **Focus for Bug Bashes**|Many bugs arise from integration failures, not unit bugs — great focus during exploratory or Bug Bash sessions.|
|🔎 **Helps with Reproduction**|Knowing which components interact helps recreate complex bugs.|
|📋 **Test Planning**|Helps identify cross-feature dependencies (e.g., message status + notification + privacy setting).|
|🤝 **Collaboration**|You can report better bugs by pointing out which **two components** are failing to integrate properly.|

---

## 📱 Real-World Example from Your Domain (Messaging App)

Let’s say you’re testing a **"Delete for Everyone"** feature.

- **Unit Tests** verify:
    - The message is marked as deleted locally.
    - The delete request function works properly.
        
- **Integration Tests** would verify:
    - The delete request reaches the server.
    - The server correctly updates the message status.
    - The message disappears from **both sender and receiver’s** chat window.
    - The UI refreshes to reflect this.
        
Even if each part passes unit tests, if **data isn't flowing correctly**, integration testing will catch it.

---

## ✅ Summary

|Aspect|Details|
|---|---|
|**Definition**|Testing interactions between integrated modules/components|
|**Goal**|Ensure modules work together correctly|
|**Performed by**|Both **developers** (via code) and **testers** (via UI/API/manual)|
|**Tools**|Postman, REST Assured, JUnit, integration pipelines in CI/CD|
|**For Testers**|Helps test feature-to-feature flows, catch real-world bugs, and plan better|