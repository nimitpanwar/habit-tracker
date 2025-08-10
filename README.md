# Habit Tracker

A beautiful, minimal habit tracker with GitHub-style contribution heatmaps. Track your daily habits and visualize your progress with an elegant, compact interface.

<img width="2870" height="1774" alt="Screenshot 2025-08-10 at 9 06 19 PM" src="https://github.com/user-attachments/assets/e9b6231d-a82a-4b8c-a7a5-d1377ba84929" />

## ✨ Features

- **GitHub-style heatmap** - Visual progress tracking with intensity levels
- **Minimal design** - Clean, compact interface focused on your data
- **Real-time sync** - Data synced across devices using Firebase
- **Click to edit** - Simple click-to-edit entries on any date
- **Year navigation** - Browse your habit history across years
- **Smart stats** - Total, daily average, streaks, and more

## 🚀 Setup

1. **Download** the HTML file
2. **Create a Firebase project** at [firebase.google.com](https://firebase.google.com)
3. **Enable Firestore** in your Firebase console
4. **Update Firebase config** in the HTML file:

```javascript
const firebaseConfig = {
    apiKey: "your-api-key",
    authDomain: "your-project.firebaseapp.com",
    projectId: "your-project-id",
    storageBucket: "your-project.appspot.com",
    messagingSenderId: "123456789",
    appId: "your-app-id"
};
```

5. **Set Firestore rules** to allow authenticated users:

```javascript
rules_version = '2';
service cloud.firestore {
  match /databases/{database}/documents {
    match /{document=**} {
      allow read, write: if request.auth != null;
    }
  }
}
```

6. **Open** the HTML file in your browser

## 💡 How to Use

- Click **"New Habit"** to create a habit
- Click any **day square** in the heatmap to edit that day's value
- Use **year arrows** to navigate through different years
- **Delete habits** using the trash icon

That's it! Start building better habits today. 🎯
