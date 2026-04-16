# BO Portfolio Tracker

A browser-based portfolio management tool for Bangladesh stock market (DSE/CSE) investors holding multiple BO (Beneficiary Owner) accounts. Consolidates holdings across brokerage accounts into a single dashboard with gain/loss calculations, asset allocation charts, dividend tracking, and historical performance records.

Built by **Mashrup Hasan** at [Nogori.ai](https://nogori.ai).

---

## Features

**Multi-account consolidation** — Manage multiple BO accounts side by side. The consolidated view merges all holdings across accounts with weighted average cost calculations and unified P&L reporting.

**PDF statement import** — Import portfolio statements from LankaBangla Securities, Royal Capital, and Shanta Securities. Accounts are detected automatically by BOID, so prices, shares, cost basis, cash balances, P&E ratios, and dividends all sync in one step.

**Manual trade entry** — Buy, sell, or update any holding manually. Supports stocks, mutual/unit funds, and cash positions.

**Dividend tracking** — Records cash dividends per account with record dates, payment dates, holding quantities, and entitled amounts.

**Historical performance** — Every update is saved as a timestamped snapshot. Each holding and each account has its own price and P&L history chart.

**Charts and analytics** — Asset allocation donut chart, broker allocation bar chart, top 10 holdings by market value, gain/loss by holding, and historical P&L line charts.

**Settings and profile** — Customise the display name, app title, and profile picture shown in the sidebar. Add, edit, or remove BO accounts at any time from the Settings panel.

**Export and print** — Export all holdings to CSV or print the current view directly from the browser.

**Undo** — A single-level undo is available for the most recent destructive action.

---

## Getting Started

No installation, build tools, or backend is required. The entire application is a single HTML file.

1. Download `BO_Portfolio_Tracker.html`
2. Open it in any modern browser (Chrome, Firefox, Edge, Safari)
3. Go to **Settings** (bottom-left of the sidebar) to set up your profile and add your BO accounts
4. Import PDF statements or add holdings manually via **+ Add Trade**

All data is saved to your browser's `localStorage` automatically.

---

## Usage Guide

### Setting up accounts
Open **Settings** from the sidebar. Under **BO Accounts**, enter the account name, short label, account number, BOID, and accent colour for each brokerage account. The BOID is required for automatic PDF detection.

### Importing PDF statements
Click **Import PDFs** in the sidebar or topbar. Select one or more statement PDFs. The app matches each file to the correct account by BOID, shows a preview of the detected changes, and applies them when you confirm.

### Adding trades manually
Click **+ Add Trade**. Select the account, enter the ticker, shares, cost basis, and current price. The action field supports Buy (adds shares), Sell (reduces shares), and Update/Replace (overwrites the holding entirely).

### Viewing history
Click any holding name in the holdings table to open its detail view, which includes price and P&L history charts and a full log of every recorded update.

### Exporting data
Click **Export CSV** to download all holdings across all accounts as a single CSV file.

---

## Supported Brokerages

The PDF parser currently supports statement formats from:

- LankaBangla Securities (LBSL)
- Royal Capital Ltd
- Shanta Securities

Additional brokerages can be added by extending the parser and registering the account BOID.

---

## Data Storage

All data is stored in the browser's `localStorage` under the key `bo_tracker_portfolios_v4`. No data is sent to any server. Clearing browser cache or switching browsers will result in data loss — use **Export CSV** regularly as a backup, or integrate with a backend (see below).

### Planned: cloud sync
A Supabase or Google Sheets backend integration is planned to enable persistent, cross-device access without relying on `localStorage`.

---

## Tech Stack

- Vanilla HTML, CSS, and JavaScript — no frameworks or build tools
- [Chart.js](https://www.chartjs.org/) for charts
- Google Fonts (DM Serif Display, DM Mono, DM Sans)
- Browser `localStorage` for persistence

---

## License

Private. All rights reserved. Built on behalf of Nogori.ai.

---

## Contact

**Mashrup Hasan**  
Email: [mashruphasan@gmail.com](mailto:mashruphasan@gmail.com)  
Phone: 01614367984  
Organisation: [Nogori.ai](https://nogori.ai)
