# Mietwerk 2D

Ein funktionsorientiertes 2D-Vermieter-Management-Spiel im Browser (Canvas + Vanilla JS), komplett offline.

## Starten
1. `index.html` lokal im Browser öffnen.
2. Kein Build, keine externen Assets.

## Ziel
- **Verlieren**: Cash < 0.
- **Gewinnen**: Cash > 250.000 € und Belegungsquote > 85 % über 3 Monate.

## Steuerung / Gameplay
- Stadtplan: Objekt anklicken.
- Objektdetails: Wohnungen sind **direkt auswählbar** (`Auswählen`-Button, blau markiert).
- Zeit:
  - `+1 Woche`
  - `+4 Wochen`
- Finanzen:
  - `Mieten einziehen`
  - `Kreditrate zahlen`
- Verwaltung:
  - `Objekt erstellen`
  - `Einheit hinzufügen`
  - `Inserat` (für ausgewählte Wohnung)
  - `Miete erhöhen (Auswahl)`
  - `Vermieten (Auswahl)`
  - `Renovieren`
  - `Aufgabe erstellen`
- **Gebrauchtmarkt**:
  - Jeden Monat neue Angebote
  - Optionales Refresh gegen Gebühr
  - Günstige Effekte mit Defekt-Risiko (kann Reparatur-Task auslösen)

## Speichern / Laden
- **Autosave** nach Ticks und wichtigen Aktionen.
- `Speichern` / `Laden` via `localStorage`.
- `Export JSON` / `Import JSON` über Textfeld.

## Hinweise
- Niedrige Zufriedenheit erhöht Mietausfall/Kündigungsrisiken.
- Renovierung ist teuer, senkt aber Folgekosten/Risiken langfristig.
- Gebrauchtmarkt kann stark helfen, ist aber nicht risikofrei.
