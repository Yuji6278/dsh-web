# Endfield Baker (终末地 · BAKER)

English | [中文](README.zh.md)

Endfield Baker — an Arknights Endfield industrial-terminal skin for the dsh
web GUI, shipped as a pure asset directory inside the skin-center package.
The conversation area is rebuilt after the BAKER communication interface;
the remaining shell layers follow Endfield's industrial vocabulary: fine
grids, diagonal signal stripes, monospace micro-labels and single-pixel
hairlines.

## What it is

- **Pure assets**: `skin.json` (v2 manifest) + `skin.css` (L1 token remap
  with `--ef-*` primitives) + `patches.css` (L3 structural patches in
  sections 0-12) + `assets/` (header art, card textures, backdrop) +
  `preview/` (light/dark screenshots). No package.json, no build step, no
  hooks.
- **One palette for both modes**: light and dark themes share a single
  terminal palette; `:root` pins `color-scheme: dark` and no
  `body[data-ds-dark-theme]` override exists, so both preview screenshots
  show the same treatment by construction.
- **Point-sampled from the reference art**: page ink, row fill, chat page,
  composer pill and both signal colours were sampled pixel by pixel from the
  BAKER reference image.
- **Rebuilt conversation area**: cyan header rule, signal-yellow selected
  rows, cut-corner console cards, a white pill composer and a frosted-grey
  chat backdrop, finished with the three-colour strip and solid deck edge
  under the header.

## Palette

| Role | Colour | What it paints |
| --- | --- | --- |
| Signal cyan | `#19CFFD` | brand accent, primary buttons, send key, header bars |
| Signal yellow | `#FFEF00` | selected rows, diagonal hatch stripes |
| Page ink | `#131514` | page background and panels |
| Chat grey | `#343634` | frosted chat page backdrop |
| Composer pill | `#F0EEEE` | white input pill and its text column |
| Alert orange | `#FF6A52` | destructive and error states |
| Confirm green | `#35D69A` | success states |

## Preview

```sh
pnpm market:build                              # refresh market/dist
open market/dist/preview.html?skin=endfield-baker&theme=light
```

`preview/light.png` and `preview/dark.png` show the same palette: the skin
does not branch on the light/dark theme.
