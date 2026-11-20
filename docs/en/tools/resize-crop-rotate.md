**English** | [简体中文](../../zh-Hans/tools/resize-crop-rotate.md) | [繁體中文](../../zh-Hant/tools/resize-crop-rotate.md) | [Deutsch](../../de/tools/resize-crop-rotate.md)

---

# Resize, Crop & Rotation

The geometry trio: **Resize** scales images by percentage or exact dimensions, **Crop** trims them with free or fixed aspect ratios, and **Rotation** rotates and flips at any angle. All three are free, and all three exist as [Pipeline](../pipeline.md) steps for batch work.

## At a glance

| | |
|---|---|
| **Availability** | Free |
| **Runs** | On your Mac — offline, nothing uploaded |
| **Input** | One image or a batch |
| **Output** | Processed copies in a destination you choose |
| **Pipeline steps** | **Resize**, **Crop**, **Rotate** — see [Pipeline](../pipeline.md) |

## Resize

1. Click **Resize** and drop in your images.
2. Choose how to scale: by percentage, or by exact pixel dimensions in the **Width** and **Height** fields. You can type a value directly or nudge it with the stepper.
3. The chain-link icon between the fields toggles **Lock aspect ratio** — locked, editing one field recalculates the other; unlocked, the two move independently (and the image can stretch).
4. Press **Save** (⌘S).

### Options

- **Percentage** — quick proportional scaling, e.g. 50% for web delivery.
- **Exact dimensions** — **Width** / **Height** in pixels with **Lock aspect ratio** on by default.
- **Fit within** — batch-friendly bounding-box mode. In the app's own words: "Each image is scaled to fit within this box, keeping its aspect ratio. Images already smaller stay unchanged." Ideal when a folder of mixed portrait and landscape shots must all end up no larger than, say, 1920 px.

## Crop

1. Click **Crop** and drop in an image.
2. Drag the corner and edge handles of the crop box, or pick a fixed aspect ratio — **Free** and **Original** are always available, alongside common fixed ratios.
3. A floating badge shows the crop numerically as you drag: the original size ("Original 4032 × 3024 px") and the selected portion ("42% selected"), so you can hit precise framings instead of eyeballing.
4. Press **Save** (⌘S).

### Options

- **Aspect ratio** — **Free** for arbitrary crops; **Original** keeps the source proportions; fixed ratios for covers, avatars, and thumbnails.
- **Alignment** (Pipeline step) — the batch Crop step crops relative to an anchor: **Center**, **Top Left**, **Top Right**, **Bottom Left**, **Bottom Right**.

## Rotation

1. Click **Rotation** and drop in your images.
2. Use **Left 90°** / **Right 90°** for the common quarter turns, the flip buttons to mirror horizontally or vertically, or drag the angle control for free rotation — the label reads out the current value ("Angle: 12°").
3. Free angles enlarge the canvas to contain the rotated image; the preview shows the resulting bounding box and its pixel size before you save.
4. Press **Save** (⌘S).

## Tips and limits

- **Resize cannot invent detail.** Scaling *up* with Resize simply interpolates pixels. To enlarge a photo and add plausible detail, use [AI Upscale](../ai/ai-upscale.md) instead.
- **Order matters in a pipeline.** Put **Crop** and **Resize** before **Watermark** — the app warns if a watermark step sits before them, because it may end up cropped off or blurred.
- **Lock the ratio unless you mean it.** An unlocked resize to arbitrary Width × Height stretches the image. The lock icon shows the current state at a glance.
- **Lossy formats are saved at 95 percent quality.** Resize, Crop, and Rotation save JPEG, HEIC, and other lossy formats at a fixed 95 percent, independent of the default quality in Settings.

## Troubleshooting

| You see | Why | Fix |
|---|---|---|
| Resized image looks distorted | **Lock aspect ratio** was off and both fields were edited | Turn the lock on and re-enter one dimension |
| Enlarged image looks soft | Resize interpolates; it can't add detail | Use [AI Upscale](../ai/ai-upscale.md) for enlargement |
| Rotated image has extra empty area | Free-angle rotation enlarges the canvas to fit the rotated frame | Expected — crop afterwards if you want the frame tight |
| Still stuck | — | [Open an issue](https://github.com/nanguoyu/OtterPix-app/issues/new/choose) |

## See also

- [Pipeline](../pipeline.md) — Resize, Rotate, and Crop as batch steps
- [AI Upscale](../ai/ai-upscale.md) — enlargement with detail reconstruction
- [Format Conversion & Compression](convert-and-compress.md)

---

**Feedback** — report bugs in [Issues](https://github.com/nanguoyu/OtterPix-app/issues/new/choose); ask questions in [Discussions](https://github.com/nanguoyu/OtterPix-app/discussions).
