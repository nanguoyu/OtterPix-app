[English](../../en/tools/metadata.md) · [简体中文](../../zh-Hans/tools/metadata.md) · [繁體中文](../../zh-Hant/tools/metadata.md) · **Deutsch**

---

# Metadaten

**Metadaten** – im App Store als Metadaten-Inspektor geführt – liest, bearbeitet und entfernt die versteckten Daten in deinen Fotos: EXIF-Kameraeinstellungen, GPS-Koordinaten, IPTC-Urheberfelder und Dateidetails. Der häufigste Job ist ein einziger Schalter: den GPS-Standort entfernen, bevor ein Foto deinen Mac verlässt.

## Auf einen Blick

| | |
|---|---|
| **Verfügbarkeit** | Kostenlos |
| **Ausführung** | Auf deinem Mac – offline, nichts wird hochgeladen |
| **Eingabe** | Ein Bild oder mehrere (bei Stapeln erscheint ein Vorschaustreifen) |
| **Ausgabe** | Eine bereinigte/bearbeitete Kopie an einem Ort deiner Wahl; das Original bleibt unangetastet |
| **Pipeline-Schritt** | **Metadaten löschen** – siehe [Pipeline](../pipeline.md) |

## Die drei Modi

Das Werkzeug hat oben drei Modi: **Ansehen**, **Bearbeiten** und **Löschen**.

### Ansehen

Alles, was die Datei trägt, sauber gruppiert: Kamera (Hersteller, Modell, Objektiv), EXIF-Belichtungsdaten (Blende, Belichtungszeit, ISO, Brennweite, Aufnahmedatum), GPS (Breitengrad, Längengrad, Höhe), IPTC (Ersteller, Quelle, Bildunterschrift, Urheberrecht) und Dateidetails (Abmessungen, Farbmodell, Ausrichtung, Software).

### Bearbeiten

Einzelne Felder neu eintragen – Aufnahmedatum, Ersteller, Urheberrecht – oder den Schalter **GPS entfernen** umlegen, um nur den Standort zu löschen, während Kamera-, Datums- und Belichtungsfelder bleiben. Übernommen wird mit **Änderungen speichern …** (⌘S).

### Löschen

Metadaten im Ganzen entfernen, über die Wahl der **Voreinstellung** und dann **Löschen und speichern unter …**:

- **Datenschutz** – „Entfernt GPS, Kamera-Identität, Objektiv und Ersteller. Behält Datum, Belichtung, Ausrichtung.“ Der richtige Standard vor dem Teilen: Das Foto sortiert sich weiter korrekt nach Datum und wird richtig herum angezeigt, verrät aber nicht mehr, wo und womit es aufgenommen wurde.
- **Alle** – „Entfernt alle Metadaten. Übrig bleiben nur die Bilddaten.“

## GPS vor dem Teilen entfernen

1. Klicke in der Seitenleiste auf **Alle Funktionen**, dann auf **Metadaten**.
2. Zieh ein Foto oder mehrere hinein – bei mehreren Dateien erscheint unten ein Vorschaustreifen zum Durchblättern.
3. Prüf im Modus **Ansehen**, was tatsächlich in der Datei steckt.
4. Nur der Standort soll weg: Wechsle zu **Bearbeiten**, leg **GPS entfernen** um, drücke **Änderungen speichern …** (⌘S).
5. Für einen gründlicheren Kahlschlag: Wechsle zu **Löschen**, wähl die Voreinstellung **Datenschutz** oder **Alle** und klicke auf **Löschen und speichern unter …**.
6. Wähl, wohin die bereinigte Kopie kommt. Dein Original bleibt unverändert auf der Platte.

## Warum Metadaten entfernen

Die EXIF-Daten eines Fotos können die exakten GPS-Koordinaten des Aufnahmeorts enthalten – vor dem Veröffentlichen bewusst zu entfernen, denn E-Mail, Cloud-Speicher und direkte Datei-Uploads reichen die Originaldatei in der Regel unverändert weiter.

## Tipps und Grenzen

- **Metadaten löschen rührt keine Pixel an.** Die Operation zielt auf die versteckten Textdatensätze, nicht aufs sichtbare Bild – und die bereinigte Fassung wird als neue Kopie gespeichert, du kannst beide jederzeit vergleichen.
- **Ganze Ordner:** Füg einer [Pipeline](../pipeline.md) einen Schritt **Metadaten löschen** hinzu und bereinige einen Ordner in einem Lauf – auf Wunsch mit Skalieren und Wasserzeichen im selben Durchgang.
- **Verlass dich nicht darauf, dass Plattformen für dich strippen.** Viele soziale Netzwerke verarbeiten Uploads neu und werfen die meisten Metadaten weg, aber die Details unterscheiden sich je Dienst und ändern sich über die Zeit. Wenn das Entfernen zählt, mach es zum bewussten Schritt.

## Fehlerbehebung

| Du siehst | Ursache | Lösung |
|---|---|---|
| Die GPS-Sektion ist im Modus Ansehen leer | Das Foto hatte nie Standortdaten (oder sie wurden bereits entfernt) | Nichts zu entfernen – fertig |
| Ein bearbeitetes Feld wurde nicht übernommen | Änderungen werden beim Speichern geschrieben, nicht live | **Änderungen speichern …** (⌘S) drücken und die gespeicherte Kopie prüfen |
| Die Datumssortierung stimmt nach dem Löschen nicht mehr | Die Voreinstellung **Alle** entfernt auch das Aufnahmedatum | Die Voreinstellung **Datenschutz** nutzen – sie behält Datum, Belichtung und Ausrichtung |
| Weiterhin Probleme | — | [Issue eröffnen](https://github.com/nanguoyu/OtterPix-app/issues/new/choose) |

## Siehe auch

- [FAQ – Datenschutz & Netzwerk](../faq.md#datenschutz--netzwerk)
- [Pipeline](../pipeline.md) – Metadaten löschen als Stapel-Schritt
- [Stapelumbenennung](batch-rename.md) – nutzt dieselben EXIF-Felder als Umbenennungs-Token

---

**Feedback** – Fehler melden in den [Issues](https://github.com/nanguoyu/OtterPix-app/issues/new/choose), Fragen stellen in den [Discussions](https://github.com/nanguoyu/OtterPix-app/discussions).
