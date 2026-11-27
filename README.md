# Handle Vault Planner Studio

Design a printable planner in your browser and download it as a print-ready PDF (A4, A5 or US Letter). No sign-up, no build step.

## Pages

| File | What it is |
|---|---|
| `index.html` | 101 planners in 10 categories (daily, weekly, monthly, habits, fitness, finance, school, work, home, lifestyle) |
| `seasonal.html` | 49 seasonal and event planners (Christmas, Noche Buena, Simbang Gabi, New Year, Valentine's, Easter, Halloween, birthdays, debut, weddings, summer) |
| `config.js` | Ko-fi username, tier links, batch surcharge and unlock-code hashes |

## Features

- 33 styles: cute, aesthetic, pixel, line art, motivational, masculine and seasonal
- Style level: Clean, Light or Overload (stickers, tape, frames)
- Click any heading on the page to rename it
- Fonts, line styles (lined, dotted, blank, checklist), binder safe zone, Monday or Sunday week start
- Single page or batch export (full month, 4 weeks, 12 months)
- Download PDF or print, with auto-save in the browser

## Ko-fi pricing ($1 to $8)

Price is calculated from how complex the planner is. Batch export adds a surcharge (default $2, capped at $8).

1. In Ko-fi, create 8 shop items, "Planner Unlock $1" to "$8".
2. In each item's thank-you message, include the matching code and a link such as `https://your-site.vercel.app/?code=HV3-XXXXX-XXXXX`. The code appears in the box and the buyer clicks **Apply**.
3. Open your site with `?owner=1` at the end of the address, fill in the item links and codes, press **Generate**, and paste the result into `config.js`.

Without a code, the PDF and print carry a watermark. A code unlocks every planner priced at or below its tier.

This is a soft paywall: the site is static, so someone who edits the page code can bypass it. For stronger protection you would need a small server that verifies Ko-fi payments.

## Deploy

Upload all files to the root of the repo, then connect it to Vercel (Framework Preset: **Other**) or turn on GitHub Pages (Settings, Pages, branch `main`, folder `/ (root)`).

The pages load fonts, jsPDF and html2canvas from public CDNs, so visitors need an internet connection.

## Customize

- Catalog: edit the `RAW` list near the top of each page's script (`Name|emoji|type|skin|blocks`).
- Styles: edit the `T` and `SK` objects.
- Quotes: edit the `QT` list.
