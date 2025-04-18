
### **Definition:**  
SDLC is a **systematic process** used to **develop, test, deploy, and maintain** software. It ensures **high-quality software** is delivered efficiently.

---

## 🔄 **Phases of SDLC (with QA Role & Example)**

|Phase|Description|QA Involvement|Real-Life Example|
|---|---|---|---|
|1. **Requirement Gathering**|Understanding what the client/user wants.|Involved in requirement reviews, checking for testability.|User wants a new "mute chat" feature in a messaging app.|
|2. **Design**|Architects plan how the system will be built (UI, DB, components).|QA reviews design to plan test strategy and identify possible risks.|The "mute" feature will be implemented with a toggle and backend flag.|
|3. **Implementation (Coding)**|Developers start coding based on design.|QA prepares test cases, test data, and test environments.|Dev builds mute toggle for chat threads. QA writes test cases like "Mute works across app restarts".|
|4. **Testing**|QA team executes test cases and reports defects.|Primary phase for QA: Functional, UI, Regression, Compliance testing, etc.|QA finds bug: Mute option not working in dark mode.|
|5. **Deployment**|Code is moved to production after passing testing.|QA may perform sanity/smoke testing on production or staging.|The mute feature goes live. QA checks if it works after deployment.|
|6. **Maintenance**|Bug fixes, updates, and support after release.|QA tests bug fixes, performs regression, and supports new updates.|Post-release, QA tests a patch that fixes mute settings not saving.|

---

## 🎯 **Why SDLC Matters for QA/Testers**

- Helps you understand **where you fit in** each phase.
- Improves **test planning and coverage**.
- Encourages early involvement (helps with early bug detection).
- Helps manage **risk and quality** throughout the lifecycle.
    

---

## 🛠️ **Common SDLC Models**

|Model|Description|When to Use|
|---|---|---|
|**Waterfall**|Sequential flow (one phase after another).|For small, clearly defined projects.|
|**V-Model**|Each development phase has a corresponding test phase.|Good for strict validation (like compliance testing).|
|**Agile**|Iterative and incremental with sprints.|Preferred for dynamic, changing requirements (your Messenger project likely used this).|
|**Spiral**|Combines iterative dev + risk analysis.|For large, complex, high-risk projects.|

---

## 🧪 Example From Your Domain (Messaging App)

- **Requirement:** "Add auto-delete messages after 24 hours."
- **Design:** Devs plan how messages expire in database and UI.
- **Implementation:** Feature is developed for both mobile and web.
- **Testing:** You test for:
    - Messages disappearing after 24 hours
    - Functionality across platforms (mobile/web/VR)
    - Edge cases (e.g., message timezones, unsent messages)
- **Deployment:** You test it in production (Smoke + Sanity).
- **Maintenance:** You verify a fix for a bug where deleted messages were still visible via notification.
    

---

## 📝 Summary

**SDLC = Planning + Building + Testing + Releasing + Maintaining software.**

As a **QA**, your role is crucial in every phase — not just testing. You ensure the product meets **requirements, quality, and user expectations**.