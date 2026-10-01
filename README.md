# Science Protocol Generator
A small, offline lab-protocol generator for school chemistry (and other science) experiments. It follows the German *Musterprotokoll* structure (**P**roblem, **H**ypothese, **B**eobachtung, **D**eutung) and runs as a **single HTML file**. No server, no build step, no internet connection needed.

> The interface is in German, matching the protocol template it is based on.

## Features

- **Template-faithful fields:** Datum, Überschrift, **P** (Problem / Frage / Ziel des Versuchs), **H** (überprüfbare Hypothese), **B** (Beobachtungen), **D** (Deutung), plus an optional field for error sources and improvements.
- **Text or table for "Beobachtung":** switch with one click.
  - *Text:* free-form observations.
  - *Tabelle:* editable measurement table with a corner label for *Werte A → / Werte B ↓*, add/remove rows and columns, Tab navigation, and an optional extra observation note.
- **Fully offline:** Tailwind CSS is compiled and inlined into the file. No CDN, no external fonts.
- **Autosave:** your input is stored in the browser (`localStorage`) and restored on the next visit.
- **Export:**
  - Copy as plain text
  - Save as `.txt` (tables become Markdown tables)
  - Print / save as PDF (print layout is black on white, UI buttons hidden)
- **Dark navy theme** for the editor.

## Usage

1. Download `protokoll.html` (or clone the repo).
2. Open it in any modern browser (double-click is enough).
3. Fill in the fields, pick **Text** or **Tabelle** for the observations, and export when done.

```bash
git clone https://github.com/ItsNovaTVs/protocol-gen.git
cd protocol-gen
# then just open protokoll.html in your browser
```

## Protocol structure

| Section | Meaning |
| --- | --- |
| Datum | Date of the experiment |
| Überschrift | Title |
| **P** | Problem / question / goal of the experiment |
| **H** | Testable hypothesis |
| **B** | Observations, short but complete (text or measurement table) |
| **D** | Interpretation, reaction equations, general rules; record all results, even if they deviate from the goal |
| Fehler / Verbesserung | Optional: what may have gone wrong and how to improve it |

The *Versuchsskizze* (experimental sketch) is intentionally not included.

## Development

The app is plain HTML + vanilla JavaScript with Tailwind CSS (v3) compiled into the file.

To change the styling, edit the Tailwind classes in the source HTML and rebuild the CSS:

```bash
npm install tailwindcss@3
npx tailwindcss -i in.css -c tailwind.config.js -o out.css --minify
```

Then inline `out.css` into the `<style>` block of the HTML file.

`in.css`:

```css
@tailwind base;
@tailwind components;
@tailwind utilities;
```

`tailwind.config.js`:

```js
module.exports = { content: ['./src.html'], theme: { extend: {} } }
```

## Browser support

Any current Chromium-based browser, Firefox, or Safari. Clipboard copy may be blocked by some browsers for locally opened files; use **Als .txt speichern** in that case.

## Privacy

Everything stays on your device. The app makes no network requests and sends no data anywhere.

## License

Add a license of your choice (for example MIT) in a `LICENSE` file.
