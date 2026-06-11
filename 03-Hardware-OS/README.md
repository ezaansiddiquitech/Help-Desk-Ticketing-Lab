### Step 3: Paste the Hardware/OS Ticket Content
Copy this entire block below and paste it into the large main text box:

```markdown
# Ticket #1099: Laptop Crashing Frequently (BSOD)

### 📞 The Ticket Submission
* **User:** Mark Davis (Finance)
* **Issue:** "My laptop randomly reboots and shows a blue screen with a sad face. It happened twice this morning while working on budget spreadsheets."

### 🔍 Troubleshooting & Action Steps
1. **Gathering Info:** Asked the user if any new software or hardware was added recently. Mark mentioned he plugged in a new external webcam yesterday.
2. **Reviewing Logs:** Booted the machine, opened **Event Viewer**, and navigated to *Windows Logs > System*. Looked for critical errors at the exact times of the crashes.
3. **Finding:** Found an error pointing to a corrupted driver file related to the new webcam (`uvcvideo.sys`).
4. **Resolution:** 
   * Disconnected the webcam.
   * Opened **Device Manager**, located the webcam under "Imaging devices," right-clicked, and selected **Uninstall Device**.
   * Re-downloaded the official, stable driver directly from the manufacturer's website and installed it.

### 💬 Customer Service Response (What I told the user)
*"Hi Mark, I found the culprit! The software driver for your new webcam was conflicting with Windows, which caused the blue screen crashes. I have uninstalled the broken software and replaced it with the official, stable version. Go ahead and use your laptop normally, and please reopen this ticket if it crashes again."*
