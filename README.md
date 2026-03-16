# 🖼️ media-to-base64

> Encode **images and videos** to Base64 — or decode Base64 back to a media file — right in your browser. No installs, no uploads, no server.

[![License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)
[![Version](https://img.shields.io/badge/version-1.0.0-green.svg)](https://github.com/MrLiPx/media-to-base64/releases)
[![Live Demo](https://img.shields.io/badge/demo-live-brightgreen.svg)](https://mrlipx.github.io/media-to-base64)

---

## ✨ Features

- **Images & videos** — JPEG, PNG, GIF, WebP, SVG, ICO, MP4, WebM and more
- **Encode & decode** — full round-trip Base64 with a single click
- **Live preview** — instant image and video previews rendered from `blob://` URLs
- **URL import** — fetch a remote media file directly, with automatic CORS proxy fallback
- **`?import=`** — pre-load a URL automatically via query parameter
- **Data URI builder** — generates a ready-to-use `data:image/png;base64,…` string with editable MIME type
- **Drag & drop** — drop any media file onto the page
- **Truncation** — large outputs show a snippet with "Show all" / "Copy full" controls
- **Zero dependencies** — pure HTML, CSS, and vanilla JS

---

## 🚀 Usage

### Open in browser

```
open index.html
```

Or serve locally:

```bash
npx serve .
# → http://localhost:3000
```

### Encode a media file

1. Drop an image or video onto the drop zone, or click **Browse**
2. The Base64 output appears instantly with a live preview below
3. Copy the raw Base64, or grab the full **Data URI** from the builder

### Decode Base64

1. Switch to **DECODE** mode
2. Paste a Base64 string or a full `data:image/png;base64,…` data URI
3. The decoded image or video renders as a live preview

### Import from a URL

Paste any direct media URL into **Import file from URL** and click **FETCH**.

The tool tries a direct fetch first. If the server blocks it (CORS), it automatically retries through the [AllOrigins](https://allorigins.win) proxy — no action required from you.

---

## 🔗 `?import=` Parameter

Pre-load any public media URL by appending `?import=<url>` to the page URL:

```
https://mrlipx.github.io/media-to-base64?import=https://example.com/photo.jpg
```

The file is fetched and encoded automatically on page load.

---

## 🖼️ Supported Formats

| Type | Formats |
|------|---------|
| **Image** | JPEG · PNG · GIF · WebP · SVG · ICO |
| **Video** | MP4 · WebM |

Previews use `blob://` URLs built with `URL.createObjectURL()` — your files never leave the browser.

---

## 📁 Project Structure

```
media-to-base64/
├── index.html        # Single-file app — everything is here
├── assets/
│   └── logo.png      # App logo used as header image and favicon
└── README.md
```

---

## ⚙️ Options

| Option | Description |
|--------|-------------|
| **URL-safe** | Replaces `+` → `-` and `/` → `_` for safe embedding in URLs |
| **No padding** | Strips trailing `=` padding characters |
| **Auto-run** | Re-encodes/decodes automatically as you type |
| **Data URI auto-generate** | Keeps the `data:…;base64,…` field live as output changes |

---

## 🛠️ Built With

- [IBM Plex Mono & Sans](https://fonts.google.com/specimen/IBM+Plex+Mono) — typography
- [Flaticon UIcons](https://www.flaticon.com/uicons) — icons (`uicons-regular-rounded`)
- [AllOrigins](https://allorigins.win) — CORS proxy fallback for URL imports

---

## 🤝 Contributing

1. Fork this repo
2. Create your branch: `git checkout -b feat/my-feature`
3. Commit: `git commit -m 'feat: add my feature'`
4. Push: `git push origin feat/my-feature`
5. Open a Pull Request

Please keep the project dependency-free (no npm, no bundler).

---

## 📄 License

MIT © [MrLiPx](https://github.com/MrLiPx)

---

<p align="center">
  Made by <a href="https://github.com/MrLiPx">@MrLiPx</a> · Star ⭐ if it's useful!
</p>
