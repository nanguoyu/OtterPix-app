[English](../../en/tools/resize-crop-rotate.md) | [简体中文](../../zh-Hans/tools/resize-crop-rotate.md) | [繁體中文](../../zh-Hant/tools/resize-crop-rotate.md) | **Deutsch**

---

# Größe ändern, Zuschneiden & Drehung

Das Geometrie-Trio: **Größe ändern** skaliert Bilder prozentual oder auf exakte Abmessungen, **Zuschneiden** beschneidet sie mit freiem oder festem Seitenverhältnis, und **Drehung** dreht und spiegelt in beliebigem Winkel. Alle drei sind kostenlos, und alle drei existieren als [Pipeline](../pipeline.md)-Schritte für die Stapelverarbeitung.

## Auf einen Blick

| | |
|---|---|
| **Verfügbarkeit** | Kostenlos |
| **Ausführung** | Auf deinem Mac – offline, nichts wird hochgeladen |
| **Eingabe** | Ein Bild oder ein Stapel |
| **Ausgabe** | Verarbeitete Kopien an einem Zielort deiner Wahl |
| **Pipeline-Schritte** | **Größe ändern**, **Zuschneiden**, **Drehen** – siehe [Pipeline](../pipeline.md) |

## Größe ändern

1. Klicke auf **Größe ändern** und leg deine Bilder ab.
2. Wähl, wie skaliert wird: prozentual, oder auf exakte Pixelmaße in den Feldern **Breite** und **Höhe**. Werte kannst du direkt eintippen oder mit dem Stepper anpassen.
3. Das Kettenglied-Symbol zwischen den Feldern schaltet **Seitenverhältnis sperren** um – gesperrt rechnet die App beim Ändern eines Felds das andere nach; entsperrt bewegen sich beide unabhängig (und das Bild kann sich verzerren).
4. Drücke **Speichern** (⌘S).

### Optionen

- **Prozentual** – schnelles proportionales Skalieren, z. B. 50 % für die Web-Ausgabe.
- **Exakte Abmessungen** – **Breite** / **Höhe** in Pixeln, **Seitenverhältnis sperren** ist standardmäßig aktiv.
- **Einpassen in** – der stapelfreundliche Rahmen-Modus. In den Worten der App: „Jedes Bild wird unter Wahrung des Seitenverhältnisses in diese Box eingepasst; bereits kleinere Bilder bleiben unverändert.“ Ideal, wenn ein Ordner gemischter Hoch- und Querformate am Ende nirgends größer als etwa 1920 px sein soll.

## Zuschneiden

1. Klicke auf **Zuschneiden** und leg ein Bild ab.
2. Zieh die Ecken- und Kantengriffe des Zuschneide-Rahmens, oder wähl ein festes Seitenverhältnis – **Frei** und **Original** sind immer verfügbar, dazu die gängigen festen Verhältnisse.
3. Ein schwebendes Badge beziffert den Zuschnitt beim Ziehen: die Originalgröße („Original 4032 × 3024 px“) und der gewählte Anteil („42 % ausgewählt“) – so triffst du präzise Ausschnitte, statt nach Augenmaß zu arbeiten.
4. Drücke **Speichern** (⌘S).

### Optionen

- **Seitenverhältnis** – **Frei** für beliebige Zuschnitte; **Original** behält die Proportionen der Quelle; feste Verhältnisse für Cover, Avatare und Thumbnails.
- **Ausrichtung** (Pipeline-Schritt) – der Stapel-Zuschneideschritt schneidet relativ zu einem Anker: **Mitte**, **Oben links**, **Oben rechts**, **Unten links**, **Unten rechts**.

## Drehung

1. Klicke auf **Drehung** und leg deine Bilder ab.
2. Nutz **Links 90°** / **Rechts 90°** für die üblichen Vierteldrehungen, die Spiegeln-Tasten für horizontales oder vertikales Spiegeln, oder zieh den Winkelregler für freie Drehungen – die Beschriftung zeigt den aktuellen Wert („Winkel: 12°“).
3. Freie Winkel vergrößern die Leinwand, damit das gedrehte Bild hineinpasst; die Vorschau zeigt den entstehenden Rahmen und seine Pixelgröße vor dem Speichern.
4. Drücke **Speichern** (⌘S).

## Tipps und Grenzen

- **Größe ändern erfindet keine Details.** *Hochskalieren* mit diesem Werkzeug interpoliert nur Pixel. Um ein Foto zu vergrößern und dabei plausible Details zu ergänzen, nimm stattdessen [KI-Upscale](../ai/ai-upscale.md).
- **In der Pipeline zählt die Reihenfolge.** Setz **Zuschneiden** und **Größe ändern** vor **Wasserzeichen** – die App warnt, wenn ein Wasserzeichen-Schritt davor steht, weil es sonst abgeschnitten oder unscharf werden kann.
- **Sperr das Seitenverhältnis, außer du willst es anders.** Ein entsperrtes Skalieren auf beliebige Breite × Höhe verzerrt das Bild. Das Kettenglied-Symbol zeigt den aktuellen Zustand auf einen Blick.

## Fehlerbehebung

| Du siehst | Ursache | Lösung |
|---|---|---|
| Das skalierte Bild wirkt verzerrt | **Seitenverhältnis sperren** war aus und beide Felder wurden geändert | Sperre aktivieren und eine Dimension neu eingeben |
| Das vergrößerte Bild wirkt weich | Größe ändern interpoliert; Details kann es nicht ergänzen | Zum Vergrößern [KI-Upscale](../ai/ai-upscale.md) verwenden |
| Das gedrehte Bild hat zusätzliche leere Flächen | Freie Drehung vergrößert die Leinwand, damit der gedrehte Rahmen hineinpasst | Erwartet – danach zuschneiden, wenn der Rahmen eng sitzen soll |
| Weiterhin Probleme | — | [Issue eröffnen](https://github.com/nanguoyu/OtterPix-app/issues/new/choose) |

## Siehe auch

- [Pipeline](../pipeline.md) – Größe ändern, Drehen und Zuschneiden als Stapel-Schritte
- [KI-Upscale](../ai/ai-upscale.md) – Vergrößern mit Detailrekonstruktion
- [Formatkonvertierung & Komprimierung](convert-and-compress.md)

---

**Feedback** – Fehler melden in den [Issues](https://github.com/nanguoyu/OtterPix-app/issues/new/choose), Fragen stellen in den [Discussions](https://github.com/nanguoyu/OtterPix-app/discussions).
