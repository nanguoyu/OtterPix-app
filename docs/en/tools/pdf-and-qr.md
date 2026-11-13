**English** | [简体中文](../../zh-Hans/tools/pdf-and-qr.md) | [繁體中文](../../zh-Hant/tools/pdf-and-qr.md) | [Deutsch](../../de/tools/pdf-and-qr.md)

---

# PDF to Image & QR Code

Two small, sharp utilities: **PDF to Image** renders PDF pages into image files at the resolution you choose, and **QR Code** generates QR codes from text or URLs.

## PDF to Image

### At a glance

| | |
|---|---|
| **Availability** | Free |
| **Runs** | On your Mac — offline, nothing uploaded |
| **Input** | A PDF ("Select or drag a PDF file here"; pasting with ⌘V works too) |
| **Output** | One image file per page, in a destination you choose |
| **Pipeline step** | No |

### How to convert PDF pages

1. Click **PDF to Image** and drop in a PDF. The tool shows the page count ("12-page PDF") with a page-by-page preview.
2. Choose which pages to convert: all of them ("All pages (12)") or a **Range** with **From** / **To** bounds — type an exact page number or nudge with the steppers.
3. Set **Resolution (DPI)**. Higher DPI means larger, sharper images — for on-screen use a modest value is plenty; for print or zoom-in reading go higher.
4. Pick the output format — PNG for crisp text and graphics, JPEG for smaller photographic pages.
5. Click **Convert & Save Page 3** (single page) or **Convert & Save 12 Pages** (range) and choose the destination. **Select another PDF** swaps documents without leaving the tool.

### Tips and limits

- **PDFs render at any DPI** — the source is vector where possible, so raising the DPI genuinely adds sharpness rather than just scaling pixels.
- **One file per page.** A range export writes numbered images, ready for slides or web embedding.
- **Extracting *text* from a scanned PDF is a different job** — that's [AI OCR](../ai/ai-ocr.md), which turns documents and scans into Markdown.

## QR Code

### At a glance

| | |
|---|---|
| **Availability** | Free |
| **Runs** | On your Mac — offline, nothing uploaded |
| **Input** | Text or a URL |
| **Output** | A QR code image saved where you choose |
| **Pipeline step** | No |

### How to generate a QR code

1. Click **QR Code**.
2. Type or paste into the content field ("Enter QR code content") — a URL, Wi-Fi note, contact line, any text. The preview regenerates as you type.
3. Set the **Size** — type an exact pixel value or nudge with the stepper.
4. Pick the **Error correction** level. Higher levels keep the code scannable when partially covered or printed small, at the cost of a denser pattern.
5. Optionally adjust **Foreground** and **Background** colors.
6. Press **Save** (⌘S).

### Tips and limits

- **Keep contrast high.** Dark foreground on light background scans most reliably; decorative color pairs can defeat scanners.
- **Long content needs headroom.** If you see "Content is too long for this error-correction level.", shorten the text or lower the error-correction level — capacity shrinks as correction grows.
- **Test a print before mass-printing.** Scanning behavior varies with print size and surface; a ten-second phone test saves a reprint.

## Troubleshooting

| You see | Why | Fix |
|---|---|---|
| Exported PDF pages look blurry | DPI too low for the target size | Raise **Resolution (DPI)** and re-export |
| "Content is too long for this error-correction level." | QR capacity exceeded at the current settings | Shorten the content or choose a lower **Error correction** level |
| A phone won't scan the generated code | Low contrast colors or printed too small | Restore dark-on-light colors, increase **Size**, raise error correction |
| Still stuck | — | [Open an issue](https://github.com/nanguoyu/OtterPix-app/issues/new/choose) |

## See also

- [AI OCR](../ai/ai-ocr.md) — extract text from documents and scanned PDFs
- [Format Conversion & Compression](convert-and-compress.md)
- [FAQ](../faq.md)

---

**Feedback** — report bugs in [Issues](https://github.com/nanguoyu/OtterPix-app/issues/new/choose); ask questions in [Discussions](https://github.com/nanguoyu/OtterPix-app/discussions).
