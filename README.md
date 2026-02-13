# Mietwerk 2D

Ein funktionsorientiertes 2D-Vermieter-Management-Spiel im Browser (Canvas + Vanilla JS).

## Starten
1. `index.html` lokal im Browser öffnen (kein Build, keine Abhängigkeiten).
2. Sofort spielbar.

## Ziel des Spiels
- **Verlieren**: Cash < 0 (Bankrott).
- **Gewinnen**: Cash > 250.000 € und Belegungsquote > 85 % über 3 Monate.

## Steuerung / Kernablauf
- Karte: Objekt anklicken, um Details zu sehen.
- Zeit:
  - `+1 Woche`
  - `+4 Wochen`
- Finanzen:
  - `Mieten einziehen`
  - `Kreditrate zahlen`
- Management:
  - `Objekt erstellen`
  - `Einheit hinzufügen`
  - `Inserat`
  - `Miete erhöhen`
  - `Renovieren`
  - `Aufgabe erstellen`

## Speichern / Laden
- **Autosave** nach jedem Tick und wichtigen Aktionen.
- Buttons:
  - `Speichern` (manuell in `localStorage`)
  - `Laden` (manuell aus `localStorage`)
  - `Export JSON` (Savegame in Textfeld)
  - `Import JSON` (JSON aus Textfeld einlesen)

## Hinweise zum Gameplay
- Schlechter Zustand und hohe Abnutzung erzeugen mehr Schäden/Tickets.
- Niedrige Zufriedenheit erhöht Kündigungs- und Mietausfallrisiken.
- Renovierung ist teuer, verbessert aber Zustand, Zufriedenheit und Langzeitstabilität.
