#compliance #law
## 🏛️ DMA (Digital Markets Act) – EU Law (2023 Onward)

📍 Region: EU  
🗓️ Enforced: 2024–25  
🎯 Focus: Prevent abuse by Big Tech Gatekeepers

#### 📜 What It Is: 
Targets “gatekeepers” like Meta, Google, Apple to ensure fair competition and give users more control over their data and app ecosystem.

#### 🔍 What’s Covered:

| **Rule**                | **Example**                                                                 |
| ----------------------- | --------------------------------------------------------------------------- |
| Cross-App Communication | Messenger must allow sending messages to Signal, Telegram via API           |
| Data Separation         | WhatsApp data cannot be auto-shared with Facebook Ads without user approval |
| Unbundling              | Facebook login should not be forced for Instagram                           |
| Self-preferencing ban   | Facebook can’t push Reels while hiding TikTok links                         |

#### 🧪 As a Tester:

- Try logging into Instagram without Facebook → should work  
- Try linking WhatsApp and Facebook → must require consent  
- Report:  
	- “Reels are getting promoted at top; TikTok links being hidden” (violates DMA)  
	- “Messenger doesn’t allow incoming messages from other apps”

#### 🔍 Key Rules:

- Must allow cross-platform communication (e.g., Messenger ↔ Signal/Telegram in future). 
- Users must choose default services (e.g., not be forced into Facebook login).  
- No mixing of data between apps without consent (e.g., WhatsApp & Facebook).  

#### 📲 Impact on Meta:

- Messenger may have to allow messages from other apps (via interoperability APIs).  
- Facebook cannot automatically use WhatsApp data for ad targeting.  
- Instagram can’t use its monopoly to promote Reels over competitors.

📋 **Example Test Scenario (API):**  
**API:** `GET /user/consent-status`  
✅ Expected:
- Returns accurate data-sharing consent flags
- Default setting is **opt-out** for third-party data sharing
- Consent can be easily revoked

📉 **Impact of Violation:**
- Fines up to **10% of global annual turnover**
- Strict scrutiny from EU Commission