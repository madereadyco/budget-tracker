# Made Ready Co — Marketing Website

The public-facing marketing site for **Made Ready Budget Tracker (MRBT)** — the only Google Sheets budget tracker on Etsy built specifically for UK banks. Sold by [Made Ready Co](https://madeready.co) on Etsy.

Live at: **[madereadyco.github.io/madeready-site](https://madereadyco.github.io/madeready-site/)**

---

## Brand

| | |
|---|---|
| Brand | Made Ready Co |
| Domain | madeready.co |
| Email | roland@madeready.co |
| Product | Made Ready Budget Tracker (MRBT) |
| Internal code | MRBT (replaces APFE everywhere) |
| Etsy shop | Made Ready Co |

---

## The product

**Made Ready Budget Tracker (MRBT)** is a Google Sheets template that:

- Imports CSV bank statements from Monzo, Chase UK, Starling, Barclays, Revolut, and any UK bank
- Auto-categorises transactions using 80+ pre-loaded UK merchant keywords
- Shows a live budget dashboard, safe-to-spend metric, and net worth tracker
- Runs entirely inside the buyer's own Google account — no subscription, one-time purchase

**MRBT Pro** adds Claude AI running invisibly inside the sheet — smart categorisation, monthly financial insights, natural language queries, and anomaly alerts — with no API key required from the buyer.

### Pricing

| Version | Price | Key addition |
|---|---|---|
| MRBT Standard | £14.99 | Full automation, UK bank CSV import |
| MRBT Pro | £34.99 | Claude AI categorisation + insights |
| MRBT Pro Upgrade | £15.00 | For existing Standard customers |

### The unique differentiator

Zero other Etsy budget trackers have built-in CSV import for UK banks. Every competitor is US-focused or generic. This is the core positioning of the entire product and should appear prominently in all listing titles, descriptions, and marketing.

**Supporting research (YouGov 2026 / Etsy audit):**
- 51% of UK adults now budget — up from 46% in 2025
- 39% of UK budgeters use spreadsheets vs only 9% who use apps
- 63% of Britons expect to cut spending in 2026
- 50M+ active UK digital bank accounts (Monzo, Chase, Starling, Barclays, Revolut)
- 0 other Etsy listings with UK-specific bank CSV import

---

## Repository contents

```
madeready-site/
├── index.html      ← Single-page marketing site (all HTML, CSS, JS in one file)
└── README.md       ← This file
```

The entire site is a self-contained HTML file. No build step, no dependencies, no npm, no framework.

---

## Site sections

| Section | ID | Description |
|---|---|---|
| Hero | — | Headline, UK bank pills, trust signals, stat eyebrow |
| Sheet preview | — | Interactive 5-tab spreadsheet mockup (clickable tabs) |
| UK differentiator banner | — | 4 research-backed stats making the competitive case |
| How it works | `#how-it-works` | 5-step setup walkthrough + MRBT Pro AI flow diagram |
| Features | `#features` | 9 feature cards (Standard + Pro) |
| What is a CSV? | `#csv` | Plain English CSV explainer + per-bank download instructions |
| Security | `#security` | CSV safety explainer + security checklist callout |
| Standard vs Pro | `#comparison` | Full feature comparison table |
| Pricing | `#pricing` | Two pricing cards + upgrade path |
| Reviews | `#reviews` | Three testimonials + 3 research-backed stats |
| FAQ | `#faq` | 8 questions including "What is a CSV?" |
| CTA | `#get-it` | Etsy buy button |
| Footer | — | Links, contact, bank tags |

---

## Tech

- Pure HTML, CSS, and vanilla JS — no framework, no build tool
- Google Fonts: DM Sans, Inter, JetBrains Mono
- Dark mode default, light mode toggle (preference saved to localStorage)
- Responsive at 760px breakpoint (hamburger menu with SVG icons)
- Interactive sheet mockup — 5 clickable tabs with formula bar updates
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

## Full product roadmap

### ✅ Phase 0 — Foundation (Complete)

Infrastructure and brand established before any product is built.

- [x] Brand name decided: **Made Ready Co**
- [x] Domain registered: **madeready.co** (Namecheap)
- [x] Email forwarding: roland@madeready.co → rolandjlevy@gmail.com (Namecheap)
- [x] Brand Google account created: madeready.co@gmail.com
- [x] GitHub account created: madereadyco
- [x] GitHub repo created: madeready-site
- [x] Marketing site built and deployed via GitHub Pages
- [x] Product named: **Made Ready Budget Tracker (MRBT)**
- [x] Two-tier pricing confirmed: Standard £14.99 / Pro £34.99
- [x] Upgrade path confirmed: £15 for existing Standard customers

---

### 🔨 Phase 1 — Build MRBT Standard (Current phase)

Build the core Google Sheet that becomes the £14.99 product.

#### Sheet architecture

- [ ] Create master Google Sheet in madeready.co@gmail.com account
- [ ] Tab 1: ⚙️ Setup
  - [ ] Income & settings section (monthly income, currency, budget period)
  - [ ] Spending categories list — ordered by UK priority: Rent/Mortgage, Energy & Utilities, Groceries, Transport, Subscriptions, Dining Out, Shopping, Healthcare, Savings, Investments
  - [ ] Keyword → Category mapping table (80+ UK merchants pre-loaded)
  - [ ] Payday setting: calendar month OR custom payday date
- [ ] Tab 2: 💳 Transactions
  - [ ] Date / Account / Description / Category (dropdown) / Amount columns
  - [ ] Data validation on Category column referencing Setup list
  - [ ] CSV import sidebar (Apps Script) — Monzo, Chase UK, Starling, Barclays, Revolut, Generic
- [ ] Tab 3: 📊 Dashboard
  - [ ] QUERY-powered budget vs actual by category
  - [ ] Safe-to-spend hero metric
  - [ ] 50/30/20 budget split calculator section
  - [ ] Monthly spending charts
  - [ ] Conditional formatting (red = over budget, green = under)
- [ ] Tab 4: 📈 Net Worth
  - [ ] Assets tracker (current account, savings, pension, investments)
  - [ ] Liabilities tracker (credit cards, loans, mortgage)
  - [ ] Net worth total + month-on-month change
  - [ ] Savings Goals section (3–5 named goals with progress and months-to-target)
- [ ] Tab 5: 🤖 Automations
  - [ ] Automation settings panel
  - [ ] CSV import log
  - [ ] Trigger status display

#### Apps Script automation layer

- [ ] Custom menu: 🤖 Made Ready Budget
- [ ] Auto-categorise function (keyword matching against Setup rules)
- [ ] CSV bank formatter with sidebar UI (6 bank presets)
- [ ] Clean descriptions utility (whitespace, uppercase normalisation)
- [ ] Overnight time-based trigger for auto-categorisation
- [ ] onOpen() menu builder

#### Product improvements from research (Phase 1)

These came directly from YouGov 2026 / Etsy competitive audit:

- [ ] UK-priority category ordering (Energy first, not alphabetical)
- [ ] Revolut CSV preset added to import sidebar
- [ ] 50/30/20 calculator tab added to Dashboard
- [ ] Payday-to-payday budget mode (toggle in Setup)

#### Delivery assets

- [ ] ReadMe PDF (Canva) — 6-step visual setup guide
- [ ] Loom setup video — 90 seconds, captions on, no audio required
- [ ] Second Loom video — "real month" demo: import CSV → categorise → read dashboard
- [ ] Make-a-copy link configured (File → Share → Publish as template)
- [ ] Delivery PDF wrapping the Make-a-copy link (the actual Etsy download)

---

### 🏪 Phase 2 — Etsy Launch

Get MRBT Standard live and generating its first sales.

- [ ] Etsy seller account fully verified (Made Ready Co)
- [ ] Etsy listing 1: MRBT Standard £14.99
  - [ ] Title: Budget Tracker Google Sheets UK | Automated Expense Tracker | Monzo Chase Starling Barclays Revolut | Personal Finance Template
  - [ ] All 13 tags filled (validated against eRank search volume)
  - [ ] 7–10 listing images (hero: MacBook marble desk, lifestyle, feature callouts, bank logos)
  - [ ] Demo video uploaded to listing
  - [ ] First 160 characters of description keyword-optimised
- [ ] Etsy Ads: £1–2/day for first 30 days to seed ranking signals
- [ ] Seed purchases from friends/family for first reviews
- [ ] Post in r/UKPersonalFinance — genuinely helpful CSV budgeting post
- [ ] TikTok/Reels video 1: "I built a spreadsheet that sorts your bank statements"
- [ ] TikTok/Reels video 2: "How much did I spend on coffee last month?" — dashboard reveal
- [ ] TikTok/Reels video 3: "Stop doing your budget manually" — problem/solution/CTA

**Launch trigger:** All delivery assets complete + listing images shot + at least 1 test purchase confirms the download flow works end to end.

---

### 🤖 Phase 3 — MRBT Pro (AI layer)

Build the £34.99 product. Only start this after MRBT Standard has validated demand (target: 10+ sales).

#### Vercel API endpoint

- [ ] Create GitHub repo: madeready-apfe-api
- [ ] Next.js project with API routes:
  - [ ] `/api/categorise` — sends transaction descriptions to Claude, returns categories
  - [ ] `/api/insight` — sends dashboard data, returns monthly plain-English insight
  - [ ] `/api/query` — receives natural language question, returns answer
  - [ ] `/api/anomalies` — scans transactions, returns flagged items
- [ ] Shared Claude API client (`lib/claude.ts`)
- [ ] Middleware: secret token validation + rate limiting
- [ ] Deploy to Vercel
- [ ] Connect custom domain: apfe.madeready.co (CNAME in Namecheap)
- [ ] Environment variables set in Vercel: ANTHROPIC_API_KEY, APFE_SECRET_TOKEN

#### Pro sheet additions

- [ ] Smart Categorise button — calls `/api/categorise` via Apps Script UrlFetchApp
- [ ] Monthly Insight button — calls `/api/insight`, writes result to Dashboard
- [ ] Natural Language Query cell — calls `/api/query`, displays plain-English answer
- [ ] Anomaly Alerts section — calls `/api/anomalies`, displays flagged items
- [ ] Secret token embedded in Apps Script (not visible in any cell)

#### Pro Etsy listings

- [ ] Listing 2: MRBT Pro £34.99
- [ ] Listing 3: MRBT Pro Upgrade £15.00 (for existing Standard customers)
- [ ] Upgrade prompt inside Standard sheet: banner cell linking to Etsy upgrade listing

**Launch trigger:** 10+ Standard sales + Vercel endpoint tested and stable.

---

### 📈 Phase 4 — Product improvements from research (v2)

These came from the YouGov 2026 / Reddit / Etsy research. Build after Pro is live.

- [ ] Savings Goals tab (🎯 Goals) — named goals, progress bars, months-to-target formula
- [ ] Debt Payoff tab (💳 Debt) — Snowball and Avalanche payoff calculators
- [ ] Payday-to-payday mode (if not shipped in Phase 1)
- [ ] Subscription tracker — list recurring payments, flag ones unused in 30+ days
- [ ] Update site to reflect new features
- [ ] Bump Standard price to £17.99 / Pro to £39.99 at v2 launch

---

### 👥 Phase 5 — Second product: MRBT Couples Edition

Research confirmed couples budget trackers are one of Etsy's top-selling finance products.

- [ ] Couples sheet variant — two income streams, shared expense dashboard, split view
- [ ] Etsy listing: MRBT Couples £19.99
- [ ] Separate listing images (lifestyle: two people, shared screen)
- [ ] Consider bundle: Standard + Couples at £27.99

---

### 🌐 Phase 6 — Move to Vercel + own domain

Move off GitHub Pages once revenue justifies it (target: £500/month consistent).

- [ ] Connect madeready.co to Vercel (A record + CNAME in Namecheap)
- [ ] madeready-site repo connected to Vercel for auto-deploy on push
- [ ] Google Workspace (hello@madeready.co) — £5.20/month — replaces email forwarding
- [ ] Add Google Analytics to site
- [ ] Consider Shopify migration at this stage to capture customer email addresses

---

### 🏢 Phase 7 — Made Ready Co as a product studio

MRBT validates the model. Future products under the Made Ready Co brand.

Future products (all researched and scoped):
- **ContractBot** — WhatsApp voice-to-contract for UK tradespeople
- **Mole** — household resale intelligence app (getmole.com)
- **Beacon Suite** — B2B SaaS for UK SEO agencies with AEO tooling
- **The Presence Project** — smartphone dependency behaviour-change app
- **ComplianceKit** — construction RAMS/CDM two-sided platform

---

## Related repos

| Repo | Description | Status |
|---|---|---|
| `madeready-site` | This repo — marketing website | ✅ Live |
| `madeready-apfe-api` | MRBT Pro AI backend (Next.js / Vercel) | ⏳ Phase 3 |

---

*© 2025 Made Ready Co · madeready.co · roland@madeready.co*
