# Teens Gospel Fest 2026 — Landing Page

A single-page landing website for **Teens Gospel Fest 2026**, a creative gospel festival for Christian teenagers to discover, develop, and deploy their God-given gifts for His glory.

![Teens Gospel Fest](bg.jpg)

---

## 📖 About the Project

This is a responsive, single-page marketing website designed to:

- Introduce the Teens Gospel Fest 2026 vision and mission
- Showcase the 8+ creative categories (music, dance, drama, etc.)
- Present the festival programs and experience
- Capture interest via a **waitlist signup** (Google Form modal)
- Provide direct contact information for enquiries

Built with **HTML + Tailwind CSS (CDN)** — no build step, no dependencies, no framework. Just open the file in a browser.

---

## 📁 File Structure

```
teens-gospel-fest/
├── index.html      # Main landing page (all-in-one HTML + CSS + JS)
├── bg.jpg          # Hero background image
├── logo.png        # Site logo (used in nav + favicon)
└── README.md       # This file
```

---

## 🚀 Quick Start

### 1. Clone or Download

Download all files into a single folder:

```
teens-gospel-fest/
├── index.html
├── bg.jpg
├── logo.png
└── README.md
```

### 2. Open in Browser

Double-click `index.html` — that's it. The site works immediately with no server required.

For live preview while editing, use VS Code's **Live Server** extension or run:

```bash
# Python 3
python -m http.server 8000

# Node.js (if you have npx)
npx serve
```

Then visit `http://localhost:8000`.

---

## ⚙️ Configuration

### 🎨 Background Image (`bg.jpg`)

The hero section uses a background image for visual impact. Replace `bg.jpg` with your own image, keeping the **exact filename**.

| Property | Recommendation |
|----------|----------------|
| Resolution | 1920×1080px or higher |
| File size | Under 500KB (compress with [squoosh.app](https://squoosh.app) or [tinyjpg.com](https://tinyjpg.com)) |
| Content | Worship concert, teen crowd, stage lights, raised hands |
| Crop | Keep center relatively clean — the title text overlays it |

The image is automatically covered with a dark gradient overlay so text stays readable regardless of the photo.

### 🖼️ Logo (`logo.png`)

Used in two places:
1. **Favicon** — the small icon in the browser tab
2. **Navigation bar** — top-left corner, next to the "TEENS GOSPEL FEST" wordmark

Recommended: **512×512px PNG** with transparent background, square aspect ratio.

### 📝 Waitlist Google Form

The "Join the Waitlist" button opens a modal with an embedded Google Form. To connect your own form:

1. Open your Google Form
2. Click **Send** (top right)
3. Click the **`<>`** (embed) icon
4. Copy the URL inside `src="..."`
5. In `index.html`, find this line (around line 470):

```html
<iframe 
    src="https://docs.google.com/forms/d/e/1FAIpQLSf_YOUR_FORM_ID_HERE/viewform?embedded=true"
    ...
```

6. Replace the placeholder URL with your own embed URL

**Important:** Set your Google Form's sharing setting to **"Anyone with the link can respond"** so visitors can submit without signing in.

### 📞 Contact Numbers

To change the phone numbers displayed in the CTA section, find this block in `index.html`:

```html
<div class="flex flex-wrap justify-center gap-x-6 gap-y-2 text-sm font-semibold text-white">
    <span>08161232797</span>
    <span>08163611763</span>
    <span>08136093359</span>
    <span>09025958168</span>
</div>
```

Update each `<span>` with your numbers.

### 🎨 Colors

The design uses a dark navy + vibrant yellow theme matching the original festival poster. To customize, look for Tailwind utility classes:

| Element | Class |
|---------|-------|
| Primary accent (yellow) | `text-yellow-400`, `bg-yellow-400` |
| Dark backgrounds | `bg-slate-950`, `bg-slate-900` |
| Body text | `text-slate-300`, `text-slate-400` |
| Primary blue | `text-blue-400`, `border-blue-500` |

For a full theme change, edit the `<style>` block at the top of `index.html`.

---

## 📱 Responsive Design

The site is fully responsive and tested across:

- 📱 **Mobile** (320px+) — stacked layout, hamburger-free nav (links hidden on mobile)
- 📱 **Tablet** (768px+) — 2-column grids activate
- 💻 **Desktop** (1024px+) — full 4-column grids, fixed parallax background

The hero's `background-attachment: fixed` is disabled on mobile to avoid scrolling bugs on iOS.

---

## 🌐 Deployment

This is a static site — deploy anywhere for free.

### Option 1: Netlify (Recommended — Drag & Drop)

1. Go to [app.netlify.com/drop](https://app.netlify.com/drop)
2. Drag your entire project folder into the drop zone
3. Done — you get a live URL instantly

### Option 2: Vercel

1. Go to [vercel.com/new](https://vercel.com/new)
2. Import your Git repo (or upload files)
3. Deploy — zero configuration needed

### Option 3: GitHub Pages

```bash
git init
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/teens-gospel-fest.git
git push -u origin main
```

Then go to **Settings → Pages** in your repo, set source to `main` branch, and save.

### Option 4: Any Web Host

Upload `index.html`, `bg.jpg`, and `logo.png` to your public HTML folder via FTP or cPanel.

---

## 🛠️ Tech Stack

| Technology | Purpose |
|------------|---------|
| HTML5 | Structure |
| [Tailwind CSS (CDN)](https://tailwindcss.com) | Utility-first styling — no build step |
| [Google Fonts](https://fonts.google.com) | Montserrat (headings) + Open Sans (body) |
| Vanilla JavaScript | Modal open/close, Escape key handling |

**No npm, no bundler, no framework.** The entire site is a single HTML file plus two images.

---

## ✨ Features

- ✅ Fully responsive single-page layout
- ✅ Hero section with background image and dark overlay
- ✅ Stats bar (Days / Categories / Talents)
- ✅ Mission & Vision cards
- ✅ 8-item creative categories grid
- ✅ 6 program highlight cards
- ✅ Waitlist modal with Google Form embed
- ✅ Contact phone numbers
- ✅ Smooth scroll to sections via nav anchors
- ✅ Accessible modal (Escape key, click-outside to close)
- ✅ Custom scrollbar in modal
- ✅ Favicon from `logo.png`

---

## 📋 Sections Overview

| Section | Anchor | Purpose |
|---------|--------|---------|
| Hero | `#top` | Main headline + CTAs |
| Stats | — | Quick credibility metrics |
| Three Pillars | — | Music / Arts / Fellowship highlight |
| About | `#about` | Mission, Vision, Simple Call |
| Experience | `#experience` | 8 creative categories |
| Programs | `#programs` | 6 experience cards |
| CTA | — | Waitlist button + contact numbers |
| Footer | — | Tagline + copyright |

---

## 🧪 Browser Support

| Browser | Status |
|---------|--------|
| Chrome / Edge | ✅ Fully supported |
| Firefox | ✅ Fully supported |
| Safari (macOS/iOS) | ✅ Supported (fixed bg disabled on mobile) |
| Samsung Internet | ✅ Supported |
| IE 11 | ❌ Not supported (uses CSS variables, backdrop-filter) |

---

## 📄 License

© 2026 Teens Gospel Fest. All rights reserved.

Tagline: *Discover your gift. Create for Christ. Show forth His beauty.*

---

## 🙏 Acknowledgements

- Festival theme and content inspired by the original **Teens Gospel Fest 2026** poster
- Design structure referenced from [Short Cutz Cr8tv Festival](https://shortcutzcr8tvfest.netlify.app/)
- Built with [Tailwind CSS](https://tailwindcss.com) and [Google Fonts](https://fonts.google.com)

---

**Jesus Changes Teens' Lives!**
```

