# Ekko landing page

A standalone redesign concept for [ekkomd.com](https://www.ekkomd.com/). Open `index.html` in a browser; no build step.

## Direction

A clinical journal instead of a SaaS template: warm paper, ink-black type, one vermilion "recording" accent and one chart green for confirmed data. No gradients, no glass cards, no stock icons.

- **Type:** Newsreader (display serif, like a medical journal), Geist (UI and body), Geist Mono (clinical data, labels). Noto Sans subsets render the Indic scripts.
- **Hero demo:** a live consultation where the Tamil and English transcript types in, key phrases get highlighted, and the SOAP note and action items fill in alongside it. This is the product, shown working, instead of a dashboard screenshot. Respects `prefers-reduced-motion` by showing the finished note.
- **Structure:** numbered sections (§ 1, § 2, § 3) on hairline rules, features as a five-step ledger (listen → separate → extract → summarize → fit), each with a small real specimen, and the blog as a table of contents.

All copy, the testimonial, blog titles, offices and contact details come from the current site. The clinical example in the demo is illustrative.

## Tokens

| Token | Value | Use |
| --- | --- | --- |
| `--paper` | `#f2efe7` | Page |
| `--sheet` | `#fbfaf6` | Raised surfaces |
| `--ink` | `#1b1915` | Text, primary buttons, closing band |
| `--ink-2` / `--ink-3` | `#5d574d` / `#958e81` | Secondary, muted |
| `--rule` | `#d6cfc0` | Hairlines |
| `--signal` | `#c9431b` | Recording, patient voice, emphasis |
| `--chart` | `#2d5a45` | Doctor voice, confirmed note data |
