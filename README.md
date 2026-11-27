# Umsatz-Forecast-Cockpit

Klickbarer Prototyp eines KI-gestützten Umsatz-Forecast-Dashboards für ein Controlling-Projekt (Medienvermarktung, digitale Werbeerlöse). Alle Daten sind fiktiv und anonymisiert.

## Dateien

| Datei | Inhalt |
|---|---|
| `forecast_dashboard.html` | Der Prototyp – eine einzige HTML-Datei, läuft ohne Backend direkt im Browser |
| `Dokumentation_Forecast-Dashboard.pdf` | Dokumentation: Analyse, Aufbau, Berechnungslogik, Annahmen, Grenzen |
| `Dokumentation_Forecast-Dashboard.html` | Dieselbe Dokumentation als Webseite |

## Starten

`forecast_dashboard.html` im Browser öffnen. Für den Import von `.xlsx`/`.xls` wird eine Internetverbindung benötigt (SheetJS wird von cdnjs geladen); CSV-Import funktioniert offline.

## Design

Dashboard und Dokumentation folgen dem RTL-Corporate-Design: Pink (`#E6007E`) als Akzentfarbe, neutrales Anthrazit für Navigation und Text, Schrift Inter (Ersatz für die nicht frei verfügbare Hausschrift). Die Farben sind zentral als CSS-Variablen (`--pink`, `--navy`, `--blue` …) und in den Chart-Paletten (`C`, `PUB_COLORS`, `GES_COLORS`, `IMPORT_PALETTE`) hinterlegt. Rot/Grün bleiben für Ampel und Abweichungen erhalten.

## Funktionen

- **Übersicht, Forecast-Analyse, Szenarien, Datenqualität, Excel-Import & SAP, Methodik**
- Filter nach Version (Budget, FC I–IV), Monat, Publisher, Gesellschaft und Wertebene (Netto 2 / Netto 4)
- KI-Forecast-Vorschlag für offene Monate, Markierung bei Abweichungen über 5 %
- Excel-Import mit automatischer Spaltenerkennung und 8-stufiger Prüfung
- GuV-Überleitung Netto 2 → Netto 4 und SAP-Upload-Datei (simuliert)
- Freigabe-Workflow Brand → Controlling → Geschäftsführung
- Simulierter, regelbasierter Controlling-Chat mit drei Rollen – als Button unten rechts, öffnet sich per Klick (auf dem Handy als Vollbild)
- Hinweise und Erklärungen erscheinen beim Überfahren mit der Maus bzw. beim Antippen (Handy/Tablet); „Hinweis(e)“ in der Ampelübersicht öffnet per Klick die vollständige Liste
- Ansicht passt sich automatisch an Handy, Tablet, Laptop und große Bildschirme an

> **Hinweis:** KI-Prototyp. Ergebnisse können Fehler enthalten und müssen vor Freigabe durch Controlling und Geschäftsführung geprüft werden. Keine produktive Systemanbindung.
