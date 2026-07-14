# Range Book

A browser-based golf practice tracker built as a single-file HTML app. No build step, no backend — open it and go.

## Usage

Open `range-book.html` in any modern browser (or visit the live GitHub Pages URL once enabled). No install, sign-up, or internet connection required for practice logging.

1. Pick a section from the home screen: **Putting**, **Chipping**, or **Driver**.
2. Tap a drill to expand it and see the goal for your skill tier (Beginner / Intermediate / Advanced).
3. Tap **Log This Session**, enter your attempts and makes, add optional notes, and save.
4. Check the **History** tab for your stats: total sessions, sessions this week, and your day streak.
5. Use the **Nearby** tab to find golf courses and driving ranges within 25 miles, either from your current location or a city/zip you type in.

## Features

- **Putting, Chipping, and Driver** practice sections, 8 drills each
- Each drill has **Beginner / Intermediate / Advanced** goal tiers
- **Session logging** — attempts, makes, and notes per session
- **History tab** with total sessions, sessions this week, and day streak
- **Nearby tab** — finds golf courses and driving ranges within 25 miles using OpenStreetMap/Overpass data, with an embedded map and one-tap directions

## Data & Privacy

All session data is saved locally in your browser's `localStorage` under the key `golf-sessions` — nothing is sent to a server, and nothing syncs between devices or browsers. Clearing your browser data or site storage will erase your history. The Nearby tab sends your location (or the city/zip you enter) to OpenStreetMap/Nominatim and Google Maps solely to look up and display nearby courses.
