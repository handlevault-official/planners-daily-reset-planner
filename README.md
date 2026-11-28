# Handle Vault Planner Studio

Design a printable planner in your browser, fill it in, and download it as a print-ready PDF (A4, A5 or US Letter). No sign-up, no build step.

## Pages

| File | What it is |
|---|---|
| `index.html` | 101 planners in 10 categories (12 of them free starters) |
| `seasonal.html` | 49 seasonal and event planners (6 free starters): Christmas, Noche Buena, Simbang Gabi, New Year, Valentine's, Easter, Halloween, birthdays, debut, weddings, summer |
| `config.js` | Ko-fi username, item links, prices, pass lengths and code hashes |

Both pages share one unlock, so a code or pass works on either page.

## Features

- **Dates:** choose "Choose the date" (pick the date, then retype it on the page if you like) or "Write the date by hand" (undated: a blank date line you can type in or fill in with a pen). In dated mode, pick one date, or a date range (daily pages per day, weekly pages per week, monthly pages per month, up to 62 pages). Presets for this month, 4 weeks and 12 months. Week can start on Monday, Sunday or Saturday. The page count and dates are shown before you export.
- **Editing on the page:** type in headings, titles, notes, checklists, priorities, hourly schedules, table cells and month cells. Tap boxes, habit dots, tracker cells and mood faces to fill them. Everything is saved in the browser and appears on the printed or exported pages.
- **Quotes:** a quote line under the title. With any paid unlock you can write one quote for every page, a rotating list (one per line), or change the quote on a single page.
- **Styles:** 33 styles (cute, aesthetic, pixel, line art, motivational, masculine, seasonal) and a Clean / Light / Overload decoration level.
- **Export:** Download PDF or Print, in A4, A5 or US Letter, with a binder safe zone option.

## Free and paid

| | Free starters | Paid planners | Date-range export |
|---|---|---|---|
| Edit and export | Yes, no watermark | Preview only, watermarked export | Needs an unlock (a free planner costs the surcharge, default $2) |

- Paid planners cost **$1 to $8**, set automatically by how complex the planner is.
- **Passes (personal use):** Weekly (7 days), Monthly (30 days) and Yearly (365 days) unlock every planner, every date and unlimited exports. Default prices are $4, $9 and $49 and can be changed in `config.js`.
- A single-planner code ($1 to $8) unlocks every planner priced at or below that amount, with no end date.
- The unlock is saved on the customer's device and is reused for every planner, date and export until a pass ends.

## Ko-fi setup

1. In Ko-fi, create 8 shop items ("Planner Unlock $1" to "$8") and 3 pass items (Weekly, Monthly, Yearly).
2. In each item's thank-you message, put the matching code and a link such as `https://your-site.vercel.app/?code=HV3-XXXXX-XXXXX`. The code appears in the box and the buyer clicks **Apply**.
3. Open your site with `?owner=1` at the end of the address, fill in the item links, prices and codes, press **Generate**, and paste the result into `config.js` on GitHub.

Ko-fi cannot tell a static site who has paid, so passes are prepaid periods that customers renew by buying again. The unlock is a soft paywall: someone who edits the page code can bypass it. For stronger protection you would need a small server that verifies Ko-fi payments.

## Deploy

Upload `index.html`, `seasonal.html`, `config.js` and this README to the root of the repo, then connect it to Vercel (Framework Preset: **Other**) or turn on GitHub Pages. The pages load fonts, jsPDF and html2canvas from public CDNs, so visitors need an internet connection.

## Customize

- Catalog: edit the `RAW` list near the top of each page's script (`Name|emoji|type|skin|blocks`).
- Free starters: change `FREE_N` (the simplest planners become free).
- Styles: edit the `T` and `SK` objects. Quotes: edit the `QT` list.
