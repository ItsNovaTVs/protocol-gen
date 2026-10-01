# Science Protocol Generator

A small, offline lab-protocol editor for school chemistry and other science experiments. It follows the German *Musterprotokoll* structure: **P**roblem, **H**ypothese, **B**eobachtung, **D**eutung.

**Language:** [English](#english) · [Deutsch](README.de.md)

## Features

- **Structured protocol:** date, title, P (problem/question/aim), H (testable hypothesis), B (observations), D (interpretation), and optional error sources/improvements.
- **Rich chemistry formatting:** subscript and superscript formatting for formulas such as H₂O and CO₂.
- **Reaction symbols:** quick buttons for →, ⇌, ↑, ↓, +, and Δ.
- **Observation modes:** switch between free text and an editable measurement table.
- **Improved tables:** separate row/column headers, a diagonal corner cell for the two axes, add/remove rows and columns, and keyboard Tab navigation.
- **Experimental sketches:** draw directly in the browser with an Apple Pencil, stylus, or drawing tablet using pointer events. Sketches are included when printing/exporting to PDF.
- **Autosave:** data is stored locally in the browser and restored on the next visit.
- **Export:** copy as plain text, save as `.txt`, or print/save as PDF.
- **Fully offline:** the app is a single `index.html` with its styling already inlined. No server or CDN is required.
- **Dark editor UI** with a printer-friendly white layout.

## Usage

1. Clone the repository or download `index.html`.
2. Open `index.html` in a modern browser.
3. Fill in the protocol.
4. Use the formatting and reaction-symbol buttons in the **D** section when writing chemical equations.
5. Switch **Beobachtung / Observations** to **Table** when measurements fit better in a grid.
6. Use the **Versuchsskizze / Experimental sketch** area for hand-drawn diagrams when a stylus or pointer device is available.
7. Print or save as PDF when finished.

```bash
git clone https://github.com/ItsNovaTVs/protocol-gen.git
cd protocol-gen
# Open index.html in your browser
```

## Protocol structure

| Section | Meaning |
| --- | --- |
| Datum | Date of the experiment |
| Überschrift | Experiment title |
| **P** | Problem / question / aim |
| **H** | Testable hypothesis |
| **B** | Observations, as text or a measurement table |
| **D** | Interpretation, reaction equations, and general rules |
| Fehler / Verbesserung | Optional sources of error and improvements |
| Versuchsskizze | Optional hand-drawn experimental sketch |

## Privacy

Everything stays on your device. The app uses browser `localStorage` for autosave and does not send protocol contents to a server.

## Development

The project is intentionally simple: plain HTML, CSS, and vanilla JavaScript. There is no build step required to run the application.

The styling currently includes a compiled/inlined Tailwind CSS reset and utility set. If the styling is changed, the generated CSS can be rebuilt separately, but contributors do not need Node.js just to run or modify the application logic.

## Browser support

Current Safari, Chromium-based browsers, and Firefox should support the editor. Stylus and drawing-tablet support depends on the browser exposing standard Pointer Events. Apple Pencil input is supported in browsers that expose the Pencil as a pointer device.

Clipboard access may be restricted for locally opened files in some browsers. The `.txt` export does not require clipboard permissions.

## License

No license is currently specified. If this project is published for reuse, add a `LICENSE` file with the chosen license.

---

# Deutsch

[English](README.md#science-protocol-generator) · [Deutsch](README.de.md)

Ein kleiner, vollständig lokaler Protokoll-Editor für Chemie- und andere naturwissenschaftliche Versuche. Die Struktur orientiert sich am deutschen *Musterprotokoll*: **P**roblem, **H**ypothese, **B**eobachtung und **D**eutung.

### Funktionen

- Strukturierte Protokollfelder für Datum, Überschrift, P, H, B und D.
- **Tief- und Hochstellung** für chemische Formeln, z. B. H₂O und CO₂.
- **Reaktionssymbole** wie →, ⇌, ↑, ↓, + und Δ.
- Beobachtungen als Freitext oder verbesserte Messwerttabelle.
- Diagonales Eckfeld der Tabelle zur Kennzeichnung von Spalten- und Zeilenachse.
- **Versuchsskizze** direkt im Browser mit Apple Pencil, Eingabestift oder Zeichentablett.
- Automatisches Speichern im Browser.
- Export als Text, `.txt` oder PDF über den Druckdialog.
- Komplett offline und ohne Server.

## Entwicklung

Das Projekt besteht bewusst nur aus HTML, CSS und Vanilla-JavaScript. Zum Ausführen der Anwendung ist kein Build-Schritt erforderlich.

## Datenschutz

Die Protokolldaten bleiben auf dem Gerät. Für das automatische Speichern wird `localStorage` verwendet; die Anwendung überträgt keine Protokolldaten an einen Server.

## Lizenz

Aktuell ist keine Lizenz festgelegt. Für eine Weiterverwendung sollte eine passende `LICENSE`-Datei ergänzt werden.