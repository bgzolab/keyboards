# AGENTS.md

Personal keyboard notes and VIA profiles. There is no application code, package manifest, build, test, lint, or CI; do not invent commands for them.

## Repository map

- `README.md`: personal keyboard history/preferences in Chinese, not a project index or setup guide. Preserve its opinionated tone.
- `docs/reviews/<model>.md`: one review per keyboard, mostly Chinese. They use Obsidian `[[wikilinks]]`, `[^footnotes]`, and status blockquotes such as `> 已卖，...`. Purchase history, prices, and opinions are intentional content, not fluff.
- `nuphy-air75-v2/README.md`: VIA setup, reset/Fn-lock instructions, and USB-ID troubleshooting for the Air75 V2.
- `nuphy-air75-v2/via3.json`: VIA v3 device definition (6×17 matrix, 84 visible keys, custom keycodes).
- `nuphy-air75-v2/layout/default.json`: saved VIA keymap with 8 layers × 102 entries and 16 macro slots.
- `nuphy-air75-v2/layout/fn-lock.json`: Fn-lock variant of the same keymap.

There is no review index to update; `README.md` is not one.

## VIA / keymap gotchas

- These are VIA JSON files, not QMK C keymaps. The repo has no firmware source and no flashing/build flow; bindings are changed through VIA definitions and saved keymaps.
- VIA matches hardware by `vendorId` + `productId`. If VIA does not recognize the board, check the USB ID (`lsusb | grep NuPhy` on Linux) and align `productId` in `via3.json`. The setup notes report `0x3265`, while the committed definition uses `0x3245`.
- Each layout's `vendorProductId` encodes the definition IDs: `(vendorId << 16) | productId` = `0x19F53245` (`435499589`). Keep it in sync if either ID changes.
- Layer arrays are flat 6×17 = 102 entries indexed by matrix position. Do not reorder, truncate, or renumber them. Use `KC_NO` for empty positions and `KC_TRNS` for transparent ones.
- The 84 physical keys rendered by `via3.json` versus 102 slots per saved layer is expected; do not pad or truncate layouts to match the visible-key count.
- `fn-lock.json` is not only a top-row swap: layer 2 also differs. Diff both layouts before syncing edits.
- `nuphy-air75-v2/README.md` still cites pre-reorganization filenames (`nuphy-air75-v2-via3.json`, `nuphy_air75_v2.layout.default.json`, `nuphy_air75_v2.layout.fn-lock.json`). Current paths are `via3.json`, `layout/default.json`, and `layout/fn-lock.json`; correct those references if you touch the README.
- Preserve indentation: `via3.json` is tab-indented, while saved layouts use 2 spaces.
- The wikilink `[[20251129-keychron-z7max|Keychron Z7Max]]` in `docs/reviews/nuphy-air75-v3.md` does not resolve; the actual file is `docs/reviews/keychron-z7max.md`. Do not copy it as an example.

## Verification

Validate JSON after any edit:

```sh
for f in nuphy-air75-v2/via3.json nuphy-air75-v2/layout/*.json; do
  python3 -m json.tool "$f" >/dev/null || exit 1
done
```

Before committing a layout, confirm it still has 8 layers, 102 entries per layer, and 16 macro slots.

## Git

- Commit subjects use Conventional Commits prefixes, e.g. `docs(reviews): add ...` and `chore(nuphy): move ...`; keep subjects short and in English.
- Work happens directly on `main`; there are no other branches, tags, or CI checks.
- `origin` is a gist URL, not a normal repository, and currently returns `Repository not found`; local `main` is ahead. Do not rely on fetch/push or treat it as a backup.
