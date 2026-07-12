# Töwerland-Schatzsuche 🏴‍☠️

Interaktive Schatzsuche für Kinder auf der Insel Juist. 12 Stationen im Ortskern,
mit Foto-Beweis, Ortsfrage, Inselwissen und Kontrollfrage pro Station.
Lösungswort: wird Buchstabe für Buchstabe gesammelt.

## Veröffentlichen mit GitHub Pages

1. Neues Repository anlegen: https://github.com/new
   - Name z. B. `juist-schatzsuche`, Sichtbarkeit **Public** (Pflicht für Pages im Free-Plan)
2. `index.html` und `README.md` hochladen ("Add file" → "Upload files") und committen
3. **Settings → Pages** öffnen
   - Source: **Deploy from a branch**
   - Branch: `main`, Ordner: `/ (root)` → **Save**
4. Nach 1–2 Minuten ist die Seite erreichbar unter:
   `https://<dein-benutzername>.github.io/juist-schatzsuche/`
5. Link per AirDrop/iMessage aufs Kinder-iPhone schicken.
   Dort in Safari öffnen und über Teilen-Menü **"Zum Home-Bildschirm"** hinzufügen.

## Technik

- Eine einzige `index.html`, keine Abhängigkeiten außer Google Fonts (CDN)
- Spielstand und Fotos werden im `localStorage` des Browsers gespeichert
  - Fotos werden auf max. 800 px verkleinert und komprimiert (~100–150 KB pro Foto),
    damit alle 12 sicher ins Safari-Speicherlimit (~5 MB) passen
  - "Von vorn beginnen" löscht Spielstand **und** Fotos
- Wichtig: Der Spielstand hängt am Browser. Nicht zwischendurch den
  Safari-Verlauf/Websitedaten löschen, sonst ist der Fortschritt weg.

## Anpassen

Stationen, Fragen und Texte stehen im `STATIONS`-Array in `index.html`.
Das Lösungswort steht im `CODE`-Array (ein Zeichen pro Station).
