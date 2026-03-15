# Jesse — Photography

A personal photography portfolio site built with plain HTML, CSS, and JavaScript.

## Structure
```
jesse-photos/
├── index.html     ← the website
├── photos.json    ← photo list (filenames, captions, categories)
├── SETUP.md       ← detailed setup instructions
└── images/        ← photo files go here
```

## Adding Photos

1. Drop image files into the `images/` folder
2. Add an entry to `photos.json`:
```json
{
  "file": "your-photo.jpg",
  "caption": "Optional caption",
  "category": "landscape"
}
```

## Deployment

Hosted on Render as a static site. Push to main to redeploy automatically.
