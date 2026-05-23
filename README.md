# World Environment Day 2026 - Digital Pledge System

![WED 2026](https://img.shields.io/badge/WED-2026-green)
![Status](https://img.shields.io/badge/status-ready-brightgreen)
![Cost](https://img.shields.io/badge/cost-FREE-blue)
![License](https://img.shields.io/badge/license-Open%20Source-orange)

> A beautiful, mobile-responsive pledge page with live counter and Google Sheets integration for the World Environment Day 2026 campaign in Nigeria.

---

## 📋 Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Demo](#demo)
- [Quick Start](#quick-start)
- [Installation](#installation)
- [Configuration](#configuration)
- [Deployment](#deployment)
- [Usage](#usage)
- [Customization](#customization)
- [Troubleshooting](#troubleshooting)
- [FAQ](#faq)
- [Support](#support)
- [Contributors](#contributors)
- [License](#license)

---

## 🌍 Overview

The WED 2026 Digital Pledge System is a complete web application designed for the "Clean Cities, Resilient Future" campaign - a partnership between Nestlé Nigeria, National Plastic Action Partnership (NPAP), African Clean Up Initiative (ACI), the Policy Innovation Centre, Federal Ministry of Environment, FBRA, CEIP, NESREA , AEPB, RAN, SONNEX, ALEF, Swiss Consulate, Kingdom of Netherlands , Waste Africa and Office of SA to Lagos on Circular Economy and Cimate Change.

**Campaign Goal:** Mobilize 10,000+ Nigerians to pledge commitment to waste sorting, littering prevention, and environmental sustainability during the June 3-9, 2026 community cleanup week.

---

## ✨ Features

### 🎨 User Interface
- ✅ Beautiful, modern design with campaign colors (green/blue gradient)
- ✅ Fully mobile-responsive (perfect on phones, tablets, desktops)
- ✅ Animated live pledge counter
- ✅ Smooth form validation with clear error messages
- ✅ Success celebration screen after pledge submission
- ✅ One-click social sharing (WhatsApp, Facebook, Twitter)

### 📊 Data Collection
- ✅ Comprehensive pledge form with:
  - Personal information (name, email, phone, location)
  - 4 core pledge commitments (checkboxes)
  - Additional commitments (volunteer, champion, tips)
  - Consent and privacy options
- ✅ Real-time data sync to Google Sheets
- ✅ Timestamp on every submission
- ✅ Export to Excel/CSV anytime

### 🔧 Technical Features
- ✅ Google Apps Script backend (serverless)
- ✅ No database required - uses Google Sheets
- ✅ HTTPS encryption (automatic on Netlify)
- ✅ Email confirmations (optional)
- ✅ Live counter updates
- ✅ Cross-browser compatible
- ✅ Lightweight (loads in <2 seconds)

### 💰 Cost
- ✅ **100% FREE** - No monthly fees ever
- ✅ Unlimited pledges
- ✅ Free hosting on Netlify
- ✅ Free Google Sheets storage
- ✅ Free SSL certificate

---

## 🎬 Demo

**Live Demo:** [https://wed2026pledge.netlify.app](https://wed2026pledge.netlify.app) *(example URL)*

### Screenshots

**Desktop View:**
```
┌─────────────────────────────────────────┐
│  🌍♻️🇳🇬                                 │
│  CLEAN CITIES, RESILIENT FUTURE        │
│  Take the Pledge for Sustainable 🇳🇬    │
├─────────────────────────────────────────┤
│  Nigerians Who Have Taken the Pledge   │
│           5,247                         │
│         and counting! 💚                │
├─────────────────────────────────────────┤
│  "I PLEDGE: I promise to sort my       │
│   waste, stop littering, and keep my   │
│   community clean..."                   │
├─────────────────────────────────────────┤
│  [Pledge Form]                          │
└─────────────────────────────────────────┘
```

---

## 🚀 Quick Start

### Prerequisites

Before you begin, you need:
- ✅ Google Account (free)
- ✅ Web browser (Chrome, Firefox, Safari, Edge)
- ✅ Text editor (VS Code, Notepad, TextEdit)
- ✅ 30 minutes of time

### Installation Summary

```bash
1. Create Google Sheet
2. Add Apps Script code
3. Deploy as Web App
4. Configure index.html
5. Deploy to Netlify
6. Create short link (bit.ly)
7. Generate QR code
```

**Total Setup Time:** 30 minutes  
**Technical Skill Required:** Beginner  
**Ongoing Maintenance:** 5 minutes/day

---

## 📥 Installation

### Step 1: Download Files

This package includes 3 files:

1. **index.html** - Main pledge page
2. **google-apps-script.js** - Backend code
3. **DEPLOYMENT_INSTRUCTIONS.md** - Detailed setup guide

Download all files to your computer.

### Step 2: Setup Google Sheets Backend

#### 2.1 Create Google Sheet

1. Go to [sheets.google.com](https://sheets.google.com)
2. Click **"+ Blank spreadsheet"**
3. Name it: **"WED 2026 Pledges"**
4. Copy the Sheet ID from the URL:
   ```
   https://docs.google.com/spreadsheets/d/[SHEET_ID]/edit
   ```
   Example: `1a2b3c4d5e6f7g8h9i0j`

#### 2.2 Add Apps Script

1. In your Google Sheet: **Extensions** → **Apps Script**
2. Delete default code
3. Copy all code from `google-apps-script.js`
4. Paste into Apps Script editor
5. Click **Save** 💾
6. Name project: **"WED 2026 Pledge Backend"**

#### 2.3 Deploy Web App

1. Click **Deploy** → **New deployment**
2. Select type: **Web app**
3. Settings:
   - Description: "WED 2026 Pledge Handler"
   - Execute as: **Me**
   - Who has access: **Anyone**
4. Click **Deploy**
5. **Authorize access:**
   - Click "Review permissions"
   - Choose your account
   - Click "Advanced" → "Go to [project] (unsafe)"
   - Click "Allow"
6. **Copy the Web App URL:**
   ```
   https://script.google.com/macros/s/AKfycby.../exec
   ```
7. **Save this URL** - you need it next!

---

## ⚙️ Configuration

### Configure index.html

1. Open `index.html` in text editor
2. Press **Ctrl + F** (or **Cmd + F** on Mac)
3. Search for: `CONFIG`
4. Update this section:

```javascript
const CONFIG = {
    GOOGLE_SCRIPT_URL: 'YOUR_GOOGLE_APPS_SCRIPT_URL_HERE',
    SHEET_ID: 'YOUR_GOOGLE_SHEET_ID_HERE',
    PAGE_URL: window.location.href
};
```

**Replace with your actual values:**

```javascript
const CONFIG = {
    GOOGLE_SCRIPT_URL: 'https://script.google.com/macros/s/AKfycby.../exec',
    SHEET_ID: '1a2b3c4d5e6f7g8h9i0j',
    PAGE_URL: window.location.href
};
```

5. **Save the file** (Ctrl + S or Cmd + S)

---

## 🌐 Deployment

### Deploy to Netlify

#### Option A: Drag & Drop (Easiest)

1. Go to [app.netlify.com/drop](https://app.netlify.com/drop)
2. Drag `index.html` onto the page
3. Wait 10 seconds
4. Your site is live! 🎉
5. Copy the URL: `https://random-name-123.netlify.app`

#### Option B: GitHub + Netlify (Best for Updates)

**Create GitHub Repository:**

1. Go to [github.com](https://github.com) and sign in
2. Click **"New repository"**
3. Name: `wed-2026-pledge`
4. Make it **Public**
5. Click **"Create repository"**
6. Upload `index.html`

**Deploy to Netlify:**

1. Go to [netlify.com](https://netlify.com) and sign up
2. Click **"Add new site"** → **"Import project"**
3. Choose **GitHub**
4. Select `wed-2026-pledge` repository
5. Click **"Deploy"**
6. Your site is live in 30 seconds!

#### Customize URL

1. In Netlify dashboard: **Site settings**
2. Click **"Change site name"**
3. Enter: `wed2026pledge`
4. Final URL: `https://wed2026pledge.netlify.app` ✅

---

## 🔗 Create Short Link

### Using Bitly (Recommended)

1. Go to [bitly.com](https://bitly.com)
2. Sign up (free)
3. Click **"Create"** → **"Link"**
4. Paste your Netlify URL
5. Custom back-half: `WED2026Pledge`
6. Click **"Create"**
7. Your short link: **bit.ly/WED2026Pledge** 🎯

### Using TinyURL (No Signup)

1. Go to [tinyurl.com](https://tinyurl.com)
2. Paste your Netlify URL
3. Custom alias: `WED2026Pledge`
4. Click **"Make TinyURL!"**
5. Your link: **tinyurl.com/WED2026Pledge**

---

## 📱 Generate QR Code

1. Go to [qr-code-generator.com](https://www.qr-code-generator.com)
2. Select **"URL"**
3. Enter: `bit.ly/WED2026Pledge`
4. Customize:
   - Add logo (optional)
   - Change color to green (#00AA44)
5. Click **"Create QR Code"**
6. Download as **PNG** (high resolution)
7. Use on all print materials! 📱

---

## 📖 Usage

### For Campaign Organizers

**Before Launch:**
- Test form with sample data
- Verify data appears in Google Sheet
- Test on mobile devices
- Share with team for feedback

**During Campaign:**
- Monitor pledge count daily
- Share milestones on social media
- Respond to technical issues
- Download backup data weekly

**After Campaign:**
- Download final pledge list
- Generate statistics report
- Thank all pledgers
- Follow up with volunteers

### For Users

**Taking the Pledge:**

1. Visit: `bit.ly/WED2026Pledge`
2. Fill out the form:
   - Enter your name and contact info
   - Select your state
   - Check all 4 pledge commitments
   - Optionally sign up to volunteer/champion
   - Consent to updates
3. Click **"SIGN THE PLEDGE"**
4. See success message
5. Share with friends!

**Sharing the Pledge:**

Use the share buttons:
- 📱 WhatsApp
- 👍 Facebook
- 🐦 Twitter
- 🔗 Copy Link

---

## 🎨 Customization

### Change Colors

Find and replace in `index.html`:

```css
#00AA44  →  Your brand green
#0066CC  →  Your brand blue
#CC3300  →  Your brand red
```

### Add Logo

After line 139 in `index.html`, add:

```html
<img src="YOUR_LOGO_URL" alt="Campaign Logo" style="width: 200px; margin-bottom: 20px;">
```

### Change Text

All text is editable in `index.html`:
- Pledge statement (line ~164)
- Form labels (lines ~200-350)
- Success message (lines ~430-440)
- Footer text (lines ~650-670)

### Add/Remove Form Fields

To add a field:

```html
<div class="form-group">
    <label for="newField">New Field Label</label>
    <input type="text" id="newField" name="newField">
</div>
```

Remember to also update:
1. Google Apps Script to save the new field
2. JavaScript validation (if required)

---

## 📊 Viewing Pledge Data

### Real-Time Dashboard

1. Open your Google Sheet
2. See all pledges in real-time
3. Columns include:
   - Timestamp
   - Name & Contact Info
   - Location (State, Community)
   - All Pledge Commitments
   - Volunteer/Champion Status
   - Consent Information

### Download Data

**Excel Format:**
- **File** → **Download** → **Microsoft Excel (.xlsx)**

**CSV Format:**
- **File** → **Download** → **Comma Separated Values (.csv)**

### View Statistics

**Total Pledges:**
- Check row count at bottom of sheet (minus header)

**By State:**
1. Click **Data** → **Pivot table**
2. Rows: State
3. Values: COUNTA of State

**Volunteers/Champions:**
1. Click **Data** → **Create a filter**
2. Filter by "Yes" in respective columns

---

## 🔧 Troubleshooting

### Form Not Submitting

**Problem:** Click submit, nothing happens

**Solutions:**
1. Check browser console (F12) for errors
2. Verify Google Apps Script URL is correct in CONFIG
3. Ensure Google Apps Script is deployed with "Anyone" access
4. Clear browser cache and try again

### Counter Shows 0 or ---

**Problem:** Live counter not updating

**Solutions:**
1. Refresh the page
2. Check Google Sheet has data
3. Verify Sheet ID is correct in CONFIG
4. Wait 10 seconds - counter updates on page load

### Email Confirmations Not Sending

**Problem:** Pledgers not receiving emails

**Solutions:**
1. Check spam/junk folder
2. Verify email function is enabled in Google Apps Script
3. Gmail has limit of 500 emails/day
4. Check Apps Script execution logs

### Page Not Loading on Netlify

**Problem:** Netlify URL shows error

**Solutions:**
1. Ensure file is named exactly `index.html` (lowercase)
2. Check Netlify deploy logs for errors
3. Verify file uploaded successfully
4. Try re-deploying

### Google Authorization Error

**Problem:** "Google hasn't verified this app" warning

**Solution:**
1. Click "Advanced"
2. Click "Go to [project name] (unsafe)"
3. This is YOUR script - it's safe
4. Click "Allow"

---

## ❓ FAQ

### Q: How much does this cost?
**A:** ₦0 - Completely FREE. No monthly fees ever.

### Q: How many pledges can I collect?
**A:** Unlimited! Google Sheets supports 10 million cells.

### Q: Can I use my own domain?
**A:** Yes! Connect a custom domain in Netlify settings (requires domain ownership).

### Q: Is the data secure?
**A:** Yes. Data is stored in YOUR Google account, HTTPS encrypted, no third-party access.

### Q: Can I customize the design?
**A:** Yes! All HTML/CSS is editable. Change colors, text, layout, etc.

### Q: What happens after June 9, 2026?
**A:** The page stays live forever (unless you delete it). You own all the data.

### Q: Can I see who pledged?
**A:** Yes, all pledge data is in your Google Sheet with names, emails, etc.

### Q: Can I export the pledge list?
**A:** Yes, download as Excel or CSV anytime from Google Sheets.

### Q: Does it work on mobile?
**A:** Yes! Fully responsive design optimized for phones and tablets.

### Q: Can I edit pledges after submission?
**A:** Admin can edit in Google Sheet. Users cannot edit after submitting.

---

## 📞 Support

### Contact

- **Email:** info.acinigeria@gmail.com
- **Phone:** 08033340972
- **Campaign:** World Environment Day 2026

### Resources

- **Setup Guide:** DEPLOYMENT_INSTRUCTIONS.md
- **Google Sheets:** [sheets.google.com](https://sheets.google.com)
- **Netlify Docs:** [docs.netlify.com](https://docs.netlify.com)
- **Apps Script Docs:** [developers.google.com/apps-script](https://developers.google.com/apps-script)

### Reporting Issues

Found a bug? Have a suggestion?

1. Check the Troubleshooting section
2. Review DEPLOYMENT_INSTRUCTIONS.md
3. Contact support email above

---

## 👥 Contributors

**Campaign Partners:**
- **Nestlé Nigeria** - Corporate sponsor
- **National Plastic Action Partnership (NPAP)** - Policy partner
- **African Clean Up Initiative (ACI)** - Implementation partner

**Technical Development:**
- Pledge system design and development
- Campaign materials and strategy
- SBCC framework integration

---

## 📜 License

This project is open source and available for use by environmental campaigns, NGOs, and community organizations.

**You are free to:**
- ✅ Use this system for your own campaigns
- ✅ Modify the design and content
- ✅ Share with other organizations
- ✅ Adapt for different causes

**Attribution:**
Please credit: "World Environment Day 2026 - Nigeria Campaign"

---

## 🎯 Campaign Goals

**Target Metrics (June 30, 2026):**
- 10,000+ pledges signed
- 40% household waste sorting adoption
- 60% awareness of 3 R's (Reduce, Reuse, Recycle)
- 5,000+ participants in June 5 cleanup events
- 200+ trained community champions
- 8 states reached

**Campaign Period:**
- **Launch:** May 28, 2026
- **Peak:** June 3-9, 2026 (Community Cleanup Week)
- **Conclusion:** June 30, 2026

---

## 📈 Success Metrics

**Pledge System Performance:**
- Page views: Track with Google Analytics
- Pledges collected: Real-time in Google Sheets
- Share rate: Monitor social media engagement
- Volunteer sign-ups: Filter in Google Sheets
- State distribution: Pivot table analysis

**Campaign Impact:**
- Waste sorting behavior change surveys
- Community cleanup participation
- Social media reach and engagement
- Media coverage and partnerships
- Long-term behavior maintenance

---

## 🔄 Updates & Maintenance

**Regular Checks:**
- Daily: Monitor pledge count and respond to issues
- Weekly: Download data backup
- Monthly: Review analytics and adjust strategy

**After Campaign:**
- Keep page live for ongoing pledges
- Use data for impact reporting
- Share success stories
- Plan follow-up initiatives

---

## 🌟 Acknowledgments

Special thanks to:
- All Nigerians who take the pledge
- Volunteers and community champions
- Campaign partners and sponsors
- Technical contributors

---

## 🇳🇬 Together, We Build a Sustainable Nigeria!

**Hashtags:**
#SortItForTheCity  
#CleanResilientCitiesNG  
#WED2026Nigeria  
#nestlingcares  
#partnershipsfortheenvironment

---

**Last Updated:** May 23, 2026  
**Version:** 1.0.0  
**Status:** Ready for Deployment ✅

---

**Questions? Need Help?**  
📧 info.acinigeria@gmail.com  
📱 08033340972  

**Let's make Nigeria cleaner, greener, and more resilient together!** 🌍♻️💚
