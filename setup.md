
Welcome to the official setup guide for **Prep Tracker**, a smart exam preparation tracker tailored for students targeting **JEE**, **NEET**, and **BITSAT**. This guide will walk you through everything needed to get the app running with Firebase and host it using GitHub Pages.

---

## 📦 Files in the Project

* `index.html` → Student Portal (dashboard, pomodoro, progress)
* `admin.html`  → Admin Panel (exam config, student progress)

---

## 🔧 Step 1: Firebase Setup

1. Go to [Firebase Console](https://console.firebase.google.com/) and click **"Add Project"**.
2. Once created:

   * Enable **Authentication** → **Sign-in method** → Enable **Email/Password** or **Google**.
   * Enable **Firestore Database** → Start in **production mode**.
3. Go to **Project Settings → General**.

   * Under **"Your Apps"**, click **\</> (Web app)**.
   * Register the app name and copy the **Firebase config**:

js
const firebaseConfig = {
  apiKey: "YOUR_API_KEY",
  authDomain: "your-project.firebaseapp.com",
  projectId: "your-project",
  storageBucket: "your-project.appspot.com",
  messagingSenderId: "XXXXXXXXXXXX",
  appId: "1:XXXXXXXXXXXX:web:XXXXXXXXXXXXXX"
};

------

🔁 Update Firebase Config in HTML Files
✅ You must replace the Firebase config block in both files:
index.html
admin.html 

In both files, look for the section like:
const firebaseConfig = {
  apiKey: "AIzaSy...",
  authDomain: "...",
  ...
};


And replace it with your actual Firebase config copied in Step 1.

⚠️ Both files must use the same Firebase project config, otherwise login and database access won't work correctly.

------
🔐  Set Admin Access
In admin.html, locate the following line near the top of the script:

js
Copy
Edit
const ADMIN_EMAILS = ['admin@example.com'];
Replace it with your actual email (the one you use to sign in to Firebase):

js
Copy
Edit
const ADMIN_EMAILS = ['youremail@gmail.com'];
✅ Only emails listed in ADMIN_EMAILS can access the Admin Panel. Others will be blocked


