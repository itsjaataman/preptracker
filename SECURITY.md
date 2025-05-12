# 🔐 Security Policy

## Supported Versions

We aim to support the latest stable version of the project. Please ensure you're using the most recent version before reporting issues.


**DO NOT** open a public issue to report a security flaw — doing so risks exposing others before a fix is ready.

---

## 🔒 Firebase Security Rules

We strongly recommend:

- Restricting access to authenticated users.
- Using Firestore rules like:

```js
rules_version = '2';
service cloud.firestore {
  match /databases/{database}/documents {
    match /users/{userId} {
      allow read, write: if request.auth != null && request.auth.uid == userId;
    }
    match /config/{docId} {
      allow read: if true;
      allow write: if request.auth != null && request.auth.token.email in [
        'ADMIN_EMAIL_1', 'ADMIN_EMAIL_2'
      ];
    }
  }
}
