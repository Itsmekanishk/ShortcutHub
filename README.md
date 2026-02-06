# ShortcutHub

**ShortcutHub** is a futuristic, single-page web app for finding keyboard shortcuts and common OS commands. Pick an OS (Mac, Windows, Android, Linux) and search in natural language to instantly filter the built-in shortcut database.

## Features

- **OS selector**: Mac, Windows, Android, Linux
- **Fast search**: keyword + simple fuzzy/token matching (e.g., “take screenshot”, “open terminal”)
- **Categorized results**: shortcuts are grouped (General, Finder/Explorer, Power, etc.)
- **Zero build setup**: runs as a static `index.html`

## Run locally

### Option 1: Open directly

1. Download/clone the repo
2. Open `index.html` in your browser

### Option 2: Serve with a local web server (recommended)

From the project folder:

```bash
python3 -m http.server 5173
```

Then open `http://localhost:5173` in your browser.

## Customize / add shortcuts

All shortcut data is stored inside `index.html` in the `shortcutDatabase` object.

- Add a new item under the relevant OS array:
  - `task`: what the shortcut does
  - `keys`: the key combination / gesture
  - `category`: grouping label shown in results

Example shape:

```js
{ task: "Take Screenshot", keys: "Win + Shift + S", category: "System" }
```

## Deploy to GitHub Pages

Because this is a static site, GitHub Pages works well.

1. Push this repo to GitHub
2. In your GitHub repo, go to **Settings → Pages**
3. Under **Build and deployment**, choose:
   - **Source**: “Deploy from a branch”
   - **Branch**: `main` (or your default branch) and **/ (root)**
4. Save, then open the Pages URL GitHub provides

## Tech stack

- **HTML/CSS/Vanilla JavaScript**
- External CDNs:
  - Google Fonts (Outfit)
  - Font Awesome icons

## Notes

- Despite the “AI-powered” tagline in the UI, the current implementation uses **client-side filtering** (token matching) rather than an external AI service.

## License

No license file is included yet. If you plan to open-source this, consider adding a `LICENSE` (MIT/Apache-2.0/GPL, etc.).

