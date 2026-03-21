# 🏥 IraqiMed Blueprint
### Iraqi 6th Year Medical Exam Study Planner

> **Designed & Developed by Dr. Ahmed H. Fadl**
> Telegram: [@AH7Hf](https://t.me/AH7Hf)

---

## 📖 About

**IraqiMed Blueprint** is a comprehensive, interactive web-based study planner built specifically for **Iraqi 6th Year Medical Students** preparing for the national comprehensive examination. It covers all four major exam subjects with their official blueprints, helping students track progress, prioritize topics, and generate personalized study plans.

The app runs entirely in a **single HTML file** — no installation, no server setup. Just open it in any browser.

---

## 📚 Subjects Covered

| Subject | Sections | Topics | Exam Questions |
|---------|----------|--------|----------------|
| 🔪 **Surgery** | 19 sections | 100+ topics | 100 Q |
| 💊 **Medicine** | 11 sections | 108 topics | 100 Q |
| 👶 **Pediatrics** | 14 sections | 72 topics | 100 Q |
| 🤱 **Gynecology & Obstetrics** | 13 sections | 65 topics | 100 Q |

All blueprints are based on the official **Iraqi Committee of Colleges of Medicine** exam specifications for 2024–2025.

---

## ✨ Features

### 🔐 User Accounts & Cloud Sync
- **Register / Sign In** with username and password
- All data saved to **Firebase Firestore** (cloud database)
- **Log in from any device** — phone, tablet, or computer
- Progress syncs automatically every 30 seconds
- **Guest mode** available (local storage only)
- Change password from the user menu

### 📊 Dashboard
- **Overall exam readiness** percentage with animated progress bar
- **Live countdown timer** to your exam date (days, hours, minutes, seconds)
- **4 stat cards**: completed topics, high-priority remaining, topics/day needed, days left
- **Section-by-section progress bars** for all subjects

### 📋 Topics Panel
- All exam topics organized by section with **exam weight %**
- **✅ Checkbox** to mark topics as completed (with animated count badge)
- **Priority system**: tag topics as 🔴 High / 🟡 Medium / 🟢 Low priority
- **Mark all section complete** button (one tap to check/uncheck an entire section)
- **Search** topics by name
- **Filter** by: All / Incomplete / Completed / High / Medium / Low priority
- **Sort sections** by exam percentage: High→Low or Low→High
- **Collapse / Expand all** sections with one button
- **➕ Create custom sections** with your own topics (edit & delete supported)
- Topics count badge per section (e.g. ✅ 3 / 18)

### 📅 Study Planner
- **Smart plan generator** distributes topics across your available days
- **Duration options**: Auto (uses exam date) or Custom (slider 1–90 days, presets)
- **Priority modes**:
  - 📊 Exam Weight — highest exam % sections first
  - ⭐ My Priority — your starred topics first
  - 🔀 Combined — blends both factors
- **Include filter**: Remaining only / All topics / High-priority only
- **✨ Suggest Plan** — shows recommended topics/day before generating
- **💾 Save plans** — up to 10 saved plans per subject per account
- **📂 Load saved plans** with one tap
- **📤 Export plan as JSON** file
- **📥 Import plan from JSON** file
- **🖨 Print / PDF** — clean print layout hides all UI
- **🕐 Auto-restore last plan** — reopens without needing to regenerate

### 🎯 Insights Dashboard
- Key stats: completed, remaining, high-priority count, days left, daily workload
- High-priority unfinished topics list
- Full section breakdown with progress bars
- Reset progress button (per subject)
- Export data as JSON

### 🎨 UI & Experience
- **Dark / Light mode** toggle (saved across sessions)
- **Motivational quotes** on every session
- **🎉 Confetti** animation at 25%, 50%, 75%, and 100% completion
- Fully **responsive** — works on mobile and desktop
- **Mobile-optimized** touch interactions (no tap delays)
- Smooth animations throughout

---

## 🚀 How to Use

### 1. Open the App
Visit the GitHub Pages URL or open `IraqiMed_Blueprint.html` directly in any browser.

### 2. Create an Account
- Click **Register**
- Enter your full name, username (letters/numbers/underscore), and password (min 4 characters)
- Click **Create Account →**

### 3. Choose Your Subject
After logging in, tap any of the 4 subject cards:
- Your progress for each subject is tracked separately
- Switch between subjects anytime using the **⇄ Change Subject** button

### 4. Track Your Topics
- Go to the **📋 Topics** tab
- Tap any topic row to **check it as completed** ✅
- Tap the **⚪ Priority** button to cycle through 🔴 High → 🟡 Med → 🟢 Low
- Use **Mark all as completed** at the bottom of each section for bulk actions

### 5. Set Your Exam Date
- On the **📊 Dashboard**, enter your exam date
- The countdown timer will start immediately
- This is used by the planner to calculate topics/day

### 6. Generate a Study Plan
- Go to the **📅 Study Plan** tab
- Choose your duration (auto or custom)
- Select priority mode
- Click **⚡ Generate Plan**
- Save or export the plan as needed

### 7. Monitor Progress
- Check the **🎯 Insights** tab for a full breakdown
- Watch your overall % grow on the dashboard as you check off topics

---

## 📱 Install as App (Mobile)

The app can be used as a shortcut on your phone's home screen:

**iPhone (Safari):**
1. Open the app URL in Safari
2. Tap the Share button → **Add to Home Screen**

**Android (Chrome):**
1. Open the app URL in Chrome
2. Tap the 3-dot menu → **Add to Home Screen**

---

## 🔧 Setup (For Developers / Self-Hosting)

### Deploy to GitHub Pages
1. Fork or clone this repository
2. Go to **Settings → Pages**
3. Set source to `main` branch, root folder
4. Your app will be live at `https://yourusername.github.io/repo-name/`

### Firebase Configuration
The app uses Firebase Firestore for cloud user storage. The config is already embedded. If you want to use your own Firebase project:

1. Go to [Firebase Console](https://console.firebase.google.com)
2. Create a new project
3. Enable **Firestore Database** (test mode)
4. Get your web app config from **Project Settings → Your Apps**
5. Replace the `FIREBASE_CONFIG` object in the HTML file
6. Set Firestore security rules:

```
rules_version = '2';
service cloud.firestore {
  match /databases/{database}/documents {
    match /surgeonprep_users/{userId} {
      allow read, write: if true;
    }
  }
}
```

---

## 📁 File Structure

```
IraqiMed_Blueprint.html   ← Single file, entire app
README.md                  ← This file
```

Everything is self-contained in one HTML file — CSS, JavaScript, and all blueprint data.

---

## 🏗 Tech Stack

| Technology | Purpose |
|-----------|---------|
| HTML5 / CSS3 | Structure & styling |
| Vanilla JavaScript | All logic, no frameworks |
| Firebase Firestore | Cloud user storage |
| Google Fonts (Syne + DM Sans) | Typography |
| localStorage | Session & offline backup |

---

## 📋 Blueprint Sources

| Subject | Source |
|---------|--------|
| Surgery | Iraqi Comprehensive Exam Blueprint — General Surgery & Branches |
| Medicine | Committee of Colleges of Medicine in Iraq — 6th Year Assessment 2024–2025 |
| Pediatrics | Iraqi Comprehensive Exam for 6th Year Medical Students — Pediatrics |
| Gynecology & Obstetrics | Iraqi Comprehensive Exam — OB/GYN Blueprint (50+50) |

---

## 🙏 Acknowledgements

This application was built to help Iraqi medical students study more effectively and systematically. Special thanks to all students who provided feedback during development.

---

## ⚠️ Disclaimer

This application is a **study aid tool** based on publicly available exam blueprints. It is not affiliated with or endorsed by the Committee of Colleges of Medicine in Iraq. Always refer to official sources for the most current examination guidelines.

---

## © Copyright

```
IraqiMed Blueprint
Copyright © 2025 Dr. Ahmed H. Fadl
All rights reserved.

Telegram: @AH7Hf
```

This project is provided for **educational purposes** for Iraqi medical students. Redistribution or commercial use without explicit permission from the author is prohibited.

---

<div align="center">

**Made with ❤️ for Iraqi Medical Students**

*Dr. Ahmed H. Fadl | [@AH7Hf](https://t.me/AH7Hf)*

</div>
