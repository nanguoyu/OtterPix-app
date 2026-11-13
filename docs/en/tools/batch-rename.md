**English** | [简体中文](../../zh-Hans/tools/batch-rename.md) | [繁體中文](../../zh-Hant/tools/batch-rename.md) | [Deutsch](../../de/tools/batch-rename.md)

---

# Batch Rename

**Batch Rename** renames many image files at once with a template system — sequential numbering, EXIF capture dates, camera names — and shows a full preview before anything is written.

## At a glance

| | |
|---|---|
| **Availability** | Free |
| **Runs** | On your Mac — offline, nothing uploaded |
| **Input** | Any number of image files |
| **Output** | Renamed copies in a folder you choose; originals stay in place unless you opt in to trashing them |
| **Pipeline step** | No — renaming is its own tool |

## How to rename a batch

1. Click **Batch Rename** and drag your files in, or use **Add Files…**.
2. Pick the order with **Sort by** — **Name**, **EXIF date**, or **Modified date**. The order determines the counter sequence.
3. Build the naming pattern in the **Template** field. Below it sit the token chips — "Tap a token to insert". The default template is `{name}_{counter:03}.{ext}`.
4. Watch the **Preview** column: every file's new name appears live, and conflicts are flagged ("2 conflict(s)") before you commit.
5. Optionally refine with **Find & Replace** and **Case** (see Options).
6. Press **Save** (⌘S), then **Choose Folder**. As the app explains: "Choose where OtterPix should save the renamed files. Originals stay in place unless you turn on 'Move originals to Trash'."

## Template tokens

| Token | Produces |
|---|---|
| `{name}` | The original file name, without extension |
| `{ext}` | The original extension (`jpg`, `png`, …) |
| `{counter}` | A sequential number; **Counter start** and **step** are configurable |
| `{counter:03}` | The counter zero-padded to a width — `001`, `002`, … |
| `{date}` | The EXIF capture date (falls back to the file's modified date if the photo has none) |
| `{date:yyyy-MM-dd}` | The capture date in a custom format |
| `{mdate}` | The file's modified date; custom formats work the same way |
| `{exif:camera}` | The camera's make and model from EXIF |

Example: `{date:yyyy-MM-dd}_{exif:camera}_{counter:03}.{ext}` → `2026-05-14_Apple iPhone 15 Pro_001.heic`.

## Options

### Find & Replace

A **Find** / **Replace** pair applied after the template, with a **Regular expression** toggle for pattern-based edits — strip a prefix, swap separators, collapse spaces.

### Case

Normalize the final name: **Keep**, **lowercase**, **UPPERCASE**, or **Title Case**.

### Move originals to Trash

Off by default. When on, the originals are moved to the macOS Trash *after* all files have been saved to the chosen folder — recoverable from the Trash if needed. This is the closest the tool gets to renaming "in place"; by default it never touches your source files.

## Tips and limits

- **Preview is the contract.** Nothing is written until you save, and conflicts (two files resolving to the same name, or a name that already exists on disk) are surfaced in the preview first.
- **`{date}` needs EXIF.** Screenshots and exported graphics often carry no capture date, in which case `{date}` falls back to the file's modified date. Sort by **EXIF date** only makes sense for camera photos.
- **Clipboard images can't be renamed.** Paste needs a real file: "Clipboard holds image data, not a file — save it to disk first."

## Troubleshooting

| You see | Why | Fix |
|---|---|---|
| "2 conflict(s)" in the preview | Two inputs resolve to identical names, or a target name already exists | Add `{counter}` to the template, or change the pattern until the preview is conflict-free |
| `{date}` gives today's date, not the photo date | The file has no EXIF capture date | Expected fallback to modified date — check the file's metadata in the [Metadata](metadata.md) tool |
| Files saved but originals still present | Default behavior — originals are never removed unless opted in | Turn on **Move originals to Trash** if you want that |
| Still stuck | — | [Open an issue](https://github.com/nanguoyu/OtterPix-app/issues/new/choose) |

## See also

- [Metadata](metadata.md) — see the EXIF fields the tokens read
- [Pipeline](../pipeline.md) — for processing (rather than renaming) whole folders
- [FAQ](../faq.md)

---

**Feedback** — report bugs in [Issues](https://github.com/nanguoyu/OtterPix-app/issues/new/choose); ask questions in [Discussions](https://github.com/nanguoyu/OtterPix-app/discussions).
