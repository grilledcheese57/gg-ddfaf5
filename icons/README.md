# App icons — PLACEHOLDERS

> **These icons are PLACEHOLDERS.** They are a plain generated grimoire mark
> (an illuminated gold star-flourish on a parchment field) produced by
> `scripts/generate-icons.mjs`. **The owner replaces them with ChatGPT-Pro art
> later** — see PROJECT.md ("aesthetic art generated via ChatGPT Pro").

## Files (referenced by the web app manifest in `vite.config.ts`)

| File                      | Size    | Purpose / `purpose`           |
| ------------------------- | ------- | ----------------------------- |
| `icon-192.png`            | 192×192 | Android home screen (`any`)   |
| `icon-512.png`            | 512×512 | Splash / high-DPI (`any`)     |
| `icon-maskable-512.png`   | 512×512 | Adaptive/masked (`maskable`)  |
| `apple-touch-icon.png`    | 180×180 | iOS home screen (apple-touch) |

## Replacing them

Drop in real PNGs at the same sizes/filenames (keep the maskable safe-zone:
keep the mark within the inner ~80% so platform masking doesn't clip it), or
re-run the generator after editing the mark:

```sh
node scripts/generate-icons.mjs
```

The generator uses the grimoire token colors (parchment `#EDE3CB`, surface
`#E3D4AE`, illuminated gold `#9A7B2E`/`#C8A02C`, ink `#2B2118`) — the manifest is
the one place these hex literals are allowed.
