# Neil Francis Williams — website

Open `index.html` in any browser. Everything is self-contained: one HTML file plus an `images/` folder. No build step, no dependencies.

## Things to replace before going live

**Contact details** (in `index.html`, search for `PLACEHOLDERS`)

- `hello@neilfranciswilliams.co.uk` — appears twice (contact block and the form script at the bottom)
- `+44 (0)000 000 0000`
- Instagram URL and handle

**Painting titles** — I used `Untitled (Tree Study)` and `Untitled (Coastal Storm)` as gallery-style placeholders since the real titles weren't supplied. Swap in the actual titles, and add dimensions/year/price in the `.meta` line under each.

## Adding more paintings

Copy one `<figure>` block inside `<div class="grid">` in the Work section, point `src` and `data-full` at the new image, and update the caption. The grid reflows automatically.

## The enquiry form

It currently opens the visitor's email app via `mailto:`. To receive enquiries on the site itself, sign up at formspree.io (free tier), then change the form to:

```html
<form id="enquiry" action="https://formspree.io/f/YOUR_ID" method="POST">
```

and delete the `enquiry` submit handler at the bottom of the `<script>` block.

## Images

Paintings were cropped out of the supplied room and gallery photographs. If Neil has flat, straight-on studio shots of the canvases, drop them into `images/` under the same filenames — they'll look sharper.

- `tree.jpg`, `coast.jpg` — the two paintings
- `hero.jpg` — a wide detail crop used behind the title
- `insitu-living.jpg`, `insitu-gallery.jpg` — the room/gallery context shots

## Hosting

Drag the whole folder onto netlify.com/drop, or push to GitHub and enable Pages. Both are free and take about a minute. A domain like `neilfranciswilliams.co.uk` costs roughly £10/year.
