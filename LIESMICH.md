# PackScan und Inventur 1.3.1

Zwei Web-Apps für iPhone und Android, die direkt mit Dolibarr arbeiten:

- **PackScan:** Pickliste nach Lagerplatz, Freigabe gepickter Aufträge, Einpacken per Label-Scan (mehrere Lieferungen mit gleicher Sendungsnummer als ein Paket), Versand abschließen
- **Inventur:** Artikel scannen, Lagerplatz vergeben, Bestand je Lager korrigieren, Zählliste und Inventurprotokoll als PDF oder CSV exportieren, Einlagern und Zurücklegen (Lagerplatz mit Wand-Raster, Bestand prüfen, Menge bestätigen)

Quellcode und Änderungen: https://github.com/groods-apps/packscan

## Sprachen

Beide Apps starten in der Sprache des Browsers. In den Einstellungen lässt sich jede der 24 Sprachen fest wählen: Deutsch, Englisch, Französisch, Spanisch, Italienisch, Portugiesisch, Niederländisch, Polnisch, Tschechisch, Slowakisch, Ungarisch, Rumänisch, Bulgarisch, Kroatisch, Slowenisch, Griechisch, Schwedisch, Dänisch, Norwegisch, Finnisch, Estnisch, Lettisch, Litauisch, Ukrainisch. Wird die Browsersprache nicht unterstützt, startet die App auf Englisch.

## Installation in drei Schritten

1. Ordner `htdocs/custom/lager/` in deiner Dolibarr-Installation anlegen.
2. Alle Dateien aus diesem Archiv hineinkopieren.
3. `https://dein-dolibarr.de/custom/lager/` auf dem Smartphone öffnen, App wählen, Zahnrad, API-Token eintragen, „Verbindung testen“.

Dolibarr muss über HTTPS erreichbar sein, sonst gibt das Smartphone die Kamera nicht frei.

Vorher in Dolibarr einrichten: Module, ergänzende Attribute (`lagerplatz`, `gtin`, `letzte_inventur`, `gepickt`), Versandarten und einen API-Benutzer mit passenden Rechten. Die ausführliche Anleitung steht auf der Website unter „Anleitung“.

## Dateien

| Datei | Inhalt |
|---|---|
| `index.html` | Startseite mit Links zu beiden Apps |
| `packscan.html` | PackScan |
| `inventur.html` | Inventur |
| `*.manifest.json`, `*.png` | Icons und Angaben für „Zum Home-Bildschirm“ |

## Lizenz

Copyright (C) 2026 Stefan Grumpelt, gRoods.de

Dieses Programm ist freie Software: Du kannst es unter den Bedingungen der GNU General Public License, Version 3 oder (nach deiner Wahl) jeder späteren Version, weitergeben und verändern. Es wird ohne jede Gewährleistung bereitgestellt. Den Lizenztext findest du in der Datei `LICENSE`.

Enthält ZXing-C++ (Apache-2.0) über zxing-wasm (MIT). Das Auslesen des Internetmarken-Matrixcodes folgt dem Verfahren der App BinaryEye (MIT).

Kontakt und Einrichtungspaket: info@groods.de, WhatsApp +49 351 16078332
