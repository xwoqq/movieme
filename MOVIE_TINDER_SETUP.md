# Movie Tinder App - Setup Guide

## 🎯 Overview
A Tinder-like app for you and your girlfriend to decide on movies together!

## 📁 Files
- `movie-tinder-admin.html` - Your admin panel (add movies, see responses)
- `movie-tinder-swiper.html` - Her swiper interface (swipe movies)

## 🚀 Quick Start (Simple Version - Using localStorage)

### Current Setup (Works Locally)
Right now, the app uses **localStorage** which means:
- ✅ Works immediately, no setup needed
- ❌ Data is stored locally on each device
- ❌ Not synced in real-time

**To use it:**
1. Open `movie-tinder-admin.html` in your browser
2. Add movies
3. Open `movie-tinder-swiper.html` in the same browser (or copy the data)
4. She swipes movies
5. Refresh admin page to see her responses

### Limitations:
- Both need to use the same browser/device OR
- You need to manually copy the data between devices

---

## 🔥 Option 1: Firebase Setup (Recommended for Real-Time Sync)

### Step 1: Create Firebase Project
1. Go to https://console.firebase.google.com
2. Click "Add project"
3. Name it (e.g., "movie-tinder")
4. Disable Google Analytics (optional)
5. Click "Create project"

### Step 2: Enable Firestore
1. In Firebase Console, click "Firestore Database"
2. Click "Create database"
3. Start in "Test mode" (for now)
4. Choose a location
5. Click "Enable"

### Step 3: Get Your Config
1. Click the gear icon ⚙️ → "Project settings"
2. Scroll to "Your apps"
3. Click the web icon `</>`
4. Register app (name it "Movie Tinder")
5. Copy the `firebaseConfig` object

### Step 4: Add Firebase to HTML Files
1. Add this before `</head>` in both HTML files:
```html
<script src="https://www.gstatic.com/firebasejs/10.7.1/firebase-app-compat.js"></script>
<script src="https://www.gstatic.com/firebasejs/10.7.1/firebase-firestore-compat.js"></script>
```

2. Replace the `firebaseConfig` in both files with your actual config

3. Replace localStorage code with Firebase code (I can help with this!)

---

## 🌐 Option 2: Host on GitHub Pages (Simple Sharing)

### Setup:
1. Create a GitHub repository
2. Upload both HTML files
3. Enable GitHub Pages
4. Share the URLs:
   - `https://yourusername.github.io/repo/movie-tinder-admin.html`
   - `https://yourusername.github.io/repo/movie-tinder-swiper.html`

### Still needs:
- A way to sync data (Firebase or backend API)

---

## 🖥️ Option 3: Simple Backend API

Create a simple Node.js/Express server:
- Store movies in a JSON file
- Both apps poll the server every few seconds
- Simple but requires hosting

---

## 💡 Recommended Approach

**For best experience:**
1. Use **Firebase Firestore** for real-time sync
2. Host on **GitHub Pages** or **Netlify** for easy sharing
3. Both of you access the same URLs
4. Real-time updates without refreshing!

---

## 🎨 Features

### Admin Panel (You):
- ✅ Add movies
- ✅ See which movies she liked/passed
- ✅ View statistics
- ✅ Share link with her

### Swiper Interface (Her):
- ✅ Swipe right (like) or left (pass)
- ✅ Drag cards or use buttons
- ✅ Keyboard shortcuts (arrow keys)
- ✅ See progress

---

## 🔧 Next Steps

1. **Test locally first** - Make sure everything works
2. **Choose sync method** - Firebase recommended
3. **Host the files** - GitHub Pages or Netlify
4. **Share the links** - Both of you use the same URLs

---

## 📝 Notes

- Movies are stored with status: `pending`, `liked`, or `passed`
- You can add your own likes later to find matches
- The app works offline (with localStorage)
- Real-time sync requires Firebase or backend

---

Need help setting up Firebase? Let me know!
