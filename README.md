## Resume – Dzmitry Kazachok

One‑page resume site. Minimal, fast, print‑friendly. Includes an optional particles background and a complete favicon set.

### Features
- **Particles toggle**: UI switch to show/hide animated background.
- **URL param support**: open with `?particles=true` to load with particles enabled.
- **Print‑friendly**: particles are hidden when printing (Ctrl+P) for clean output.
- **Favicons**: multi‑size favicon set in `favicon/` with proper `<link>` tags in `index.html`.

### Quick start
- Open directly: `index.html`
- Or run a local server (recommended):

```powershell
cd D:\Docs\MyAI\Personal_Agent_Workspace\03_Career\GitHub\resume
python -m http.server 5500
# then open http://localhost:5500/index.html
```

With particles enabled by URL:
`http://localhost:5500/index.html?particles=true`

### Project structure
```text
resume/
  index.html        # main page
  style.css         # styles (includes @media print to hide particles)
  app.js            # particles init + toggle + URL param handling
  particles.js      # particles.js library
  favicon/          # favicon set (ico + png sizes)
    ├─ favicon.ico
    ├─ favicon-16x16.png
    ├─ favicon-32x32.png
    ├─ android-chrome-192x192.png
    ├─ android-chrome-512x512.png
    └─ apple-touch-icon.png (180x180)
```

### Favicons
- All icons live under `favicon/`.
- Head tags in `index.html` already include ICO/PNG/Apple Touch links with relative paths.
- If a changed icon doesn’t appear immediately, hard‑reload (Ctrl+F5) or add a version query, e.g. `favicon/favicon.ico?v=2`.

### Printing
- Use the browser’s print dialog (Ctrl+P). The particles layer is hidden automatically for clean printouts.