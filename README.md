# Hamtramck Bazaar Retail Accelerator
## Orientation Presentation

A code-based slide deck built with [Reveal.js](https://revealjs.com/).  
Navigate with **Left / Right arrow keys** or a standard USB clicker.

---

## Repo Structure

```
bazaar-orientation/
├── index.html        ← Main presentation (all slides live here)
├── css/
│   └── theme.css     ← All branding, colors, layout, hover effects
└── README.md         ← This file
```

**To edit slides:** Open `index.html` in VS Code. Each slide is a `<section>` block. Search for the slide title comment (e.g., `SLIDE 3 · INTRODUCTIONS`) to jump to it.

**To edit colors or typography:** Open `css/theme.css`. All brand colors are CSS variables at the top of the file under `TOKENS`.

---

## Running Locally

No build step needed. Two options:

### Option 1 — VS Code Live Server (recommended)
1. Install the [Live Server extension](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer) in VS Code
2. Right-click `index.html` → **Open with Live Server**
3. Opens at `http://127.0.0.1:5500`

### Option 2 — Python (no extensions needed)
```bash
cd bazaar-orientation
python3 -m http.server 8080
```
Then open `http://localhost:8080` in your browser.

> ⚠️ Do not open `index.html` directly as a `file://` URL — Reveal.js needs to run from a server (even a local one) to work correctly.

---

## Deploying to Cloudflare Pages

1. Push this repo to GitHub via GitHub Desktop
2. Go to [Cloudflare Pages](https://pages.cloudflare.com/) → **Create a project**
3. Connect your GitHub account and select this repo
4. Set these build settings:
   - **Build command:** *(leave blank)*
   - **Build output directory:** `/` (root)
5. Click **Save and Deploy**

Your deck will be live at a `*.pages.dev` URL within ~30 seconds.  
Every push to `main` auto-deploys — no manual step needed.

---

## Navigation

| Action | Key |
|---|---|
| Next slide / fragment | → Right arrow or Space |
| Previous slide / fragment | ← Left arrow |
| Jump to slide | Press `G` then type slide number |
| Overview mode | Press `O` |
| Full screen | Press `F` |
| Pause / black screen | Press `B` |

**USB clicker:** Any standard HID presentation clicker (Logitech R400, R800, etc.) works immediately — forward/back buttons map to right/left arrows natively.

---

## Editing Tips

### Adding a new slide
Copy an existing `<section>` block and paste it between two others. The `data-transition` attribute controls the entry animation for that slide (`slide`, `fade`, `zoom`, `none`).

### Fragment (step-by-step reveal) on an element
Add `class="fragment fade-up"` to any element to make it appear on the next arrow press:
```html
<p class="fragment fade-up">This appears on next press.</p>
```

### Changing brand colors
Edit the `:root` block at the top of `css/theme.css`:
```css
:root {
  --teal:   #016B78;   /* ← change this */
  --amber:  #D4861A;   /* ← or this */
}
```
The change cascades everywhere automatically.

---

## Dependencies

All loaded via CDN — no npm, no build step:
- [Reveal.js 5.1](https://cdnjs.cloudflare.com/ajax/libs/reveal.js/5.1.0/)
- [Google Fonts: Outfit + Lato](https://fonts.google.com)

Requires internet connection to load fonts and Reveal.js on first run. For fully offline use, download those assets and update the paths in `index.html`.
