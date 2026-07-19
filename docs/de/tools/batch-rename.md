[English](../../en/tools/batch-rename.md) · [简体中文](../../zh-Hans/tools/batch-rename.md) · [繁體中文](../../zh-Hant/tools/batch-rename.md) · **Deutsch**

---

# Stapelumbenennung

**Stapelumbenennung** benennt viele Bilddateien auf einmal um – mit einem Vorlagensystem für fortlaufende Nummern, EXIF-Aufnahmedaten und Kameranamen – und zeigt eine vollständige Vorschau, bevor irgendetwas geschrieben wird.

## Auf einen Blick

| | |
|---|---|
| **Verfügbarkeit** | Kostenlos |
| **Ausführung** | Auf deinem Mac – offline, nichts wird hochgeladen |
| **Eingabe** | Beliebig viele Bilddateien |
| **Ausgabe** | Umbenannte Kopien in einem Ordner deiner Wahl; Originale bleiben liegen, außer du entscheidest dich fürs Verschieben in den Papierkorb |
| **Pipeline-Schritt** | Nein – Umbenennen ist ein eigenes Werkzeug |

## Einen Stapel umbenennen

1. Klicke auf **Stapelumbenennung** und zieh deine Dateien hinein, oder nutz **Dateien hinzufügen …**.
2. Leg die Reihenfolge mit **Sortierung** fest – **Name**, **EXIF-Datum** oder **Änderungsdatum**. Die Reihenfolge bestimmt die Zählerfolge.
3. Bau das Namensmuster im Feld **Vorlage**. Darunter sitzen die Token-Chips – „Token zum Einfügen antippen“. Die Standardvorlage ist `{name}_{counter:03}.{ext}`.
4. Beobachte die Spalte **Vorschau**: Jeder neue Dateiname erscheint live, und Konflikte werden vor dem Ausführen markiert („2 Konflikt(e)“).
5. Verfeinere bei Bedarf mit **Suchen & Ersetzen** und **Groß/Klein** (siehe Optionen).
6. Drücke **Speichern** (⌘S), dann **Ordner wählen**. Die App erklärt es selbst: „Wähle, wo OtterPix die umbenannten Dateien speichern soll. Originale bleiben an ihrem Platz, sofern ‚Originale in den Papierkorb verschieben‘ nicht aktiviert ist.“

## Vorlagen-Token

| Token | Ergibt |
|---|---|
| `{name}` | Der ursprüngliche Dateiname ohne Endung |
| `{ext}` | Die ursprüngliche Endung (`jpg`, `png`, …) |
| `{counter}` | Eine fortlaufende Nummer; **Zähler ab** und **Schritt** sind einstellbar |
| `{counter:03}` | Der Zähler mit führenden Nullen auf feste Breite – `001`, `002`, … |
| `{date}` | Das EXIF-Aufnahmedatum (fällt aufs Änderungsdatum der Datei zurück, wenn das Foto keins hat) |
| `{date:yyyy-MM-dd}` | Das Aufnahmedatum in einem eigenen Format |
| `{mdate}` | Das Änderungsdatum der Datei; eigene Formate funktionieren genauso |
| `{exif:camera}` | Hersteller und Modell der Kamera aus den EXIF-Daten |

Beispiel: `{date:yyyy-MM-dd}_{exif:camera}_{counter:03}.{ext}` → `2026-05-14_Apple iPhone 15 Pro_001.heic`.

## Optionen

### Suchen & Ersetzen

Ein **Suchen**/**Ersetzen**-Paar, das nach der Vorlage greift, mit einem Schalter **Regulärer Ausdruck** für musterbasierte Änderungen – ein Präfix entfernen, Trennzeichen tauschen, Leerzeichen zusammenfassen.

### Groß/Klein

Normalisiert den endgültigen Namen: **Beibehalten**, **klein**, **GROSS** oder **Anfangsbuchstaben**.

### Originale in den Papierkorb

Standardmäßig aus. Ist die Option an, wandern die Originale in den macOS-Papierkorb, *nachdem* alle Dateien im gewählten Ordner gespeichert wurden – bei Bedarf aus dem Papierkorb wiederherstellbar. Näher kommt das Werkzeug einem Umbenennen „an Ort und Stelle“ nicht; standardmäßig rührt es deine Quelldateien nie an.

## Tipps und Grenzen

- **Die Vorschau ist der Vertrag.** Geschrieben wird erst beim Speichern, und Konflikte (zwei Dateien mit demselben Zielnamen oder ein Name, den es auf der Platte schon gibt) erscheinen zuerst in der Vorschau.
- **`{date}` braucht EXIF.** Screenshots und exportierte Grafiken tragen oft kein Aufnahmedatum; dann fällt `{date}` aufs Änderungsdatum zurück. Die Sortierung nach **EXIF-Datum** ergibt nur bei Kamerafotos Sinn.
- **Bilder aus der Zwischenablage lassen sich nicht umbenennen.** Einfügen braucht eine echte Datei: „Die Zwischenablage enthält Bilddaten, keine Datei — bitte zuerst als Datei sichern.“

## Fehlerbehebung

| Du siehst | Ursache | Lösung |
|---|---|---|
| „2 Konflikt(e)“ in der Vorschau | Zwei Eingaben ergeben identische Namen, oder ein Zielname existiert bereits | `{counter}` in die Vorlage aufnehmen oder das Muster ändern, bis die Vorschau konfliktfrei ist |
| `{date}` liefert das heutige Datum statt des Fotodatums | Die Datei hat kein EXIF-Aufnahmedatum | Erwarteter Rückfall aufs Änderungsdatum – prüf die Datei im [Metadaten](metadata.md)-Werkzeug |
| Dateien gespeichert, aber die Originale sind noch da | Standardverhalten – Originale werden nie entfernt, außer du entscheidest dich dafür | **Originale in den Papierkorb** aktivieren, wenn du das willst |
| Weiterhin Probleme | — | [Issue eröffnen](https://github.com/nanguoyu/OtterPix-app/issues/new/choose) |

## Siehe auch

- [Metadaten](metadata.md) – die EXIF-Felder ansehen, die die Token auslesen
- [Pipeline](../pipeline.md) – zum Verarbeiten (statt Umbenennen) ganzer Ordner
- [FAQ](../faq.md)

---

**Feedback** – Fehler melden in den [Issues](https://github.com/nanguoyu/OtterPix-app/issues/new/choose), Fragen stellen in den [Discussions](https://github.com/nanguoyu/OtterPix-app/discussions).
