# Made Ready Co — Marketing Website

The public-facing marketing site for **Made Ready Budget Tracker (MRBT)** — an automated Google Sheets budget tracker for UK banks, sold on Etsy by [Made Ready Co](https://madeready.co).

Live at: **[madereadyco.github.io/madeready-site](https://madereadyco.github.io/madeready-site/)**

---

## What this repo contains

```
madeready-site/
├── index.html      ← Single-page marketing site (all HTML, CSS, JS in one file)
└── README.md       ← This file
```

The entire site is a single self-contained HTML file. No build step, no dependencies, no npm, no framework.

---

## The product

**Made Ready Budget Tracker** is a Google Sheets template that:

- Imports CSV bank statements from Monzo, Chase UK, Starling, Barclays, and any UK bank
- Auto-categorises transactions using 80+ pre-loaded UK merchant keywords
- Shows a live budget dashboard, safe-to-spend metric, and net worth tracker
- Runs entirely inside the buyer's own Google account — no subscription, one-time purchase

**MRBT Pro** adds Claude AI running invisibly inside the sheet — smart categorisation, monthly financial insights, natural language queries, and anomaly alerts — with no API key required from the buyer.

| Version | Price | Key addition |
|---|---|---|
| MRBT Standard | £14.99 | Full automation, UK bank CSV import |
| MRBT Pro | £34.99 | Claude AI categorisation + insights |
| MRBT Pro Upgrade | £15.00 | For existing Standard customers |

---

## Site sections

| Section | Description |
|---|---|
| Hero | Headline, bank pills, trust signals |
| Sheet preview | Interactive 5-tab spreadsheet mockup |
| How it works | 5-step setup walkthrough + MRBT Pro AI flow diagram |
| Features | 9 feature cards (Standard + Pro) |
| Security | CSV safety explainer + checklist callout |
| Comparison | Standard vs Pro feature table |
| Pricing | Two pricing cards + upgrade path |
| Reviews | Three testimonials + key stats |
| FAQ | 7 questions with accordion answers |
| CTA | Etsy buy button |
| Footer | Links, contact, tags |

---

## Tech

- Pure HTML, CSS, and vanilla JS — no framework, no build tool
- Google Fonts: DM Sans, Inter, JetBrains Mono
- Dark mode default with light mode toggle (preference saved to localStorage)
- Responsive at 760px breakpoint (hamburger menu)
- Interactive sheet mockup with 5 clickable tabs
- Deployed via GitHub Pages

---

## How to update

**Quick edit (no local setup needed):**

1. Open `index.html` in this repo on GitHub
2. Click the pencil ✏️ icon
3. Make your changes
4. Click **Commit changes** → **Commit directly to main**
5. GitHub Pages rebuilds automatically — live within ~60 seconds

**Local edit:**

```bash
git clone https://github.com/madereadyco/madeready-site.git
cd madeready-site
# edit index.html in VS Code or any editor
git add .
git commit -m "describe your change"
git push
```

---

## Related repos

| Repo | Description | Status |
|---|---|---|
| `madeready-site` | This repo — marketing website | Live |
| `madeready-apfe-api` | MRBT Pro AI backend (Next.js / Vercel) | In development |

---

## Brand

| | |
|---|---|
| Brand | Made Ready Co |
| Domain | madeready.co |
| Product | Made Ready Budget Tracker (MRBT) |
| Contact | roland@madeready.co |
| Etsy shop | Made Ready Co |

---

## Roadmap

- [ ] Connect custom domain `madeready.co` via Vercel
- [ ] Build `madeready-apfe-api` — Claude AI proxy endpoint for MRBT Pro
- [ ] Add MRBT Pro listing to Etsy
- [ ] Add upgrade listing (£15) for existing Standard customers
- [ ] Build the actual MRBT Google Sheet and Apps Script
- [ ] Record Loom setup video
- [ ] Create ReadMe PDF in Canva

---

*© 2025 Made Ready Co · madeready.co*
