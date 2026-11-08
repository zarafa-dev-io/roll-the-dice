# Roll the Dice, Meet Jean-Michel!

Interactive goose-game board presenting a career, hobbies and personal projects.
Single page, no build step and no dependencies: open `index.html` or put the
folder on any static host (GitHub Pages, Netlify, an S3 bucket…).

## Content

All content lives in the JSON block `<script type="application/json" id="board-data">`
inside `index.html`:

- `board`: title, subtitle, and the shared images (`hub_image`, `board_image`,
  `path_image`, `pawn_image`).
- `style`: one entry per square type, with its color, legend label and painted `frame`.
- `tiles`: the squares. The path follows the `next` links from the `start` square.
  Each square can have an `image`; add `"image_fit": "contain"` to show a logo
  whole instead of filling the picture area.

## Images

- `images/01.webp` … `25.webp`, `26-arcad.webp`: square illustrations
- `images/hub.webp`: central panel background
- `images/board.webp`, `images/path.webp`: repeating meadow and cobblestone textures
- `images/pawn.webp`: the pawn
- `images/frames/*.webp`: painted frames, one per category (9-slice, slice 40 px)

## Controls

Space or the die rolls · → moves one square · click a square to read its story.
Fonts load from Google Fonts; without a connection the page falls back to system fonts.
