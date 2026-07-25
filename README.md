# 📚 Lorebook

A web app for writers to organize their story worlds — characters, bestiary, outline, places and notes, with multi-book support and live sync across devices.

## ✨ Features

- **Multiple books** — after signing in you pick a book from your list; books can be added, renamed or deleted, and each keeps fully separate data
- **Character cards** — name, powers, description and a photo for every character
- **Bestiary** — a catalog of the creatures that inhabit your story world
- **Outline** — chapters with event lists, reordered by drag & drop
- **Places** — locations with notes and a photo gallery
- **Notes** — quick notes with search
- **Recent changes** — an activity log showing what was edited last

## 🔄 Sync and security

- **Sign-in** (Firebase Authentication, email + password) — only the signed-in owner can see their data
- **Live sync** (Firebase Realtime Database) — a change saved on your computer shows up on your phone within seconds, and vice versa
- **Offline mode** — data is also saved locally in the browser, so the app keeps working without internet
- **Database access rules** restrict reads and writes strictly to the owner's account
- Photos are automatically downscaled before saving to conserve storage

## 🛠 Tech stack

| Layer | Technology |
|---|---|
| Frontend | HTML + CSS + vanilla JavaScript (single file, zero frameworks) |
| Authentication | Firebase Authentication |
| Database | Firebase Realtime Database |
| Hosting | GitHub Pages |

The whole app fits in a single `index.html` — no build step, no dependencies to install. The layout is responsive and works well on phones.

## 🚀 Getting started

The app runs at this repository's GitHub Pages URL. Without signing in, only the login screen is visible — all content is private.

To run your own copy:

1. Clone the repository and create a free [Firebase](https://console.firebase.google.com) project (Spark plan).
2. Enable **Authentication** (email/password) and add a user.
3. Create a **Realtime Database** with rules restricting access to `users/$uid`.
4. Paste your `firebaseConfig` into `index.html`.
5. Publish the file on any static hosting (e.g. GitHub Pages).
