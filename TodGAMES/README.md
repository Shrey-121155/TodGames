# Tiny Explorers 🌞

A simple, ad-free, offline-friendly learning app for toddlers (ages 2-4).
Four activities: Animals, Counting, Colors, Shapes — all original content
(emoji + CSS shapes + voice narration), so there's nothing to license and
nothing that can break from a copyright claim.

## What's in this folder
- `index.html` — the entire app (HTML + CSS + JS in one file)
- `manifest.json` — lets parents "Add to Home Screen" so it feels like a real app
- `sw.js` — service worker, makes it work fully offline after the first load
- `icon-192.png` / `icon-512.png` — the app icon

## How to publish it on Replit (takes ~3 minutes)
1. Go to replit.com and create a new Repl → choose the **HTML/CSS/JS** template
2. Delete the placeholder files Replit creates
3. Upload all 5 files from this folder into the Repl (drag and drop works)
4. Click **Run** — Replit will give you a live `.replit.app` URL
5. Open that URL on a phone browser → tap the share/menu icon → **"Add to Home Screen"**
   - On Android (Chrome): ⋮ menu → "Add to Home screen"
   - On iPhone (Safari): Share icon → "Add to Home Screen"
6. It'll now sit on the home screen with its own icon, open full-screen, no browser bar — feels like a native app, and works offline.

## How to customize it
Everything lives in `index.html`. A few easy edits:

**Change the app name:** search for `Tiny Explorers` (appears in the `<title>`,
the `<h1>`, and `manifest.json`) and replace it.

**Add more animals/colors/shapes:** find the `DATA` object near the top of
the `<script>` tag — each activity is just a JavaScript array. Add a new
`{emoji:'🐰', name:'Rabbit', sound:'Squeak'}` line to add a rabbit, for example.

**Add a 5th activity:** copy the pattern of one existing bubble (HTML) +
one `DATA` entry + one `reactX()` function — it's the same shape every time.

## Why no real videos?
We looked at this — most "free nursery rhyme videos" floating around the
internet (including ones marked "public domain" on archive.org) are actually
still-copyrighted commercial content (CoCoMelon, PBS Kids, etc.) that got
mislabeled by whoever uploaded them. Using them would put the app at real
takedown/copyright risk. Everything here is built from scratch — emoji,
CSS shapes, and the browser's built-in speech voice — so it's 100% yours
and 100% safe to publish.

If you later want real narrated videos, the cleanest path is recording your
own simple clips and dropping them into the app — happy to help wire that up
when you're ready.

## A note before going live for real users
This is a fun, legit MVP — but apps aimed at kids under 13 are tightly
regulated (COPPA in the US, Google Play Families policy, Apple's Kids
Category). Since this version collects zero data, shows no ads, and has
no accounts, you're in a pretty safe spot. If you ever add analytics, ads,
or user accounts down the line, that's the point to look into those rules
properly — happy to help when you get there.
