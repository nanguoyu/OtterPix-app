**English** | [简体中文](../../zh-Hans/tools/metadata.md) | [繁體中文](../../zh-Hant/tools/metadata.md) | [Deutsch](../../de/tools/metadata.md)

---

# Metadata

**Metadata** — listed on the App Store as Metadata Inspector — reads, edits, and strips the hidden data inside your photos: EXIF camera settings, GPS coordinates, IPTC creator fields, and file details. Its most common job is one toggle: removing the GPS location before a photo leaves your Mac.

## At a glance

| | |
|---|---|
| **Availability** | Free |
| **Runs** | On your Mac — offline, nothing uploaded |
| **Input** | One image or several (a thumbnail strip appears for batches) |
| **Output** | A cleaned/edited copy saved where you choose; the original stays untouched |
| **Pipeline step** | **Clear Metadata** — see [Pipeline](../pipeline.md) |

## The three modes

The tool has three modes along the top: **View**, **Edit**, and **Clear**.

### View

Everything the file carries, grouped into tidy sections: camera (Make, Model, Lens), EXIF exposure data (Aperture, Shutter Speed, ISO, Focal Length, Date Taken), GPS (Latitude, Longitude, Altitude), IPTC (Creator, Credit, Caption, Copyright), and file details (Dimensions, Color Model, Orientation, Software).

### Edit

Retype individual fields — **Artist**, **Copyright**, **Description**, **Date Taken** — or flip the **Remove GPS** toggle to drop only the location while camera, date, and exposure fields stay. Commit with **Save Edits…** (⌘S).

### Clear

Wipe metadata wholesale via the **Preset** choice, then **Clear & Save As…**:

- **Privacy** — "Strips GPS, camera identity, lens, and creator. Keeps date, exposure, orientation." It also removes the camera owner name and lens serial number, plus the IPTC creator, contact, copyright, and place fields. The right default before sharing: the photo still sorts correctly by date and displays right-side-up, but no longer says where it was taken, with what, or by whom.
- **All** — "Removes every metadata field. The result is pure pixel data."

## How to remove GPS before sharing

1. Click **All Features** in the sidebar, then **Metadata**.
2. Drag in one photo or several — with multiple files, a thumbnail strip appears at the bottom so you can flip through them.
3. Check **View** mode to see what's actually in the file.
4. For location only: switch to **Edit**, flip **Remove GPS**, press **Save Edits…** (⌘S).
5. For a fuller wipe: switch to **Clear**, choose the **Privacy** or **All** preset, and click **Clear & Save As…**.
6. Pick where the cleaned copy goes. Your original file stays untouched on disk.

## Why strip metadata

A photo's EXIF can include the exact GPS coordinates of where it was taken — worth removing deliberately before publishing, since email, cloud drives, and direct file uploads generally pass the original file along unchanged.

## Tips and limits

- **Clearing metadata leaves the picture as it is.** The operation targets the hidden records, not the visible image; lossy formats such as JPEG are re-encoded at high quality. The cleaned version is saved as a new copy, so you can compare the two any time.
- **Whole folders:** add a **Clear Metadata** step to a [Pipeline](../pipeline.md) and strip a folder in one run — resizing and watermarking in the same pass if you like.
- **Don't rely on platforms to strip for you.** Many social networks re-process uploads and drop most metadata, but the details differ per service and change over time. If removal matters, make it an explicit step.

## Troubleshooting

| You see | Why | Fix |
|---|---|---|
| GPS section is empty in View mode | The photo never had location data (or it was already stripped) | Nothing to remove — you're done |
| An edited field didn't stick | Edits are written on save, not live | Press **Save Edits…** (⌘S) and check the saved copy |
| Date-based sorting broke after clearing | The **All** preset removes the capture date too | Use the **Privacy** preset — it keeps date, exposure, and orientation |
| Still stuck | — | [Open an issue](https://github.com/nanguoyu/OtterPix-app/issues/new/choose) |

## See also

- [FAQ — Privacy & network](../faq.md#privacy--network)
- [Pipeline](../pipeline.md) — Clear Metadata as a batch step
- [Batch Rename](batch-rename.md) — uses the same EXIF fields as rename tokens

---

**Feedback** — report bugs in [Issues](https://github.com/nanguoyu/OtterPix-app/issues/new/choose); ask questions in [Discussions](https://github.com/nanguoyu/OtterPix-app/discussions).
