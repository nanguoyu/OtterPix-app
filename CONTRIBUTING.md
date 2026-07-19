# Contributing to OtterPix

中文用户：Issue 与讨论都欢迎直接用中文。 · Deutschsprachige: Issues und Diskussionen gern auch auf Deutsch.

OtterPix is a closed-source Mac app, so contributing here looks a little different from a typical open-source project — **no code required**. The contributions that move the app forward are reports, corrections, and answers.

## Write a bug report that gets fixed

The fastest path from report to fix is a report the developer can reproduce. The [bug report form](https://github.com/nanguoyu/OtterPix-app/issues/new/choose) asks for everything below; the gold standard is:

- **Exact steps**, numbered, starting from a fresh launch. "Open AI Cutout → drop a PNG → click Cut Out" beats "cutout is broken".
- **What you expected** and **what actually happened** — one sentence each.
- **App version** (in OtterPix: **OtterPix → About OtterPix**), **macOS version**, and **Mac chip** (M1/M2/M3/M4 family).
- **A screenshot with a neutral test image.** This is a public tracker — keep personal photos out of it. Photo EXIF data can contain GPS locations (OtterPix's **Metadata** tool strips it), and crash logs can contain your macOS username and file paths, so redact before pasting.

One issue per problem. Two bugs in one issue means at least one of them gets lost.

## Improve a translation

OtterPix's interface ships in 18 languages, and native speakers catch what translators miss. If a string in any language is wrong, awkward, or clipped, open a [translation feedback issue](https://github.com/nanguoyu/OtterPix-app/issues/new/choose) with four things: the language, where the text appears (e.g. "AI Cutout → Model picker"), the current text, and your suggested text. These fixes routinely ship in the next release.

## Answer questions

Helping someone in [Q&A](https://github.com/nanguoyu/OtterPix-app/discussions/categories/q-a) is a real contribution. If you know the answer — or even just the right docs page — jump in. A community where questions get answered is worth more than any single feature.

## Vote with reactions

👍 reactions on issues and feature requests are considered during triage. If an existing issue matches your problem or wish, reacting to it (and adding any new detail as a comment) is more useful than opening a duplicate.

## Pull requests

**This repo accepts PRs only for typo/link fixes inside `docs/` and `assets/` alt text. PRs touching anything else will be closed with thanks — the app itself is closed-source.**

For anything bigger than a typo — restructuring a guide, adding a section — open an issue or a discussion first so the change can be agreed before you spend time on it.

## Everything else

Routing for questions, billing, and private reports lives in [SUPPORT.md](SUPPORT.md). Security reports: [SECURITY.md](SECURITY.md).
