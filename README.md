# 📚 Exam Tracker - JEE/NEET/BITSAT

This is a comprehensive progress tracker and productivity tool for students preparing for **JEE**, **NEET**, and **BITSAT** . Built as a single-page web application using **Firebase**, it provides features like a Pomodoro timer, task manager, mock test tracker, and streak-based study motivation — all wrapped in a clean and responsive UI.

---

## 🚀 Features

### 🧠 Exam-Specific Tracking
- Supports **JEE**, **NEET**, and **BITSAT** with subject-wise and chapter-wise tracking.
- Custom exam date input and default exam countdown.

### ✅ Daily Tasks
- Add, check off, edit, or delete tasks.
- Tracks task history and boosts streaks with task completion.

### ⏳ Pomodoro Timer
- Preset and customizable timers for Study, Short Break, and Long Break.
- Visual timer with break-mode color changes.
- Tracks sessions and cycles intelligently.

### 📝 Mock Tests Tracker
- Log mock test performance.
- View and manage past test results.
- Encourages weekly test attempts.

### 🔥 Streak & Points System
- Daily streaks and badges based on task activity.
- Points system to gamify study discipline.
- Optional streak freeze (WIP feature).

### 🎯 Progress Analytics
- Subject-wise progress bars.
- Overall exam preparation percentage.

### 👤 Profile Settings
- Select exam type anytime.
- Set custom exam date.
- Save and update preferences.

### 🔐 Firebase Auth + Firestore
- User authentication using Firebase.
- Real-time database for storing user data.
- Admin panel for managing advertisement banners.

---

## 🛠️ Tech Stack

- **Frontend**: HTML, CSS (custom & inline), vanilla JavaScript
- **Auth & Database**: Firebase Auth, Firebase Firestore
- **Hosting**: GitHub Pages or Firebase Hosting

---

## 📸 Screenshots

![image](https://github.com/user-attachments/assets/3c950df2-7369-47ca-aadf-6bd1ba78d34b)
![image](https://github.com/user-attachments/assets/1cf6ff24-7a78-4448-9584-9e7fbab0e5fc)


---

## 🧑‍💻 Admin Panel

Only verified admin users (by email) can:
- Set/edit dynamic advertisement HTML content displayed on the dashboard.

Admin emails are defined in the `ADMIN_EMAILS` array inside the JS.

---

## 🔒 Security

- Firebase rules should be configured to restrict data access to authenticated users only.
- Admin actions (like editing advertisement content) are protected by email-based admin verification.

---
## 🔧 Firebase Setup
- Enable Firestore and Authentication
- Add `users` and `config/advertisement` documents
- Use recommended security rules (see `SECURITY.md`)

--------
## 🧭 Getting Started

1. Clone the repository:
   ```bash
   git clone https://github.com/itsjaataman/preptracker.git
   cd preptracker

----


![GitHub last commit](https://img.shields.io/github/last-commit/itsjaataman/preptracker)
![GitHub issues](https://img.shields.io/github/issues/itsjaataman/preptracker)
