# Science Protocol Generator

**Sprache:** [English](README.md) · [Deutsch](README.de.md)

Ein kleiner, vollständig lokaler Protokoll-Editor für Chemie- und andere naturwissenschaftliche Versuche. Die Struktur orientiert sich am deutschen *Musterprotokoll*: **P**roblem, **H**ypothese, **B**eobachtung und **D**eutung.

## Funktionen

- **Strukturiertes Protokoll:** Datum, Überschrift, P (Problem/Frage/Ziel), H (überprüfbare Hypothese), B (Beobachtung), D (Deutung) sowie Fehlerquellen und Verbesserungen.
- **Chemie-Formatierung:** Tief- und Hochstellung für Formeln wie H₂O und CO₂.
- **Reaktionssymbole:** Schnelltasten für →, ⇌, ↑, ↓, + und Δ.
- **Beobachtungen:** Freitext oder editierbare Messwerttabelle.
- **Verbesserte Tabellen:** getrennte Zeilen-/Spaltenköpfe, diagonales Eckfeld für die beiden Achsen, Zeilen und Spalten hinzufügen/entfernen sowie Tab-Navigation.
- **Versuchsskizze:** direkt im Browser mit Apple Pencil, Eingabestift oder Zeichentablett zeichnen. Die Skizze wird beim Drucken bzw. Speichern als PDF berücksichtigt.
- **Automatisches Speichern:** Die Daten werden lokal im Browser gespeichert und beim nächsten Besuch wiederhergestellt.
- **Export:** als Text kopieren, als `.txt` speichern oder drucken/PDF speichern.
- **Komplett offline:** Die Anwendung besteht aus einer einzelnen `index.html`; kein Server und kein CDN sind erforderlich.

## Verwendung

1. Repository klonen oder `index.html` herunterladen.
2. `index.html` in einem modernen Browser öffnen.
3. Protokoll ausfüllen.
4. Im Bereich **D** die Formatierungs- und Reaktionssymbol-Schaltflächen für chemische Gleichungen verwenden.
5. Bei Messwerten auf **Tabelle** umschalten.
6. Für eine handgezeichnete Versuchsskizze den Skizzenbereich mit einem kompatiblen Stift oder Zeigegerät verwenden.
7. Anschließend drucken oder als PDF speichern.

```bash
git clone https://github.com/ItsNovaTVs/protocol-gen.git
cd protocol-gen
# index.html im Browser öffnen
```

## Protokollstruktur

| Abschnitt | Bedeutung |
| --- | --- |
| Datum | Datum des Versuchs |
| Überschrift | Titel des Versuchs |
| **P** | Problem / Frage / Ziel |
| **H** | Überprüfbare Hypothese |
| **B** | Beobachtung als Text oder Messwerttabelle |
| **D** | Deutung, Reaktionsgleichungen und allgemeine Regeln |
| Fehler / Verbesserung | Optionale Fehlerquellen und Verbesserungen |
| Versuchsskizze | Optionale handgezeichnete Versuchsskizze |

## Datenschutz

Alle Protokolldaten bleiben auf dem Gerät. Für das automatische Speichern wird `localStorage` verwendet. Die Anwendung überträgt keine Protokolldaten an einen Server.

## Entwicklung

Das Projekt besteht bewusst nur aus HTML, CSS und Vanilla-JavaScript. Zum Ausführen der Anwendung ist kein Build-Schritt erforderlich.

## Browser-Unterstützung

Aktuelle Versionen von Safari, Chromium-basierten Browsern und Firefox sollten den Editor unterstützen. Stift- und Zeichentablett-Unterstützung hängt davon ab, ob der Browser standardmäßige Pointer Events bereitstellt. Apple-Pencil-Eingaben funktionieren in Browsern, die den Pencil als Pointer-Gerät bereitstellen.

Die Zwischenablage kann bei lokal geöffneten Dateien in manchen Browsern eingeschränkt sein. Der `.txt`-Export benötigt keine Zwischenablage-Berechtigung.

## Lizenz

Derzeit ist keine Lizenz festgelegt. Für eine Weiterverwendung sollte eine passende `LICENSE`-Datei ergänzt werden.