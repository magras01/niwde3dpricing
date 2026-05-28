# NIWDE3D Pricing Calculator

A standalone web app for 3D print sellers to calculate accurate product pricing — covering every cost from filament and electricity to platform fees, affiliate commissions, and machine depreciation.

Built by a rider, for makers. No server. No login. No subscription. Just open and use.

---

## Live Demo

> Deploy to GitHub Pages, Netlify, or Vercel and paste your URL here.

---

## Features

### Calculator
- **Printer Specs** — cost, lifespan, power consumption with saved printer presets (e.g. Bambu Lab A1, P1S)
- **Print Job** — print time, items per plate, failed print rate
- **Material & Energy** — filament usage, filament cost per kg, electricity cost
- **Hardware & Components** — dynamic add/remove rows for inserts, magnets, screws, etc.
- **Platform & Fees** — platform fee %, affiliate commission %, tax rate
- **Overhead** — packaging, labor, selling price, monthly target units

### Platform Presets
- Built-in: **Shopee**, **TikTok**, **Lazada**, **Wholesale**
- Add, edit, and delete your own custom presets
- **Your current setup** — personal scratchpad that saves your data across preset switches

### Analytics (live, updates instantly)
- Production cost per item
- Break-even price
- Suggested price (3× rule)
- Profit per item & profit margin
- You receive (after all fees)
- Monthly profit, revenue, overhead
- Printer ROI — months to pay off your printer
- Monthly filament spend
- Cost breakdown bars

### Price Comparison Table
- Add multiple price points to compare side by side
- Shows: you receive, profit, margin, monthly profit, status (Loss / Low / OK / Great)
- Auto-updates when any input changes

### Data Management
- **Save / Load / Update / Delete** products — stored in browser localStorage
- **Saved printer presets** — load printer specs in one click
- **Export to Excel (.xlsx)** — two sheets: Pricing + Price Comparison
- **Import from Excel (.xlsx)** — re-import any previously exported file

---

## Getting Started

### Option 1 — Run locally
1. Download `index.html`
2. Open it in any browser
3. No installation needed

### Option 2 — Host on GitHub Pages
1. Fork this repository
2. Go to **Settings → Pages**
3. Set source to `main` branch, root folder
4. Your app is live at `https://yourusername.github.io/repo-name`

### Option 3 — Deploy to Netlify
1. Go to [netlify.com](https://netlify.com)
2. Drag and drop `index.html`
3. Live in 30 seconds

---

## How Pricing is Calculated

```
Electricity per plate   = (watts ÷ 1000) × print time × electricity cost
Filament per plate      = (grams ÷ 1000) × filament cost per kg
Machine depreciation    = (printer cost ÷ lifespan hours) × print time

Base cost per item      = (electricity + filament + depreciation) ÷ items per plate
Failed print waste      = base cost × fail rate ÷ (1 − fail rate)

Production cost         = base cost + failed waste + packaging + labor + hardware & components

Net revenue             = selling price − platform fee − affiliate − tax
Profit per item         = net revenue − production cost
Break-even price        = production cost ÷ (1 − platform% − affiliate% − tax%)
Suggested price (3×)    = production cost × 3
```

---

## Data & Privacy

All data is stored locally in your browser using `localStorage`. Nothing is sent to any server. Clearing your browser data will erase saved products and presets — use the **Export** button regularly to back up your data as Excel files.

---

## Tech Stack

- Pure HTML, CSS, JavaScript — no frameworks, no build tools
- [Inter](https://fonts.google.com/specimen/Inter) — UI font
- [JetBrains Mono](https://fonts.google.com/specimen/JetBrains+Mono) — numbers and metrics
- [SheetJS (xlsx)](https://sheetjs.com/) — Excel export and import

---

## Screenshots

> Add screenshots here after deployment.

---

## Roadmap

- [ ] Worst-case profit (fail rate doubled)
- [ ] Fee sensitivity analysis
- [ ] Daily units needed
- [ ] PWA support (installable on mobile)
- [ ] Cloud sync across devices

---

## License

MIT — free to use, modify, and distribute.

---

Made with ☕ and ASA filament by **NIWDE3D**
