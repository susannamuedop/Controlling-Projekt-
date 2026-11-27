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

Das Dashboard folgt der Ad-Alliance-CI aus der Präsentationsvorlage (Theme „RTL United White“):

- **Basis Schwarz/Weiß:** schwarze Navigation, schwarze Primär-Buttons und aktive Zustände, weiße Flächen.
- **Logo:** Ad-Alliance-Logo im Kopf, „Part of RTL“ im Navigationsfuß, Logo-Verlauf (`#E30164 → #784898 → #00B6ED`) als Linie über dem Kopf.
- **Akzentfarben aus dem Theme:** Violett `#6E0CED` (Akzent 1, Hauptserie in Charts), Blau `#0C39ED` (Links), Petrol `#009699`, Orange `#FF5C01`, Gelb `#EDC00C`, Rot `#D4000D`.
- **Schrift:** „RTL United Text“, sofern lokal installiert; sonst Inter als frei verfügbarer Ersatz. Die Hausschrift wird nicht mitgeliefert.
- **Form:** kantige Ecken (4 px), keine Schatten, fette Überschriften.

Die Farben liegen zentral als CSS-Variablen (`--pink` = Primäraktion, `--blue` = Akzent, `--link`, `--brand-grad` …) und in den Chart-Paletten (`C`, `PUB_COLORS`, `GES_COLORS`, `IMPORT_PALETTE`). Grün/Orange/Rot bleiben für Ampel und Abweichungen erhalten.

## Funktionen

- **Übersicht, Forecast-Analyse, Szenarien, Datenqualität, Excel-Import & SAP, Methodik**
- Filter nach Version (Budget, FC I–IV), Monat, Publisher, Gesellschaft und Wertebene (Netto 2 / Netto 4)
- KI-Forecast-Vorschlag für offene Monate, Markierung bei Abweichungen über 5 %
- Excel-Import mit automatischer Spaltenerkennung und 8-stufiger Prüfung
- GuV-Überleitung Netto 2 → Netto 4 und SAP-Upload-Datei (simuliert)
- Freigabe-Workflow Brand → Controlling → Geschäftsführung
- Simulierter, regelbasierter Controlling-Chat mit drei Rollen

> **Hinweis:** KI-Prototyp. Ergebnisse können Fehler enthalten und müssen vor Freigabe durch Controlling und Geschäftsführung geprüft werden. Keine produktive Systemanbindung.
