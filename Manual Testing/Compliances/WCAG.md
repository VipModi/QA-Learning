#compliance #law

## ♿ WCAG (Web Content Accessibility Guidelines)

📍 **Created by:** W3C (World Wide Web Consortium)  
🗓️ **Current Version:** **WCAG 2.1** (WCAG 2.2 was released in 2023)  
🎯 **Purpose:** Make **web and mobile content accessible** to **people with disabilities**

---

#### 📜 What It Is:

WCAG is a **global standard** for digital accessibility. It ensures websites, apps, and software are **usable by people with visual, auditory, physical, speech, cognitive, language, learning, and neurological disabilities**.

Apps like **Messenger, Facebook, Instagram, and WhatsApp** must follow WCAG to comply with laws like **EAA** and **ADA**.

---

#### 📦 WCAG is Based on 4 Pillars (POUR):

| 🧩 Principle       | 📝 Meaning                  | 💡 Example                                              |
| ------------------ | --------------------------- | ------------------------------------------------------- |
| **P**erceivable    | Users can perceive the info | Alt text for images on Instagram                        |
| **O**perable       | Users can navigate it       | Tab through Messenger chat list using keyboard          |
| **U**nderstandable | Info and UI must be clear   | Error messages on Facebook forms are easy to understand |
| **R**obust         | Compatible with tools       | WhatsApp works with screen readers like VoiceOver, NVDA |

---

#### 🔍 Key WCAG 2.1 Guidelines (with Examples):

|Guideline|Description|Meta App Example|
|---|---|---|
|**Alt Text**|Provide alternative text for images|Instagram alt text for screen readers|
|**Keyboard Navigation**|All functions should be accessible via keyboard|Messenger chat list navigation|
|**Color Contrast**|Text should be readable over background|WhatsApp chat screen readability|
|**Resizable Text**|Allow zooming without breaking layout|Facebook posts readable at 200% zoom|
|**Labels for Inputs**|Forms must have visible and screen-reader-friendly labels|Facebook login form|
|**Error Identification**|Errors should be easy to find and fix|"Invalid email" messages in login forms|

---

#### 🧪 As a Tester (Your Tasks):

|✅ What to Test|🔍 Tools or Methods|
|---|---|
|Screen reader support|VoiceOver (iOS), TalkBack (Android), NVDA (Windows)|
|Keyboard navigation|Use only Tab/Shift+Tab/Enter|
|Contrast ratio|Use tools like Axe, Lighthouse, or Color Contrast Analyzer|
|Zoom up to 200%|No horizontal scroll or broken layout|
|Input form labels|Check for ARIA labels or proper `<label>` usage|
|Captions on media|Ensure YouTube/Facebook videos include subtitles|

---

#### 📈 WCAG Levels of Compliance:

|Level|Meaning|
|---|---|
|**A**|Basic accessibility (minimum requirement)|
|**AA**|Industry standard, required for most laws (✅ Recommended)|
|**AAA**|Highest level (hard to achieve everywhere)|

---

#### 📲 Impact on Meta:

|App|WCAG-Based Changes|
|---|---|
|Facebook|Enhanced post visibility for screen readers, form labels|
|Instagram|Alt-text generation and manual override for posts|
|Messenger|Full keyboard navigation, proper screen reader focus|
|WhatsApp|Voice message transcripts, scalable font sizes|

| Area                    | Checklist Item                                | Example / Notes                                  |
| ----------------------- | --------------------------------------------- | ------------------------------------------------ |
| ✅ Keyboard Navigation   | All features can be accessed via keyboard     | Tab, Enter, Space, Shift+Tab                     |
| ✅ Screen Reader Support | Elements have proper labels, roles, alt texts | Use semantic HTML, aria-label, alt tags          |
| ✅ Color Contrast        | Text/background contrast is 4.5:1 or higher   | Avoid light gray on white                        |
| ✅ Text Resize           | Text should be readable even at 200% zoom     | Layout should not break                          |
| ✅ Error Messaging       | Clear, accessible error messages with focus   | e.g., “Invalid email” announced by screen reader |
| ✅ Captions/Subtitles    | For videos or voice notes                     | Add transcript/captions where needed             |
| ✅ Time-Out Warning      | Warn before session timeout                   | Include “Extend Session” option                  |
| ✅ No Motion Triggers    | Avoid auto-playing animations                 | Provide user controls                            |

---

#### 🔁 Bonus: Process Tips for Testers

- 🧪 Use Accessibility Testing Tools: Axe, Wave, Chrome DevTools, NVDA/VoiceOver 
- 🔐 Check Network Requests: Inspect API calls to see if PII (personal data) is exposed  
- 📄 Work with Legal/Compliance Teams: Get their sign-off on policies and flows  
- 📷 Take Screenshots & Recordings: Helpful when submitting bugs or compliance reports


📋 **Example Test Scenario (API):**  
**API:** `GET /page/metadata`  
✅ Expected:
- Includes **ARIA roles**, alt text references, and label mappings
- Color contrast and tab order follow WCAG 2.1 AA
- Dynamic content supports keyboard navigation

📉 **Impact of Violation:**
- Legal action (especially in US, Canada, EU) under ADA, EAA, etc.
- Risk of **accessibility lawsuits**
- Poor user experience for people with disabilities = **reputational harm**