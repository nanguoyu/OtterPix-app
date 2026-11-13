[English](../../en/tools/pdf-and-qr.md) | [简体中文](../../zh-Hans/tools/pdf-and-qr.md) | [繁體中文](../../zh-Hant/tools/pdf-and-qr.md) | **Deutsch**

---

# PDF zu Bild & QR-Code

Zwei kleine, präzise Helfer: **PDF zu Bild** rendert PDF-Seiten in der Auflösung deiner Wahl als Bilddateien, und **QR-Code** erzeugt QR-Codes aus Text oder URLs.

## PDF zu Bild

### Auf einen Blick

| | |
|---|---|
| **Verfügbarkeit** | Kostenlos |
| **Ausführung** | Auf deinem Mac – offline, nichts wird hochgeladen |
| **Eingabe** | Ein PDF („PDF-Datei auswählen oder hierher ziehen“; Einfügen mit ⌘V geht auch) |
| **Ausgabe** | Eine Bilddatei pro Seite, an einem Zielort deiner Wahl |
| **Pipeline-Schritt** | Nein |

### PDF-Seiten umwandeln

1. Klicke auf **PDF zu Bild** und leg ein PDF ab. Das Werkzeug zeigt die Seitenzahl („PDF mit 12 Seiten“) mit einer Seite-für-Seite-Vorschau.
2. Wähl, welche Seiten umgewandelt werden: alle („Alle Seiten (12)“) oder ein **Bereich** mit **Von**/**Bis**-Grenzen – exakte Seitenzahl eintippen oder mit den Steppern anpassen.
3. Stell die **Auflösung (DPI)** ein. Höhere DPI heißt größere, schärfere Bilder – für die Bildschirmnutzung reicht ein moderater Wert; für Druck oder Zoom-Lektüre geh höher.
4. Wähl das Ausgabeformat – PNG für gestochenen Text und Grafik, JPEG für kleinere fotolastige Seiten.
5. Klicke auf **Seite 3 konvertieren & speichern** (einzelne Seite) bzw. **12 Seiten konvertieren & speichern** (Bereich) und wähl das Ziel. **Andere PDF auswählen** wechselt das Dokument, ohne das Werkzeug zu verlassen.

### Tipps und Grenzen

- **PDFs rendern in jeder DPI** – die Quelle ist, wo möglich, Vektor; eine höhere DPI bringt also echte Schärfe statt bloß skalierter Pixel.
- **Eine Datei pro Seite.** Ein Bereichs-Export schreibt nummerierte Bilder, fertig für Folien oder Web-Einbettung.
- ***Text* aus einem gescannten PDF zu holen ist ein anderer Job** – das ist [AI Texterkennung](../ai/ai-ocr.md), die Dokumente und Scans in Markdown verwandelt.

## QR-Code

### Auf einen Blick

| | |
|---|---|
| **Verfügbarkeit** | Kostenlos |
| **Ausführung** | Auf deinem Mac – offline, nichts wird hochgeladen |
| **Eingabe** | Text oder eine URL |
| **Ausgabe** | Ein QR-Code-Bild, gespeichert an einem Ort deiner Wahl |
| **Pipeline-Schritt** | Nein |

### Einen QR-Code erzeugen

1. Klicke auf **QR-Code**.
2. Tipp oder füg etwas ins Inhaltsfeld ein („QR-Code-Inhalt eingeben“) – eine URL, eine WLAN-Notiz, eine Kontaktzeile, beliebiger Text. Die Vorschau erneuert sich beim Tippen.
3. Stell die **Größe** ein – exakten Pixelwert eintippen oder mit dem Stepper anpassen.
4. Wähl die **Fehlerkorrektur**-Stufe. Höhere Stufen halten den Code scanbar, wenn er teilweise verdeckt oder klein gedruckt ist – um den Preis eines dichteren Musters.
5. Pass bei Bedarf die Farben für **Vordergrund** und **Hintergrund** an.
6. Drücke **Speichern** (⌘S).

### Tipps und Grenzen

- **Halte den Kontrast hoch.** Dunkler Vordergrund auf hellem Grund scannt am zuverlässigsten; dekorative Farbpaare können Scanner scheitern lassen.
- **Langer Inhalt braucht Luft.** Erscheint „Inhalt ist für diese Fehlerkorrekturstufe zu lang.“, kürz den Text oder senk die Fehlerkorrektur – die Kapazität schrumpft, je stärker die Korrektur.
- **Vor der Massenauflage einen Probedruck scannen.** Das Scanverhalten hängt von Druckgröße und Oberfläche ab; ein Zehn-Sekunden-Test mit dem Handy erspart den Neudruck.

## Fehlerbehebung

| Du siehst | Ursache | Lösung |
|---|---|---|
| Exportierte PDF-Seiten wirken unscharf | DPI zu niedrig für die Zielgröße | **Auflösung (DPI)** erhöhen und neu exportieren |
| „Inhalt ist für diese Fehlerkorrekturstufe zu lang.“ | Die QR-Kapazität ist bei den aktuellen Einstellungen überschritten | Inhalt kürzen oder eine niedrigere **Fehlerkorrektur**-Stufe wählen |
| Ein Handy scannt den erzeugten Code nicht | Kontrastarme Farben oder zu klein gedruckt | Dunkel-auf-hell wiederherstellen, **Größe** erhöhen, Fehlerkorrektur anheben |
| Weiterhin Probleme | — | [Issue eröffnen](https://github.com/nanguoyu/OtterPix-app/issues/new/choose) |

## Siehe auch

- [AI Texterkennung](../ai/ai-ocr.md) – Text aus Dokumenten und gescannten PDFs holen
- [Formatkonvertierung & Komprimierung](convert-and-compress.md)
- [FAQ](../faq.md)

---

**Feedback** – Fehler melden in den [Issues](https://github.com/nanguoyu/OtterPix-app/issues/new/choose), Fragen stellen in den [Discussions](https://github.com/nanguoyu/OtterPix-app/discussions).
