#compliance #law
## ♿ EAA (European Accessibility Act) – EU Law (enforced 2025 onward)

📍 Region: EU  
🗓️ Enforced: From **June 28, 2025** (law passed in 2019)  
🎯 Focus: Make digital services accessible to people with disabilities

#### 📜 What It Is: 
Requires digital services (apps/websites) to be accessible to people with disabilities.
The **EAA** mandates that all major digital services (including social media apps like Facebook, Instagram, WhatsApp, Messenger) must be **accessible** to people with **visual, auditory, cognitive, or motor impairments**. It aligns with **WCAG 2.1** (Web Content Accessibility Guidelines).


#### 🔍 What’s Covered:

| **Feature**           | **Example in Meta Apps**                                          |
| --------------------- | ----------------------------------------------------------------- |
| Screen Reader Support | VoiceOver or NVDA should read all buttons/texts on Facebook       |
| Keyboard Navigation   | Use Tab/Shift+Tab to move through Instagram feed                  |
| Alt Text for Images   | Instagram must allow user to write alt text or auto-generate      |
| High Contrast Mode    | Support dark mode or contrast settings                            |
| Error Handling        | “Password is incorrect” must be announced for screen reader users |

#### 🧪 As a Tester:

- Use screen reader tools (NVDA for Windows, VoiceOver for Mac)  
- Try zooming the screen to 200%  
- Test all forms/buttons with keyboard only 

|✅ Task|💡 Example|
|---|---|
|Check Screen Reader Support|Use TalkBack or VoiceOver to navigate Messenger app|
|Test with Keyboard Only|Navigate Instagram web version using **Tab/Shift+Tab**|
|Validate Alt Text|Verify that uploaded images on Facebook auto-generate or allow manual alt text|
|Color Contrast|Use tools like **axe** or **Lighthouse** to check contrast ratio on WhatsApp|
|Video/Audio Accessibility|Ensure captions are shown by default in video content|

#### 🔍 Key Rules:

- Must support **screen readers** (e.g., VoiceOver, NVDA)
- **Color, text, layout** must support people with **low vision or color blindness**
- Apps must be usable **with assistive technologies**
- Content must **not rely on audio alone** (e.g., include captions)
- Error messages must be **clear and announced to screen readers**

#### 📲 Impact on Meta:

- Facebook and Messenger must be fully usable by screen readers.  
- Instagram must offer alt text for images and ensure keyboard navigability.  
- All Meta apps need accessible error messages, proper focus, and more.

| Platform      | Required Changes                                                                  |
| ------------- | --------------------------------------------------------------------------------- |
| **Facebook**  | Must support accessible form fields, error handling, and alt text for every image |
| **Instagram** | Image alt-text auto-generation; accessible stories and reels                      |
| **Messenger** | Voice messages need transcripts; navigation support for screen readers            |
| **WhatsApp**  | Improve contrast, allow magnification, transcripts for voice notes                |

**API:** `GET /user/settings/accessibility`  
✅ Expected:
- Supports screen readers, text scaling, captions
- Returns enabled accessibility features
- Works across web/mobile/TV devices

📉 **Impact of Violation:**
- Platform may be **excluded from EU markets**
- Legal complaints from disabled users or watchdog groups
- Negative **press and brand perception**