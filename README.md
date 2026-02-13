# Mietwerk 2D

Funktionsorientiertes 2D-Vermieter-Management im Browser (Canvas + Vanilla JS), komplett offline.

## Starten
1. `index.html` im Browser öffnen.
2. Kein Build, keine externen Dependencies.

## Neu: Schwierigkeit, Mieterpool, echter Häusermarkt
- **Schwierigkeit** (Leicht/Normal/Schwer) beim Neustart auswählbar.
- **Mieterpool**: Es gibt einen Bewerber-Pool; Vermietung erfolgt über Bewerber-Auswahl (nicht garantiert passend/erfolgreich).
- **Häusermarkt**: Häuser können nur über Marktangebote gekauft werden.
- **Verkäufe**:
  - Einzelne **Wohnung** verkaufen (nur leer und nicht letzte Einheit des Hauses)
  - Ganzes **Haus** verkaufen (nur wenn alle Einheiten leer)

## Kern-Buttons
- Zeit: `+1 Woche`, `+4 Wochen`
- Finanzen: `Mieten einziehen`, `Kreditrate zahlen`
- Wohnung/Objekt:
  - `Einheit hinzufügen`
  - `Inserat (Auswahl)`
  - `Mieter aus Pool zuweisen`
  - `Miete +5% (Auswahl)`
  - `Wohnung verkaufen (Auswahl)`
  - `Renovieren`
  - `Aufgabe erstellen`
  - `Haus verkaufen`
- Markt:
  - `Häusermarkt aktualisieren`
  - `Gebrauchtmarkt aktualisieren`

## Ziel
- **Game Over**: Cash < 0
- **Sieg**: Cash > 300.000 € und Belegung > 87 % über 3 Monate

## Speichern/Laden
- Autosave nach Ticks und wichtigen Aktionen.
- `Speichern` / `Laden` via `localStorage`.
- `Export JSON` / `Import JSON` via Textfeld.
