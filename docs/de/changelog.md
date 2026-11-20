[English](../../CHANGELOG.md) | [简体中文](../zh-Hans/changelog.md) | [繁體中文](../zh-Hant/changelog.md) | **Deutsch**

---

# Changelog

Versionshinweise, wie im [Mac App Store](https://apps.apple.com/app/id6772468615) veröffentlicht.

## 1.3.2 (November 2026)

- Fotos behalten Aufnahmedatum, Kameradaten, Ort und Urheberrecht, wenn du sie komprimierst, konvertierst, skalierst, zuschneidest, drehst oder mit einem Wasserzeichen versiehst.
- „AI Bilderzeugung“: Das standardmäßige 8-Bit-Modell wird jetzt vollständig installiert, und unterbrochene Downloads laufen dort weiter, wo sie unterbrochen wurden.
- „AI Anonymisieren“ verdeckt Inhalte auch in sehr großen Fotos genauso zuverlässig, „Volltonfarbe“ ist standardmäßig vollständig deckend, und Objektnamen erscheinen in deiner Sprache. Gespeicherte Bilder enthalten keine Standortdaten und keine identifizierenden Angaben.
- „AI Texterkennung“ behält bereits gelesene Seiten, wenn du stoppst oder eine Seite fehlschlägt, liest gedrehte PDF-Seiten vollständig und weist auf passwortgeschützte PDFs hin.
- Die „Ordner-Automatisierung“ verarbeitet Dateien nach einem vorübergehenden Problem erneut, stoppt beim Pausieren nach der aktuellen Datei und macht weiter, sobald ein externes Laufwerk wieder angeschlossen ist. Kurzbefehle und AppleScript melden Fehler verständlicher, und AppleScript erhält den Befehl „stop“.
- Bilder sind nach dem Drehen, Zuschneiden und Konvertieren richtig ausgerichtet und haben exakt die richtige Größe, „AI Upscale“ und „AI Radierer“ erhalten die Transparenz, und für zu große Bilder gibt es eine klare Meldung.

## 1.3.1 (September 2026)

- „AI Anonymisieren“ bietet drei neue Stile: Hex-Mosaik, Volltonfarbe (mit frei wählbarer Farbe und Deckkraft) und Regenbogenblöcke.
- Änderungen an Künstler, Urheberrecht, Beschreibung und Aufnahmedatum unter „Metadaten“ werden jetzt zuverlässig gespeichert, auch unter macOS 27. „Metadaten“ zeigt außerdem den IPTC-Ersteller an.
- Die Voreinstellung „Datenschutz“ von „Metadaten löschen“ entfernt jetzt auch den Kamerabesitzer, die Seriennummer des Objektivs sowie die in IPTC gespeicherten Angaben zu Ersteller, Kontakt, Urheberrecht und Ort.
- Lässt sich ein Modell nicht löschen, zeigen die Einstellungen jetzt den Grund an.
- „AI Bilderzeugung“ zeigt jetzt für jedes Modell die korrekte Downloadgröße an.

## 1.3.0 (August 2026)

- Alle AI-Arbeitsbereiche wurden mit klareren, anpassungsfähigen Bedienelementen und vollständigen Modell- und Qualitätshinweisen neu gestaltet.
- Modelldownloads zeigen auf Funktionsseiten und in den Einstellungen denselben Fortschritt und lassen sich pausieren, fortsetzen oder abbrechen; Teildownloads werden zuverlässig weitergeführt.
- Bei der AI Bilderzeugung stehen Modell und Präzision jetzt direkt beim Prompt, und alle benötigten Komponenten werden vor der Erzeugung vollständig geladen.
- Die Ersteinrichtung, der Wechsel der Downloadquelle und die Speicheranzeige für Modelle wurden zuverlässiger.

## 1.2.3 (Juli 2026)

- Werkzeugkarten lassen sich wieder in die Verarbeitungspipeline ziehen.
- Im Menü „Schritt hinzufügen“ werden die Namen der Operationen jetzt korrekt in der ausgewählten App-Sprache angezeigt.

## 1.2.2 (Juli 2026)

- Das neue OtterPix-Symbol in der Menüleiste hält deine Abläufe griffbereit. Lege Bilder oder Ordner darauf ab, um sie an die Pipeline zu senden, und öffne das Hauptfenster mit einem Klick erneut. Wenn das Symbol aktiviert ist, bleibt OtterPix nach dem Schließen des Hauptfensters über die Menüleiste erreichbar.
- Neu in Pro: Die Ordnerautomatisierung überwacht ausgewählte Ordner und wendet auf neue Bilder automatisch eine gespeicherte Pipeline-Vorlage an.
- Führe unterstützte Werkzeuge und gespeicherte Vorlagen über Kurzbefehle und AppleScript aus. Die Bildverarbeitung bleibt auf deinem Mac.
- AI-Werkzeuge prüfen vor dem Laden von Modellen die Hardwarekompatibilität und erklären verständlich, wann die native Ausführung auf einem Mac mit Apple Chip erforderlich ist. Außerdem verbessert dieses Update die Zuverlässigkeit beim Start über die Menüleiste, bei Ordnerberechtigungen und der Fensterverwaltung sowie bei Bedienungshilfen und Lokalisierung.

## 1.2.1 (Juli 2026)

- Verbesserungen bei Stabilität und Feinschliff in der ganzen App.

## 1.2.0 (Juli 2026)

- OtterPix spricht jetzt 18 Sprachen — neu hinzugekommen sind Traditionelles Chinesisch, Japanisch, Koreanisch, Thai, Vietnamesisch, Französisch, Italienisch, Spanisch, brasilianisches Portugiesisch, Schwedisch, Finnisch, Norwegisch, Türkisch, Russisch und Ukrainisch. Jedes Menü, jedes Werkzeug und jede Meldung ist vollständig lokalisiert.
- Dazu Verbesserungen bei Stabilität und Feinschliff.

## 1.1.4 (Juli 2026)

- AI Texterkennung: originalgetreuere Ausgabe — einzeilige Überschriften über Abbildungen bleiben erhalten, verbundene Tabellenzellen werden korrekt ausgerichtet, reine Abbildungsseiten gelten nicht mehr fälschlich als leer. Kopieren aus der gerenderten Ansicht fügt jetzt ein eigenständiges Dokument samt Abbildungen ein.
- Der Speicherverbrauch sinkt nach AI-Läufen wieder — beim Verlassen der Seite und direkt nach Abschluss.
- Gratis-Kontingent: Ein Foto, das die heutige Gratis-Nutzung bereits verbraucht hat, bleibt nach einem Wechsel weiter kostenlos bearbeitbar.
- Fehlt ein Modell, bietet jede AI-Funktion jetzt direkt „Einstellungen öffnen“ an.
- ⌘S funktioniert überall, Downloads werden vor dem Speichern geprüft, Abbrechen erscheint nicht mehr als Fehler, und diverse Feinheiten (Dark Mode, deutsche Texte) wurden poliert.

## 1.0 – 1.1.3 (2026)

Frühere Versionshinweise wurden nicht archiviert. Die aktuelle Version findest du im [Mac App Store](https://apps.apple.com/app/id6772468615).

---

Hinweis: AI Bilderzeugung und AI Texterkennung sind im Mac App Store für Festlandchina nicht verfügbar.
