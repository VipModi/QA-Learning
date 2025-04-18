#compliance #law
## 🏛️ CCPA (California Consumer Privacy Act) – USA (California)

📍 **Region:** California, USA  
🗓️ **Enforced:** January 1, 2020  
🔁 **Expanded by:** CPRA (2023)  

🎯 **Focus:** Give users control over their **personal data** and how it’s **collected, used, or sold**

#### 📜 **What It Is:**  
A privacy law for **California residents** that forces businesses like Meta to be transparent about data practices and gives users strong rights like deletion, access, opt-out, and correction.

---

## 🔍 What’s Covered:

|🛡️ Rule|📱 Example (Meta Apps)|
|---|---|
|**Right to Know**|Download a copy of your data from Facebook (posts, likes, messages, etc.)|
|**Right to Delete**|Permanently delete your Instagram account and data|
|**Right to Opt-Out**|Use “Do Not Sell My Info” on Messenger to stop third-party sharing|
|**Right to Non-Discrimination**|Meta can’t limit features if you opt out of tracking|
|**Right to Correct**|Correct name or gender in Facebook profile if it's incorrect|

---

## 🧪 As a Tester:

|✅ Task|💡 Example|
|---|---|
|Test “Download My Info” flow|Ensure Messenger exports all chat history and metadata|
|Simulate Data Deletion|Verify Facebook deletes posts, messages, photos permanently|
|Check Opt-Out Behavior|Use a test user to opt-out and ensure no tracking continues|
|Consent Testing|Test toggles like “Allow Ads Personalization” are respected|
|Validate Privacy Policy Links|Ensure “Do Not Sell My Info” is accessible and functional|

---

## 🔍 Key Rules:

- Meta must tell users **what data is collected** and **why**.
- Users must be able to **delete**, **access**, or **opt out** of data sale.
- **Cookies, pixel tracking, and targeted ads** must comply with user preferences.
- Meta **can’t penalize users** for exercising these rights.
- **Biometric data** (e.g., facial recognition) is protected and must be used transparently.

---

## 📲 Impact on Meta & Its Apps:

| **Platform**  | **Impact**                                                                |
| ------------- | ------------------------------------------------------------------------- |
| **Facebook**  | Must offer clear opt-outs for data selling; strict deletion flow required |
| **Instagram** | User must be able to delete or download data anytime                      |
| **Messenger** | Consent required before analyzing message content for ads                 |
| **WhatsApp**  | Clear controls for data sharing with Facebook (especially after backlash) |
📋 **Example Test Scenario (API):**  
**API:** `POST /user/opt-out-sale`  
✅ Expected:
- Immediately stops sale of user data
- Confirmed with user and logged
- Only accessible by verified California residents

📉 **Impact of Violation:**
- Penalties up to **$7,500 per violation**
- Class action lawsuits possible
- Public shaming via California Attorney General’s disclosures