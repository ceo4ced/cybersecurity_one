# CYBER.ORG Range - Student Credential Lookup Tool

A secure, single-page web application for students to look up their CYBER.ORG Range login credentials using their Student ID.

## 🔗 Live Access

**Student Access URL:** `https://ceo4ced.github.io/cybersecurity_one/CyberRange_Password_Lookup.html`

## 🚀 Quick Setup: Enable GitHub Pages

1. Navigate to your repository settings:
   - Go to: `https://github.com/ceo4ced/cybersecurity_one/settings/pages`

2. Configure GitHub Pages:
   - **Source:** Deploy from a branch
   - **Branch:** `main`
   - **Folder:** `/ (root)`
   - Click **Save**

3. Wait 1-2 minutes for deployment

4. Access your live page at the URL shown in the green confirmation box

## 📋 Features

✅ **Secure Lookup** - Students enter their Student ID to retrieve credentials  
✅ **3-Attempt Lockout** - Automatic 30-minute lockout after 3 failed attempts  
✅ **FERPA Compliant** - Student names are hashed for privacy  
✅ **Persistent Security** - Lockout status persists across page refreshes using localStorage  
✅ **Auto-Reset Timer** - Lockout automatically expires after 30 minutes  
✅ **Mobile Responsive** - Works on all devices

## 👨‍🏫 Teacher Instructions

### Share with Students

Share this direct link with your students:
```
https://ceo4ced.github.io/cybersecurity_one/CyberRange_Password_Lookup.html
```

You can also create a shortened link using:
- [bit.ly](https://bitly.com)
- [tinyurl.com](https://tinyurl.com)

### Unlock a Locked-Out Student

If a student gets locked out and needs immediate access:

1. Ask the student to open their browser's **Developer Console**:
   - **Chrome/Edge:** Press `F12` or `Ctrl+Shift+J` (Windows) / `Cmd+Option+J` (Mac)
   - **Firefox:** Press `F12` or `Ctrl+Shift+K` (Windows) / `Cmd+Option+K` (Mac)
   - **Safari:** Enable Developer Menu first, then `Cmd+Option+C`

2. In the console, type this command and press Enter:
   ```javascript
   localStorage.removeItem('cyberrange_lookup_data'); location.reload();
   ```

3. The page will refresh and the student can try again

### Update Student Credentials

To update the student list:

1. Edit `CyberRange_Password_Lookup.html`
2. Locate the `credentials` object in the `<script>` section
3. Update student data following this format:
   ```javascript
   "STUDENT_ID": { 
     hash: "Student #XXXX", 
     username: "UUID", 
     password: "UUID" 
   }
   ```
4. Commit and push changes to GitHub
5. GitHub Pages will auto-update in 1-2 minutes

## 🎓 Student Instructions

1. Visit the credential lookup page
2. Enter your **Student ID Number** (10-12 digits)
3. Click "🔍 Look Up My Credentials"
4. Copy your username and password
5. Go to **apps.cyber.org** and log in

⚠️ **Important:**
- You have **3 attempts** to enter the correct Student ID
- After 3 failed attempts, you'll be locked out for 30 minutes
- Keep your password confidential - do not share with classmates
- If you have issues, contact Mr. Williams

## 🔧 Technical Details

- **Technology:** HTML, CSS, JavaScript (no dependencies)
- **Data Storage:** Client-side localStorage (no server required)
- **Security:** 3-attempt rate limiting with time-based lockout
- **Privacy:** FERPA-compliant hashed student identifiers
- **Hosting:** GitHub Pages (free static hosting)

## 🐛 Troubleshooting

### Issue: "Student Not Found"
- **Solution:** Double-check your Student ID number
- **Solution:** Ensure you're using the ID number, not your name
- **Solution:** Contact Mr. Williams if the problem persists

### Issue: Locked out before 30 minutes
- **Solution:** Clear browser cache and cookies
- **Solution:** Use a different browser
- **Solution:** Contact Mr. Williams for manual reset

### Issue: Page not loading
- **Solution:** Wait 2-3 minutes after enabling GitHub Pages
- **Solution:** Check that GitHub Pages is enabled in repository settings
- **Solution:** Try clearing browser cache

### Issue: Lockout timer stuck
- **Solution:** Refresh the page
- **Solution:** Clear localStorage (see unlock instructions above)

## 📞 Support

For technical issues or questions:
- **Email:** Contact Mr. Williams  
- **In-Class:** See Mr. Williams during class time

---

**North Carolina Cyber Academy** | Cybersecurity 1 | 2026
