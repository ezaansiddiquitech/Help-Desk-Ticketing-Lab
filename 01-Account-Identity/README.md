```markdown
# Ticket #1102: Locked Out of Microsoft 365 (MFA)

### 📞 The Ticket Submission
* **User:** Elena Rostova (HR)
* **Issue:** "I got a new phone over the weekend. Now when I try to log into my email, it sends a verification code to my old phone, which I don't have anymore. Help!"

### 🔍 Troubleshooting & Action Steps
1. **Identity Verification:** Before making security changes, verified Elena's identity by calling her via an approved company contact number and confirming her employee ID.
2. **Admin Action:** Logged into the **Microsoft Entra ID admin center** (formerly Azure AD).
3. **Resolution:** 
   * Located Elena’s user profile.
   * Navigated to *Authentication methods* and selected **Require re-register multifactor authentication**.
   * This cleared her old phone data and forced her login screen to prompt her to scan a new QR code.

### 💬 Customer Service Response (What I told the user)
*"Hi Elena, I have reset your authentication settings from the admin dashboard. The next time you log in to your email, it will prompt you to set up the Microsoft Authenticator app on your new phone as if it were your first time. Let me know if you run into any snags during the setup!"*
