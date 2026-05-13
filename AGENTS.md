# AGENTS.md

## Cursor Cloud specific instructions

This is a simple static website (HTML/CSS/JS) with zero build dependencies. There is no package manager, no build tool, and no framework.

### Running the site

Serve the site locally with any static file server. The simplest option:

```sh
python3 -m http.server 8080 --directory /workspace
```

Then open `http://localhost:8080/` in Chrome.

### Structure

- `index.html` — single-page app with inline CSS/JS containing a photo gallery and guestbook
- `ys1.jpg`, `ys2.jpg`, `ys3.jpg`, `kystest.jpg` — photo assets
- `ysvideo1.mp4` — video asset

### Testing

There are no automated tests, linters, or build steps. Verify changes by opening the site in a browser and manually testing both sections:
1. **사진전 (Photo Gallery)** — photos and video render correctly
2. **방명록 (Guestbook)** — form submission creates entries in the DOM

### Notes

- The guestbook is client-side only; entries are stored in the DOM and lost on page refresh.
- No external services, databases, or APIs are required.
