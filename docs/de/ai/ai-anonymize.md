[English](../../en/ai/ai-anonymize.md) · [简体中文](../../zh-Hans/ai/ai-anonymize.md) · [繁體中文](../../zh-Hant/ai/ai-anonymize.md) · **Deutsch**

---

# AI Anonymisieren

**AI Anonymisieren** erkennt die Personen und Fahrzeuge in einem Foto und verwischt oder verpixelt sie – Gesichter und Kennzeichen in einem Durchgang abgedeckt – während du bestimmst, wer und was scharf bleibt.

![Das OtterPix-Werkzeug AI Anonymisieren auf macOS: erkannte Personen mit nummerierten Rahmen im Eingabe-Bereich, das verwischte Ergebnis im Ausgabe-Bereich.](../../../assets/de/aiAnonymize.webp)

## Auf einen Blick

| | |
|---|---|
| **Verfügbarkeit** | Pro – im Gratis-Plan eine Gratis-Nutzung pro Tag |
| **Ausführung** | Auf dem Gerät; nach dem einmaligen Modell-Download offline (~138 MB) |
| **Eingabe** | Ein Bild |
| **Ausgabe** | Das Foto mit den gewählten Erkennungen verwischt oder verpixelt |
| **Pipeline-Schritt** | Nein – wer scharf bleibt, entscheidest du interaktiv |

Alles läuft lokal auf deinem Mac. Bilder werden nie hochgeladen – die App nutzt das Netz nur für die Modell-Downloads, die du selbst anstößt, und die Kaufbestätigung über den App Store.

## So anonymisierst du ein Foto

1. Öffne OtterPix und klicke im KI-Bereich des Werkzeugrasters auf **AI Anonymisieren**.
2. Leg dein Foto im Bereich **Eingabe** ab.
3. Klicke auf **Anonymisieren**. Die lokale KI findet die Personen und Fahrzeuge im Bild, nummeriert jede Erkennung und zeigt das verwischte Ergebnis im Bereich **Ausgabe**.
4. Wähl eine **Methode**: **Verwischen** für einen weichen, fotografischen Look, oder **Mosaik** für die klassische Verpixelung. Die Regler **Stärke** und **Radius** steuern, wie kräftig der Effekt ausfällt.
5. Klicke auf ein nummeriertes Feld in der Eingabe, um diese Person oder dieses Fahrzeug auszunehmen – die Ausgabe baut sich sofort neu auf, ohne neuen KI-Lauf. Ein weiterer Klick verwischt wieder. Der Overlay-Hinweis sagt es so: „Tippe ein Feld an, um einzelne Objekte vom Verwischen auszunehmen.“
6. Klicke auf **Speichern** (⌘S) und wähl, wohin die anonymisierte Kopie kommt. Deine Originaldatei bleibt unangetastet.

## Optionen

### Methode, Stärke, Radius

**Verwischen** hält das Bild ruhig und fotografisch; **Mosaik** ist unverkennbar absichtlich – das passt zu Kennzeichen und allem Dokumentartigen. Wofür du dich auch entscheidest: Stell die Stärke hoch genug ein, dass Person oder Kennzeichen wirklich nicht mehr erkennbar sind – Anpassungen bauen sofort neu auf, Feintuning kostet also nichts.

### Ziele

Die Chip-Zeile **Ziele:** schaltet ganze Klassen auf einmal – Personen an, Fahrzeuge aus, oder umgekehrt. **Weitere Ziele …** öffnet die volle Auswahl, gegliedert in acht Gruppen: **Personen**, **Fahrzeuge**, **Tiere**, **Außenbereich**, **Accessoires**, **Sport**, **Elektronik**, **Innenbereich** – so lassen sich auch Laptops, Rucksäcke oder Haustiere verwischen, wenn ein Foto das verlangt.

### Kontrolle pro Erkennung

Klassen-Chips setzen die Regel; Klicks auf nummerierte Felder machen die Ausnahmen. „Alle außer mir“ oder „jedes Auto außer meinem“ dauert Sekunden: alles erkennen lassen, dann das eigene Feld anklicken und ausnehmen.

## Tipps und Grenzen

- **Auf vollen Fotos präzise klicken.** Bei sich überlappenden Personen ordnet OtterPix deinen Klick der Person zu, die tatsächlich unter dem Cursor liegt – klick die Person an, nicht nur in ihre Nähe.
- **Verwischt wird die ganze Erkennung.** Eine verwischte Person schließt ihr Gesicht ein; ein verwischtes Fahrzeug sein Kennzeichen.
- **Vor dem Veröffentlichen prüfen.** Die Erkennung ist ein starker erster Durchgang, kein Urteil – sehr kleine, angeschnittene oder stark verdeckte Motive können durchrutschen. Für einen übrig gebliebenen Rest ist der [KI-Radierer](ai-eraser.md) das Partnerwerkzeug: übermalen und ganz entfernen.
- **Nur Standbilder.** AI Anonymisieren arbeitet auf Bildern, nicht auf Video. Für einen Clip exportierst du die Frames, die du veröffentlichen willst, und anonymisierst diese.
- **Die Anzeige bestätigt die Abdeckung** – „3 Region(en) verwischt“ nennt exakt, wie viele Erkennungen betroffen waren.

## Fehlerbehebung

| Du siehst | Ursache | Lösung |
|---|---|---|
| „Wähle mindestens eine Klasse zum Verwischen aus.“ | Alle Zielklassen sind abgeschaltet | Eine Klasse in der Zeile **Ziele:** wieder aktivieren (oder über **Weitere Ziele …**) |
| Ein Hinweis, dass das Modell fehlt | Das Erkennungsmodell (~138 MB) liegt nicht auf der Platte | Im Fehler auf **Einstellungen öffnen** klicken und es laden (auch unter **Einstellungen → KI**) |
| „Gratis-Nutzung dieses Werkzeugs heute aufgebraucht“ | „Jedes KI-Werkzeug hat täglich eine Gratis-Nutzung – diese wird um Mitternacht zurückgesetzt.“ | Auf den Reset warten oder upgraden. Das heutige Foto bleibt frei nachjustierbar |
| Eine Person oder ein Kennzeichen wurde nicht erkannt | Zu klein, am Rand angeschnitten oder stark verdeckt | Nichts ausnehmen und noch einmal prüfen; Reste mit dem [KI-Radierer](ai-eraser.md) beseitigen |
| Der erste Lauf ist langsamer als spätere | Das Modell wird einmal pro Sitzung geladen | Folgende Läufe sind schneller |
| Weiterhin Probleme | — | [Issue eröffnen](https://github.com/nanguoyu/OtterPix-app/issues/new/choose) |

## Siehe auch

- [KI-Radierer](ai-eraser.md) – ein Motiv entfernen statt verwischen
- [Metadaten](../tools/metadata.md) – vor dem Teilen auch GPS entfernen
- [FAQ – Datenschutz & Netzwerk](../faq.md#datenschutz--netzwerk)

---

**Feedback** – Fehler melden in den [Issues](https://github.com/nanguoyu/OtterPix-app/issues/new/choose), Fragen stellen in den [Discussions](https://github.com/nanguoyu/OtterPix-app/discussions).
