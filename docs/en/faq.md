**English** · [简体中文](../zh-Hans/faq.md) · [繁體中文](../zh-Hant/faq.md) · [Deutsch](../de/faq.md)

---

# FAQ

## About

### What is OtterPix?

An image toolkit for the Mac: ten one-click basic tools (convert, compress, resize, crop, rotate, watermark, rename, metadata, PDF to image, QR code), a visual [Pipeline](pipeline.md) for batch workflows, and seven on-device AI features. Everything runs locally on Apple silicon — no accounts, no uploads.

### Is OtterPix open source?

No. OtterPix is a commercial, closed-source app distributed through the Mac App Store — there is no source code in this repo, and none is planned. This repo is the app's public home instead: guides, release notes, and the bug tracker.

### Which languages does OtterPix speak?

The app's interface ships in 18 languages. The guides in this repo are maintained in four: English, 简体中文, 繁體中文, and Deutsch. Wrong or awkward translations in any of the 18 are worth an [issue](https://github.com/nanguoyu/OtterPix-app/issues/new/choose) — native-speaker corrections routinely ship in the next release.

### What does it require?

macOS 14 (Sonoma) or later on an Apple silicon Mac (M1 or newer). Intel Macs are not supported. For AI Generation, 16 GB RAM or more is recommended.

## Formats & files

### Which formats can OtterPix read and write?

Read and write: JPEG, PNG, TIFF, BMP, HEIC, WebP, AVIF — plus an **Other Formats** section in the conversion picker for the less common formats your Mac can write. Reading is much broader still: the Home drop zone advertises PNG · JPEG · HEIC · TIFF · WebP · GIF +51. PDFs can be rendered to images at any DPI with the [PDF to Image](tools/pdf-and-qr.md) tool.

### Are color profiles and EXIF orientation preserved?

Most operations preserve color profiles and EXIF orientation. The one thing that removes metadata is the thing designed to: the [Metadata](tools/metadata.md) tool's clear function and the Pipeline's **Clear Metadata** step.

### Does OtterPix modify my original files?

No tool overwrites originals. Saving always writes copies to a destination you choose; Batch Rename likewise writes into a folder you pick and leaves originals in place unless you explicitly turn on **Move originals to Trash**.

## Privacy & network

### Does OtterPix upload my images?

No. Every operation — including AI inference — runs locally on your Mac. The app contains no analytics SDK and never uploads your images, generation prompts, OCR content, or usage telemetry. Its limited network traffic is for StoreKit; a startup Cloudflare edge-country lookup used only to choose a model-download mirror; a small URL-only model-manifest refresh when the model store is first used; and model downloads that you initiate. None of these requests contains your media or processing content. Full details are in the [privacy policy](https://otterpix.app/en/privacy).

### Can I use OtterPix offline?

Yes. Basic processing and AI inference with already-downloaded models work offline. A connection is still needed for initial or updated model downloads and StoreKit purchase or restore operations; the metadata and routing requests above do not upload processing content.

### How do I remove GPS data from photos before sharing?

Use the [Metadata](tools/metadata.md) tool: the **Remove GPS** toggle drops only the location, or the **Privacy** clear preset strips GPS plus camera identity, lens, and creator while keeping date, exposure, and orientation.

## AI models

### Why does an AI feature want to download something?

Each AI feature is powered by a model that ships separately from the app to keep the download small. The first time you run a feature, it fetches its model; after that, the feature works fully offline. Sizes range from a few megabytes (the smallest upscale model) up to several gigabytes (image generation).

### Where do I manage the models?

**Settings → AI**. Every model can be downloaded or deleted there, and active downloads can be paused, resumed, or cancelled. Partial data is retained across relaunch and shown as resumable rather than installed. Feature pages show the same shared progress for the model they need.

### Do models cost anything?

No. Model downloads are free for every feature, including the Pro tools.

## Free & Pro

### What exactly is free?

All ten basic tools, the Pipeline, AI OCR, and AI Generation — permanently, not as a trial. On top of that, each of the five Pro AI tools (AI Upscale, AI Cutout, AI Eraser, AI Anonymize, AI Restore) includes one free use per day.

### How does the daily free use work?

Each Pro AI card shows an amber **Free today** badge while its free use is available. After a successful run, the banner says: "Today's free use for this tool is up" — "Each AI tool gets one free use a day — this one resets at midnight." The use is charged per loaded photo, not per click: you can re-run, refine, and iterate on the same photo all day within that one use, and revisiting a photo you already used today's run on keeps it free to refine.

### What are the free-plan limits in the Pipeline?

"Free plan: one image when a Pro step is used. Upgrade for batches." — one Pro step per pipeline, single image while it's present, and running it consumes that tool's daily free use. Details in the [Pipeline guide](pipeline.md#free-plan-limits).

### What does Pro cost, and how do I manage it?

Pro comes as a monthly subscription, a yearly subscription, or a one-time lifetime purchase — see current pricing on the [Mac App Store](https://apps.apple.com/app/id6772468615). Subscriptions are managed and cancelled in your [Apple Account subscriptions](https://apps.apple.com/account/subscriptions). The lifetime purchase is a one-time payment: nothing renews, and there is no subscription to manage.

### How do refunds work?

All purchases are processed by Apple, so refund requests go through Apple at [reportaproblem.apple.com](https://reportaproblem.apple.com). The developer cannot see your payment details or issue refunds directly.

## Regional availability & support

### Is every feature available in every country?

In the version of OtterPix distributed through the mainland-China Mac App Store, AI Generation and AI OCR are not available. Every other feature — including all five Pro AI tools — is available in every region OtterPix ships to. See the [Terms of Service](https://otterpix.app/en/terms) for details.

### Where do I report a bug or ask a question?

Bugs → [open an issue](https://github.com/nanguoyu/OtterPix-app/issues/new/choose). Questions → [Discussions → Q&A](https://github.com/nanguoyu/OtterPix-app/discussions/categories/q-a). English, 中文, and Deutsch are all welcome. For anything private or sensitive: hello@otterpix.app.

## See also

- [Getting started](getting-started.md)
- [Pipeline](pipeline.md)
- [Changelog](../../CHANGELOG.md)

---

**Feedback** — report bugs in [Issues](https://github.com/nanguoyu/OtterPix-app/issues/new/choose); ask questions in [Discussions](https://github.com/nanguoyu/OtterPix-app/discussions).
