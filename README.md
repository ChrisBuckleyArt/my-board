# Project Tracker — Setup Guide

## What this is
A completely private, customisable kanban-style task board.
No personal information is baked into the code — you name it and set it up on first launch.
Use it for anything: "Christia's WIP", "Ben's Task Board", work projects, etc.

---

## Step 1 — Add your Firebase keys (free, ~8 minutes)
Firebase is Google's free database that syncs your tasks across all your devices.

1. Go to **console.firebase.google.com** and sign in with your Google account
2. Click **"Add project"** → name it `project-tracker` → Continue → disable Analytics → **Create project**
3. In the left sidebar: **Build → Realtime Database → Create Database → US location → Test mode → Enable**
4. Click the ⚙️ gear icon (top left) → **Project settings**
5. Scroll to **"Your apps"** → click the **</>** web icon → name it `project-tracker` → **Register app**
6. Copy the entire `firebaseConfig = { ... }` block shown on screen

7. Open `index.html` in a text editor (right-click → Open With → TextEdit on Mac, Notepad on PC)
8. Find the section that says `REPLACE THIS WITH YOUR FIREBASE CONFIG`
9. Replace the entire `const firebaseConfig = { ... }` block with what you copied
10. Save the file

---

## Step 2 — Upload to GitHub Pages
1. Go to **github.com** → sign in → click **+** → New repository
2. Name it `project-tracker` → Public → Create repository
3. Click **"uploading an existing file"**
4. Open this zip → go INSIDE the `project-tracker-pwa` folder → select ALL 5 files inside
5. Drag them into GitHub → scroll down → **Commit changes**
6. Go to **Settings → Pages → Branch: main → Save**
7. Wait 1-2 minutes → your board is live at `https://YOUR-USERNAME.github.io/project-tracker`

---

## Step 3 — First launch & setup
Open your URL — you'll see a setup screen asking you to:
- Name your board (e.g. "Christia's WIP")
- Pick an accent colour
- Add your categories

This is all stored privately in YOUR Firebase database — nothing is shared with anyone.

---

## Step 4 — Install as an app
**Mac/PC (Chrome):** Open URL → click ⊕ in address bar → Install
**iPhone/iPad (Safari):** Open URL → Share button → "Add to Home Screen" → Add

---

## Step 5 — Use on multiple devices
Just open the same URL on every device — they all sync automatically through Firebase.
No special link or code needed — just the URL.

---

## To create a SECOND board (e.g. Ben's Task Board)
You can reuse the same Firebase project for multiple boards!
Each board gets its own slot in the database based on its name.
Just upload the same files to a different GitHub repository and go through setup again with a different board name.
