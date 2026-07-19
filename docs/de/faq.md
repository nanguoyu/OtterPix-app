[English](../en/faq.md) · [简体中文](../zh-Hans/faq.md) · [繁體中文](../zh-Hant/faq.md) · **Deutsch**

---

# FAQ

## Über OtterPix

### Was ist OtterPix?

Ein Bild-Werkzeugkasten für den Mac: zehn Ein-Klick-Basiswerkzeuge (Konvertieren, Komprimieren, Größe ändern, Zuschneiden, Drehen, Wasserzeichen, Umbenennen, Metadaten, PDF zu Bild, QR-Code), eine visuelle [Pipeline](pipeline.md) für Stapel-Workflows und sieben lokale KI-Funktionen. Alles läuft lokal auf Apple Silicon – keine Konten, keine Uploads.

### Ist OtterPix Open Source?

Nein. OtterPix ist eine kommerzielle Closed-Source-App aus dem Mac App Store – dieses Repository enthält keinen Quellcode, und das ist auch nicht geplant. Stattdessen ist es das öffentliche Zuhause der App: Handbücher, Versionshinweise und der Bug-Tracker.

### Welche Sprachen spricht OtterPix?

Die Oberfläche der App gibt es in 18 Sprachen. Die Handbücher in diesem Repository werden in vier gepflegt: English, 简体中文, 繁體中文 und Deutsch. Falsche oder holprige Übersetzungen in einer der 18 Sprachen sind ein [Issue](https://github.com/nanguoyu/OtterPix-app/issues/new/choose) wert – Korrekturen von Muttersprachlern landen regelmäßig im nächsten Release.

### Was setzt OtterPix voraus?

macOS 14 (Sonoma) oder neuer auf einem Mac mit Apple Silicon (M1 oder neuer). Intel-Macs werden nicht unterstützt. Für die KI-Bilderzeugung sind 16 GB RAM oder mehr empfohlen.

## Formate & Dateien

### Welche Formate liest und schreibt OtterPix?

Lesen und Schreiben: JPEG, PNG, TIFF, BMP, HEIC, WebP, AVIF – dazu eine Sektion **Andere Formate** im Format-Picker für die selteneren Formate, die dein Mac schreiben kann. Gelesen wird noch deutlich mehr: Die Ablagezone auf **Start** nennt PNG · JPEG · HEIC · TIFF · WebP · GIF +51. PDFs rendert das Werkzeug [PDF zu Bild](tools/pdf-and-qr.md) in beliebiger DPI zu Bildern.

### Bleiben Farbprofile und die EXIF-Orientierung erhalten?

Die meisten Operationen erhalten Farbprofile und EXIF-Orientierung. Metadaten entfernt nur, was genau dafür gebaut ist: die Löschen-Funktion des [Metadaten](tools/metadata.md)-Werkzeugs und der Pipeline-Schritt **Metadaten löschen**.

### Verändert OtterPix meine Originaldateien?

Kein Werkzeug überschreibt Originale. Gespeichert wird immer als Kopie an einen Ort deiner Wahl; auch die Stapelumbenennung schreibt in einen Ordner, den du auswählst, und lässt die Originale liegen – außer du aktivierst ausdrücklich **Originale in den Papierkorb**.

## Datenschutz & Netzwerk

### Lädt OtterPix meine Bilder hoch?

Nein. Jede Operation – einschließlich aller KI-Funktionen – läuft lokal auf deinem Mac. Die App enthält kein Analytics-SDK, keine Telemetrie und keinen Bild-Upload. Sie läuft in der macOS-Sandbox, und ihre Netzwerkberechtigungen decken genau zwei Dinge ab: den Download der KI-Modelldateien bei der ersten Nutzung einer KI-Funktion und die App-Store-Kaufbestätigung. Alle Details in der [Datenschutzerklärung](https://otterpix.app/de/privacy).

### Funktioniert OtterPix offline?

Ja. Die Basiswerkzeuge arbeiten ab dem ersten Start offline. Jede KI-Funktion braucht einen einzigen Online-Moment – ihren ersten Modell-Download – und läuft danach dauerhaft offline.

### Wie entferne ich GPS-Daten aus Fotos, bevor ich sie teile?

Mit dem [Metadaten](tools/metadata.md)-Werkzeug: Der Schalter **GPS entfernen** löscht nur den Standort; die Voreinstellung **Datenschutz** entfernt GPS plus Kamera-Identität, Objektiv und Ersteller und behält Datum, Belichtung und Ausrichtung.

## KI-Modelle

### Warum will eine KI-Funktion etwas herunterladen?

Hinter jeder KI-Funktion steht ein Modell, das getrennt von der App ausgeliefert wird, damit der App-Download klein bleibt. Beim ersten Lauf einer Funktion lädt sie ihr Modell; danach arbeitet die Funktion vollständig offline. Die Größen reichen von wenigen Megabyte (kleinstes Upscale-Modell) bis zu mehreren Gigabyte (Bilderzeugung).

### Wo verwalte ich die Modelle?

Unter **Einstellungen → KI**. Jedes Modell lässt sich dort herunterladen, erneut laden oder löschen – Löschen gibt Speicherplatz frei, und die Funktion fragt beim nächsten Mal einfach wieder nach dem Download.

### Kosten die Modelle etwas?

Nein. Modell-Downloads sind für jede Funktion kostenlos, auch für die Pro-Werkzeuge.

## Kostenlos & Pro

### Was genau ist kostenlos?

Alle zehn Basiswerkzeuge, die Pipeline, die KI-Texterkennung und die KI-Bilderzeugung – dauerhaft, nicht als Testphase. Zusätzlich enthält jedes der fünf Pro-KI-Werkzeuge (KI-Upscale, KI Freistellen, KI-Radierer, AI Anonymisieren, KI-Wiederherstellung) eine Gratis-Nutzung pro Tag.

### Wie funktioniert die tägliche Gratis-Nutzung?

Jede Pro-KI-Karte trägt ein bernsteinfarbenes **Heute gratis**-Abzeichen, solange ihre Gratis-Nutzung verfügbar ist. Nach einem erfolgreichen Lauf meldet das Banner: „Gratis-Nutzung dieses Werkzeugs heute aufgebraucht“ – „Jedes KI-Werkzeug hat täglich eine Gratis-Nutzung – diese wird um Mitternacht zurückgesetzt.“ Gezählt wird pro geladenem Foto, nicht pro Klick: Dasselbe Foto kannst du innerhalb dieser einen Nutzung den ganzen Tag neu berechnen, verfeinern und anpassen – und auch ein Foto, auf dem die heutige Nutzung bereits lief, bleibt beim erneuten Öffnen frei bearbeitbar.

### Welche Grenzen hat der Gratis-Plan in der Pipeline?

„Gratis: ein Bild pro Pipeline mit Pro-Schritt. Upgrade für Stapel.“ – ein Pro-Schritt pro Pipeline, ein einzelnes Bild, solange der Pro-Schritt enthalten ist, und sein Lauf verbraucht die tägliche Gratis-Nutzung des jeweiligen Werkzeugs. Details im [Pipeline-Handbuch](pipeline.md#grenzen-im-gratis-plan).

### Was kostet Pro, und wie verwalte ich es?

Pro gibt es als Monatsabo, Jahresabo oder einmaligen Lifetime-Kauf – aktuelle Preise stehen im [Mac App Store](https://apps.apple.com/app/id6772468615). Abos verwaltest und kündigst du in deinen [Apple-Account-Abos](https://apps.apple.com/account/subscriptions). Der Lifetime-Kauf ist eine Einmalzahlung: Nichts verlängert sich, und es gibt kein Abo zu verwalten.

### Wie funktionieren Rückerstattungen?

Alle Käufe wickelt Apple ab; Rückerstattungen laufen deshalb über Apple unter [reportaproblem.apple.com](https://reportaproblem.apple.com). Der Entwickler sieht deine Zahlungsdaten nicht und kann selbst keine Rückerstattungen ausstellen.

## Regionale Verfügbarkeit & Support

### Ist jede Funktion in jedem Land verfügbar?

In der über den Mac App Store für Festlandchina vertriebenen Version von OtterPix sind KI-Bilderzeugung und KI-Texterkennung nicht verfügbar. Alle anderen Funktionen – einschließlich der fünf Pro-KI-Werkzeuge – sind in jeder Region verfügbar, in der OtterPix erscheint. Details in den [Nutzungsbedingungen](https://otterpix.app/de/terms).

### Wo melde ich einen Fehler oder stelle eine Frage?

Fehler → [Issue eröffnen](https://github.com/nanguoyu/OtterPix-app/issues/new/choose). Fragen → [Discussions → Q&A](https://github.com/nanguoyu/OtterPix-app/discussions/categories/q-a). English, 中文 und Deutsch sind gleichermaßen willkommen. Für Privates oder Sensibles: hello@otterpix.app.

## Siehe auch

- [Erste Schritte](getting-started.md)
- [Pipeline](pipeline.md)
- [Changelog](changelog.md)

---

**Feedback** – Fehler melden in den [Issues](https://github.com/nanguoyu/OtterPix-app/issues/new/choose), Fragen stellen in den [Discussions](https://github.com/nanguoyu/OtterPix-app/discussions).
