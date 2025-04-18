#compliance #law
### 📘 What is Compliance Testing?

Compliance Testing (also called Conformance Testing) ensures that the software system adheres(follows) to legal, regulatory, or organizational standards — such as [[GDPR]], [[HIPAA]], [[ePrivacy Directive]] , [[WCAG]], etc.

### 📌 Why is Compliance Testing Important?

Because failure to comply can result in:

- ⚠️ Legal penalties or fines  
- 😡 Loss of user trust  
- 🔐 Security vulnerabilities  
- 🛑 Blocking of app by regulators (like EU’s DMA/EAA rules) 

### 🔍 Examples of Compliance Standards:

| **Domain**        | **Standard**                     | **Purpose**                                       |
| ----------------- | -------------------------------- | ------------------------------------------------- |
| Privacy           | [[GDPR]], [[ePrivacy Directive]] | Data protection for EU citizens                   |
| Accessibility     | [[WCAG]], [[EAA]]                | Makes app usable for people with disabilities     |
| Security          | [[ISO 27001]], [[PCI DSS]]       | Protects sensitive data (esp. for finance/e-comm) |
| Healthcare        | [[HIPAA]]                        | Protects patient health data (USA)                |
| Social Media (EU) | [[DMA]], [[DSA]]                 | Regulates fairness and transparency               |

### 🧪 Tester’s Role in Compliance Testing:

- Verifying data privacy controls (e.g., opt-in/opt-out, consent)  
- Ensuring accessibility (e.g., screen reader compatibility)  
- Testing for secure data storage & transfer  
- Reviewing audit logs & user rights  
- Reporting violations of compliance standards 
### 💡 Real-World Example (Messenger App):

Let’s say you’re testing a chat app in the EU:
- 🔒 Users must explicitly consent before tracking their activity (GDPR)  
- ♿ App must work with keyboard-only navigation and screen readers (WCAG)  
- 🌍 App must support multi-language disclosures and cookie preferences (ePrivacy)

| ⚖️ Compliance                                                          | 🧾 **Definition**                                                 | 🎯 **Goal**                                                 | ✅ **What Needs to Comply**                                                                  |
| ---------------------------------------------------------------------- | ----------------------------------------------------------------- | ----------------------------------------------------------- | ------------------------------------------------------------------------------------------- |
| **GDPR**  <br>_(General Data Protection Regulation)_                   | EU law on data privacy and protection                             | Give individuals control over their personal data           | Apps/services collecting or processing personal data of EU users                            |
| **HIPAA**  <br>_(Health Insurance Portability and Accountability Act)_ | US law to protect health info (PHI)                               | Ensure privacy & security of health records                 | Healthcare providers, insurers, apps handling **PHI**                                       |
| **DMA**  <br>_(Digital Markets Act)_                                   | EU regulation targeting Big Tech gatekeepers                      | Promote fair competition & user freedom                     | Large platforms (search, messaging, ads) designated as **gatekeepers**                      |
| **ePrivacy Directive**  <br>(EU Cookie Law)                            | EU law focused on privacy in electronic communications            | Control tracking (e.g., cookies) and communications secrecy | Any service using cookies, email/SMS tracking, behavioral ads                               |
| **EAA**  <br>_(European Accessibility Act)_                            | EU directive on accessibility                                     | Ensure equal digital access for disabled users              | Hardware, software, websites, apps, ATMs, e-readers in the EU                               |
| **WCAG**  <br>_(Web Content Accessibility Guidelines)_                 | Global standard for digital accessibility                         | Provide inclusive access to web/mobile content              | Websites, mobile apps, documents, videos — globally recognized                              |
| **ISO 27001**                                                          | International standard for Information Security Management (ISMS) | Secure sensitive business and customer data                 | Organizations managing confidential or sensitive info (e.g., B2B SaaS, finance, healthcare) |
| **PCI DSS**  <br>_(Payment Card Industry Data Security Standard)_      | Global standard for payment card security                         | Protect cardholder data from theft and fraud                | Merchants, apps, or services storing/transmitting card data                                 |