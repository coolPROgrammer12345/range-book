# Range Book

A browser-based golf practice tracker built as a single-file HTML app. No build step — open it and go. Accounts and session data are backed by Supabase, so your history syncs across devices.

## Usage

Open `range-book.html` in any modern browser (or visit the live GitHub Pages URL). Create an account (email + password) or log in — your sessions are tied to your account and follow you across devices.

1. Sign up or log in from the welcome screen.
2. Pick a section from the home screen: **Putting**, **Chipping**, or **Driver**.
3. Tap a drill to expand it and see the goal for your skill tier (Beginner / Intermediate / Advanced).
4. Tap **Log This Session**, enter your attempts and makes, add optional notes, and save.
5. Check the **History** tab for your stats: total sessions, sessions this week, day streak, and weekly practice balance.
6. Tap **Share Your Stats** on the History tab to share or copy a quick summary.
7. Use the **Nearby** tab to find golf courses and driving ranges within 25 miles, either from your current location or a city/zip you type in.
8. Check the **Points** tab for your point total and how points are earned.
9. Use the **Credits** tab to log out.

## Features

- **Accounts** — sign up or log in with email and password; your data follows you across devices
- **Putting, Chipping, and Driver** practice sections, 9 drills each
- Each drill has **Beginner / Intermediate / Advanced** goal tiers
- **Session logging** — attempts, makes, and notes per session
- **Goal-hit badges** — sessions that meet their tier's goal get a ✓ badge, both right after saving and in History
- **Weekly balance** — see how many sessions you've logged per category this week
- **Share Your Stats** — export a short text summary via the native share sheet or clipboard
- **History tab** with total sessions, sessions this week, and day streak
- **Points** — earn 100 points per 10 makes logged in a session (capped at 50 makes/session). Only one point-earning session counts every 90 seconds, so points can't be farmed by spamming fake sessions
- **Nearby tab** — finds golf courses and driving ranges within 25 miles using OpenStreetMap/Overpass data, with an embedded map and one-tap directions

## Data & Privacy

Session data is stored in a Supabase (hosted Postgres) database, tied to your account. Row-level security policies restrict every row to its owner — no other user or anonymous visitor can read or write your sessions. Data persists across devices and browsers as long as you're logged into the same account; logging out doesn't delete anything, it just stops loading it locally. The Nearby tab sends your location (or the city/zip you enter) to OpenStreetMap/Nominatim and Google Maps solely to look up and display nearby courses.
