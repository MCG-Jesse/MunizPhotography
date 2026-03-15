# Jesse Photography — Setup Guide

A simple, beautiful gallery site you can host for free and share with anyone.

---

## Quick Start

### Step 1 — Add your photos

Copy your image files into the `images/` folder inside this project.

Any format works: JPG, PNG, WEBP, etc.

**Tip:** Rename your files to something descriptive before adding them, like
`canyon-sunset.jpg` or `haley-portrait.jpg`. It'll make the next step easier.

---

### Step 2 — Update photos.json

Open `photos.json` in any text editor (Notepad, TextEdit, VS Code, etc.)
and list your photos. Each entry looks like this:

```json
[
  {
    "file": "canyon-sunset.jpg",
    "caption": "Sandia Mountains at dusk",
    "category": "landscape"
  },
  {
    "file": "haley-portrait.jpg",
    "caption": "",
    "category": "portrait"
  }
]
```

- **file** — the exact filename in your `images/` folder (required)
- **caption** — shown in the lightbox viewer (optional, leave "" to skip)
- **category** — used for the filter buttons at the top (optional)

You can use any category names you like — "landscape", "street", "travel",
"portrait", etc. They'll automatically appear as filter buttons on the site.

---

### Step 3 — Preview locally (optional)

Open `index.html` directly in your browser to preview the site.

> **Note:** Photos won't load in a plain file:// preview due to browser security
> restrictions. To preview with photos, you can use VS Code's Live Server extension,
> or just deploy to Netlify (it takes 30 seconds — see below).

---

### Step 4 — Deploy to Netlify (free)

This gets you a real link you can share with family.

1. Go to **https://netlify.com** and create a free account (or log in)
2. Click **"Add new site"** → **"Deploy manually"**
3. Drag your entire `jesse-photos` folder onto the upload area
4. Netlify gives you a URL like `https://random-name.netlify.app`
5. Optional: click **"Site settings"** → **"Change site name"** to pick something nicer,
   like `jesse-photography.netlify.app`

That's it. Share the link with family and they can browse your gallery.

---

## Updating the site later

When you want to add more photos:

1. Add the new image files to the `images/` folder
2. Add entries for them in `photos.json`
3. Drag the folder to Netlify again (or use their "deploys" page to upload)

Netlify will automatically update the live site.

---

## Customizing

All the styling and text lives in `index.html`. To change things:

- **Your name in the header** — search for `Jesse` and replace with your name
- **Site title** — update the `<title>` tag and the `og:title` meta tag
- **Column layout** — the grid defaults to 3 columns. Search for `columns: 3`
  and change the number
- **Colors** — the color palette is defined at the top of the `<style>` block
  under `:root { ... }`. `--accent` controls the gold color, `--bg` controls
  the background

---

## File structure

```
jesse-photos/
├── index.html       ← the website
├── photos.json      ← your photo list
├── SETUP.md         ← this guide
└── images/
    ├── your-photo-1.jpg
    ├── your-photo-2.jpg
    └── ...
```

---

Questions? The setup is intentionally simple — if something isn't working,
the most common issue is a filename mismatch between `photos.json` and
what's actually in the `images/` folder. Double-check the spelling and
file extension (`.jpg` vs `.JPG`, etc.)
