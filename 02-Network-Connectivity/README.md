# Ticket #1042: User Cannot Access the Internet

### 📞 The Ticket Submission
* **User:** Sarah Jenkins (Marketing)
* **Issue:** "My internet is down. I can't access Google or our internal shared drive. Everyone else around me is fine. Need help ASAP!"

### 🔍 Troubleshooting & Action Steps
1. **Physical Layer Check:** Asked the user to verify the Ethernet cable was securely plugged into both the wall jack and the docking station. (Confirmed).
2. **IP Configuration Check:** Opened Command Prompt and ran `ipconfig /all`. 
   * *Finding:* The machine had an IP address of `169.254.1.45`.
   * *Root Cause Analysis:* A `169.254.x.x` address means **APIPA** (Automatic Private IP Addressing). The computer could not talk to the DHCP server to grab a real, valid IP address.
3. **Resolution:** * Ran `ipconfig /release` to drop the bad configuration.
   * Ran `ipconfig /renew` to request a fresh IP from the DHCP server.
   * The machine successfully grabbed a valid corporate IP (`192.168.1.75`).

### 💬 Customer Service Response (What I told the user)
*"Hi Sarah, it looks like your computer temporarily lost its connection to our network router and assigned itself a placeholder address. I’ve refreshed your network connection, and you should be fully back online now. Please let me know if your shared folders are loading properly!"*
