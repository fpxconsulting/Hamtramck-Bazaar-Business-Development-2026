# Hamtramck Bazaar Business Development Course
## April 2026 Cohort — Slide Deck Collection

A code-based presentation system built with [Reveal.js](https://revealjs.com/).  
One shared codebase, consistent branding, six sessions.  
Navigate with **Left / Right arrow keys** or a standard USB clicker.

---

## Repo Structure

Hamtramck-Bazaar-Business-Development-2026/
├── orientation.html  ← Orientation session (April 25, 2026)
├── session-1.html    ← Session 1: Business Clarity (May 2)
├── session-2.html    ← Session 2: Pricing and Hidden Costs
├── session-3.html    ← Session 3: Sales and Visibility
├── session-4.html    ← Session 4: Operations
├── session-5.html    ← Session 5: Pitch and Direction
├── css/
│   └── theme.css     ← All branding, colors, layout — shared across all sessions
├── assets/
│   ├── access-logo.png
│   ├── fpx-logo.png
│   └── hamtramck-bazaar-logo.png
└── README.md         ← This file

To edit slides: Open the relevant session file in VS Code. Each slide is a <section> block. Search for the slide title comment to jump to it.

To edit colors or typography: Open css/theme.css. All brand colors are CSS variables at the top under TOKENS. Changes cascade across all six session files automatically.

---

## Session Index

| File | Session | Date |
|---|---|---|
| orientation.html | Orientation | April 25, 2026 |
| session-1.html | Business Clarity | May 2, 2026 |
| session-2.html | Pricing and Hidden Costs | TBD |
| session-3.html | Sales and Visibility | TBD |
| session-4.html | Operations | TBD |
| session-5.html | Pitch and Direction | TBD |

---

## Running Locally

No build step needed. Two options:

Option 1 — VS Code Live Server (recommended)
1. Install the Live Server extension in VS Code
2. Right-click the session file you want to present and select Open with Live Server
3. Opens at http://127.0.0.1:5500

Option 2 — Python (no extensions needed)
cd Hamtramck-Bazaar-Business-Development-2026
python3 -m http.server 8080
Then open http://localhost:8080/session-1.html in your browser.

Do not open any HTML file directly as a file:// URL. Reveal.js needs to run from a server, even a local one, to work correctly.

---

## Deploying to Cloudflare Pages

1. Push this repo to GitHub via GitHub Desktop
2. Go to Cloudflare Pages and create a project
3. Connect your GitHub account and select this repo
4. Set Build command to blank and Build output directory to /
5. Click Save and Deploy

Each session file will be available at its own URL. Every push to main auto-deploys.

---

## Navigation

| Action | Key |
|---|---|
| Next slide or fragment | Right arrow or Space |
| Previous slide or fragment | Left arrow |
| Jump to slide | Press G then type slide number |
| Overview mode | Press O |
| Full screen | Press F |
| Pause or black screen | Press B |

USB clicker: Any standard HID clicker works immediately. Forward and back buttons map to right and left arrows natively.

---

## Editing Tips

To add a new slide, copy an existing <section> block and paste it between two others. The data-transition attribute controls the entry animation: slide, fade, zoom, or none.

To make an element reveal on the next arrow press, add class="fragment fade-up" to it.

To change brand colors, edit the :root block at the top of css/theme.css. The change cascades across all session files automatically.

---

## Dependencies

All loaded via CDN — no npm, no build step:
- Reveal.js 5.1
- Google Fonts: Outfit and Lato

Requires an internet connection to load fonts and Reveal.js. For fully offline use, download those assets and update the paths in each HTML file.

---

## Partners

This program is a partnership between ACCESS, the Hamtramck Bazaar, and FPX Consulting.
FPX Consulting is leading the curriculum and instruction for the cohort.