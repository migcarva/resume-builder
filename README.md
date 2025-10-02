# Resume Builder

Single-file resume editor that runs entirely in the browser. Import your data from `resume.json`, tweak the layout live, and print or export JSON without any build tooling.

## Quick start

1. Clone the repository and enter the project directory.
2. Start a static file server (examples below) and open `http://127.0.0.1:8000`.

```bash
# Option A: Python 3 (preinstalled on macOS/Linux)
python3 -m http.server --bind 127.0.0.1 8000

# Option B: Node.js
npx serve .
```

Alternatively, open `index.html` directly in a modern browser; some features such as the File System Access API work best when served over `http`.

## Usage

- Click the sections in the left panel to edit basics, summary, skills, experience, projects, and education.
- Changes save automatically to `localStorage` (`resumeDataV1`).
- Use **Export JSON** to download a backup, **Import JSON** to load a saved file, and **Print / Save PDF** to produce a shareable document.
- Add company logos by dropping images into `logos/` and selecting them from the logo dropdown inside each experience entry.

## Custom data

The project ships with a neutral sample profile (`resume.json`). Replace it with your own data or export a fresh copy from the editor. Each section accepts arrays of objects—fields are self-explanatory and can be removed if unused.

```json
{
  "version": 1,
  "basics": { "name": "Alex Doe", "title": "Senior Frontend Engineer" },
  "skills": [
    { "group": "Core", "items": ["TypeScript", "React"] }
  ],
  "experience": [
    { "role": "Lead Frontend Engineer", "company": "Acme Analytics" }
  ]
}
```

## Browser support

Tested on the latest Chrome, Edge, Firefox, and Safari. File System Access API buttons fall back to import/export if the browser does not support them.

## License

Released under the MIT License. See `LICENSE` for details.
