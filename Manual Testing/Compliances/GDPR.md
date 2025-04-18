#compliance #law
## 🌍 GDPR (General Data Protection Regulation) – EU Law

📍 Region: EU  
🗓️ Enforced: 2018  
🎯 Focus: Protect personal data of users and give them control.

#### 📜 What It Is: 
A comprehensive data privacy law that protects how companies collect, store, and use personal data of EU citizens, regardless of where the company is based.

#### 🔍 What’s Covered:

| **Area**           | **Explanation**                                             | **Example in Meta**                                                                                           |
| ------------------ | ----------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- |
| Consent Management | Apps must ask explicit permission for data tracking or ads. | Instagram must show a banner asking: “Allow Instagram to track your activity across other apps and websites?” |
| Right to Access    | Users can request a copy of all their data.                 | WhatsApp → Settings → Request account info → Gets a .zip of chats, metadata                                   |
| Right to Erasure   | Users can delete their account and all associated data.     | Facebook: “Delete My Account” deletes posts, friends, and stored metadata                                     |
| Data Portability   | Users can download and move their data to another app.      | Instagram allows you to export all posts and messages                                                         |
| Data Minimization  | Only collect data that is necessary for service.            | WhatsApp should not ask for GPS unless needed for a feature like location sharing                             |

#### 🔧 As a Tester:
- Check if cookies and ads are disabled by default until user gives consent.  
- Verify that exported data is complete and readable.  
- Try deleting an account → ensure no data remains in backend (ask dev if needed). 
- Capture bugs like:  
	- “No proper consent flow before Facebook shows ads”  
	- “User profile is not completely deleted after deletion request”  

### 🔍 Key Rules:

- Explicit Consent: You must ask before tracking, storing cookies, or collecting personal info.  
- Right to Access: Users can request a copy of their data.  
- Right to Erasure: Users can request that their data be deleted (“Right to be forgotten”).  
- Data Portability: Users should be able to export their data easily.  
- Data Breach Notification: Must notify users within 72 hours of breach.

### 📲 Impact on Meta:

- Facebook and Instagram must clearly ask for consent before showing personalized ads.  
- WhatsApp must not share data with Facebook without opt-in.  
- All Meta platforms must have a “Download My Data” and “Delete Account” feature.  
- Meta has faced hefty fines (millions of euros) for non-compliance.

### 🛡️ GDPR Compliance Testing Checklist (Data Privacy)

| **Area**            | **Checklist Item**                                          | **Example / Notes**                                                       |
| ------------------- | ----------------------------------------------------------- | ------------------------------------------------------------------------- |
| Consent             | Explicit consent before collecting personal data            | Show opt-in checkboxes (not pre-checked) for location, analytics, cookies |
| Right to Access     | User can request/download their data                        | "Download My Data" feature                                                |
| Right to Delete     | User can permanently delete their account/data              | "Delete My Account" → backend data also removed                           |
| Cookie Consent      | Cookie banner visible on first visit                        | Must include “Accept” and “Customize” options                             |
| Privacy Policy      | Easily accessible, clear, and in user’s language            | Footer + account settings link                                            |
| Third-Party Sharing | Disclose any data shared with 3rd parties                   | Analytics, ad providers, etc.                                             |
| Data Minimization   | Only collect data needed for function                       | Don’t collect phone number unless required                                |
| Security Controls   | User data stored & transmitted securely (HTTPS, encryption) | No sensitive data in logs or URLs                                         |

📋 **Example Test Scenario (API):**  
**API:** `DELETE /user/account`  
✅ Expected:
- User's personal data is **completely erased** (“right to be forgotten”)
- Operation is **logged**, secure, and irreversible
- Only authenticated user can trigger it

📉 **Impact of Violation:**
- Fines up to **€20 million or 4% of global revenue**
- Severe **brand damage and user distrust**