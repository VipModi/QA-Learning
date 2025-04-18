
## ✅ **What is Severity?**

**Severity** refers to **how serious the bug is** in terms of **functionality or system impact**.

> 🔧 **It is determined by QA/Testers.**

### Severity Levels:

|Common Label|Alternate Label (Used in Some Projects)|Description|
|---|---|---|
|**Critical**|Blocker / Showstopper|Complete failure. App crashes, data loss, system down. No workaround.|
|**High**|**Major**|Important functionality is broken, but the app still runs. Workaround may exist.|
|**Medium**|**Normal / Moderate**|Bug in a non-core feature, or not always reproducible.|
|**Low**|**Minor**|Small issue, like spacing/alignment problems or rare edge cases.|
|_(Lowest)_|**Trivial / Cosmetic**|Typos, color mismatches, icon padding, etc. No user impact.

---

## ✅ **What is Priority?**

**Priority** refers to **how soon the bug should be fixed** based on **business or release goals**.

> 📅 **It is usually decided by the Product Manager or QA Lead.**

### Priority Levels:

|Level|Meaning|
|---|---|
|**High**|Needs immediate fix for release.|
|**Medium**|Should be fixed, but not urgent.|
|**Low**|Can be fixed in future releases.|

---

## 🎯 Severity vs Priority – Key Differences

|Feature|Severity|Priority|
|---|---|---|
|Who sets it|QA/Testers|PM / Dev Lead / QA Lead|
|Focus|Technical impact|Business urgency|
|Type|Objective|Subjective|
|Change Rate|Rarely changes|Can change frequently|

---

## 🧪 Real-World Examples from a Messaging App

|Scenario|Severity|Priority|Why|
|---|---|---|---|
|App crashes on clicking "Send Message"|Critical|High|Core feature broken, must fix now.|
|Typo in "You have new mesage"|Low|Medium|Not urgent, but looks unprofessional.|
|Profile picture doesn’t load on dark mode|Medium|Low|Doesn’t block user, low business impact.|
|Privacy toggle not working (users can’t hide status)|High|High|Affects user trust and compliance.|
|Emoji reactions misaligned on desktop only|Low|Low|Minor visual issue on less-used platform.|

---

## 🎯 **4 Common Combinations of Severity and Priority**

|Severity|Priority|Description|
|---|---|---|
|High|High|Urgent and serious — must fix now|
|High|Low|Serious bug, but not urgent (low business impact)|
|Low|High|Not serious, but urgent to fix (e.g., client request)|
|Low|Low|Minor issue, not urgent — can wait|

---

## 🧪 **Scenario-Based Examples for Each Combination**

---

### 🔴 1. **High Severity + High Priority**

> **“The app crashes when sending a message.”**

- **Severity**: High — a **core feature** is broken.
- **Priority**: High — must fix before release.
- ✅ This is a **showstopper bug**.
    

---

### 🟠 2. **High Severity + Low Priority**

> **“App crashes when accessing an old archived chat (very rare, not often used).”**

- **Severity**: High — crash is a serious issue.
- **Priority**: Low — it happens only on an old feature used by few users.
- ✅ Fix is **important but can be deferred**.
- Other: 
	- UI misalignment on the home screen
	- Incorrect button label on a rarely used feature
	- Spelling mistake in the footer or legal terms section
	- Minor color issue on a non-critical element like a tooltip
	- Broken link in a non-essential, rarely visited page
    

---

### 🟡 3. **Low Severity + High Priority**

> **“The client logo is misaligned on the login screen.”**

- **Severity**: Low — doesn’t affect functionality.
- **Priority**: High — it’s a client branding concern and must be fixed before demo/release.
- ✅ Must fix it **quickly even though it’s a small issue**.
- Other  : 
	- Security vulnerability affecting only a small set of users
	- Major performance issue impacting a rarely used feature
	- Data corruption in a feature used by a limited user group
	- Critical bug in an outdated version of the app that's rarely used
	- Server crash during off-peak hours, affecting few users
    

---

### 🟢 4. **Low Severity + Low Priority**

> **“Spacing issue in the footer of settings page on tablets only.”**

- **Severity**: Low — visual only.
- **Priority**: Low — not many users see it; can be fixed later.
- ✅ Fix when there’s time — **not urgent at all**.
    

---

## 🧠 Bonus: Table for Interview Quick Recap

|Severity|Priority|Example|
|---|---|---|
|High|High|Messaging crash on Android|
|High|Low|Rarely used view crashes in app|
|Low|High|Client logo misaligned in banner|
|Low|Low|Padding issue in terms & conditions page|
## 💡 Pro Tip for Interviews:

> "Severity is about how **bad** the bug is. Priority is about how **fast** it should be fixed."

You can even say:

> "High severity ≠ always high priority. A crash on a hidden settings page might be high severity but low priority."