
## 🐞 **What is Bug Life Cycle (Defect Life Cycle)?**

The **Bug Life Cycle** (or **Defect Life Cycle**) is the **journey of a bug** from the moment it is found until it is closed. It defines the **statuses** a bug goes through and the **actions** taken by testers and developers at each stage.

---

## 🔁 **Typical Bug Life Cycle Phases (with Example)**

|Status|Description|Who is Involved|Example|
|---|---|---|---|
|**New**|Bug is logged for the first time.|QA|You find that "mute chat" doesn’t persist after app restart and raise it in JIRA.|
|**Assigned**|Bug is assigned to a developer.|Team Lead / QA Lead|Lead assigns the bug to the iOS developer.|
|**Open**|Dev starts investigating/fixing the issue.|Developer|Dev confirms issue is valid and begins fixing it.|
|**Fixed**|Dev has made the fix and submitted the code.|Developer|Dev updates backend toggle logic and marks as Fixed.|
|**Ready for Retest**|Build with fix is available for testing.|QA / Dev|You get the updated build and prepare to retest.|
|**Retesting**|QA tests the fix.|QA|You verify mute is now persisting after app restart.|
|**Reopen** (optional)|Bug still exists even after fix.|QA|If issue still exists, you mark it as Reopen.|
|**Verified**|QA confirms the bug is fixed.|QA|You verify issue is fully fixed across all platforms.|
|**Closed**|Bug is permanently fixed, no further action.|QA|You close the ticket in JIRA after verification.|
|**Rejected** / **Not a Bug** (optional)|Dev disagrees with the bug or it’s invalid.|Developer|Bug raised was due to wrong test data. Dev rejects it.|
|**Deferred** (optional)|Bug is valid but postponed for future.|PM / Dev / QA|Low priority bug: “Minor color issue on info icon” deferred to next release.|
|**Duplicate** (optional)|Same issue already reported.|QA / Dev|Bug already exists under another ticket ID.|

---

## 📊 **Bug Life Cycle Flow (Visual in Text Format)**

```
New → Assigned → Open → Fixed → Ready for Retest → Retesting → Verified → Closed
         ↑         |                                   ↓      
		  ←        |        ←           ←        ←   Reopen	
				   ↓
	Duplicate | Rejected | Differed | Not a Bug	
```
													

---

## 🧪 Example from Your Project (Messenger)

Imagine you're testing **"Edit Message" feature**:

1. 🔍 You notice that **edited messages don’t update in dark mode** → Raise bug = **New**
2. 🧑‍💻 Bug is assigned to frontend dev → **Assigned**
3. Dev investigates and starts fix → **Open**
4. Fix is pushed in latest build → **Fixed**
5. You retest in mobile + desktop → **Retesting**
6. Bug is verified on all platforms → **Verified**
7. You mark bug as **Closed**
    

---

## 🧠 Pro Tips (for Interviews + Real Projects)

- Use **clear steps to reproduce (STR)** when logging.
- Always attach **screenshots, logs, or videos**.
- Tag correct severity (**Critical, Major, Minor**) and priority (**High, Medium, Low**).
- Maintain **strong communication** with devs and triage team.