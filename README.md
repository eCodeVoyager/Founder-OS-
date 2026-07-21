# Founder OS

A single-file personal operating system for running a company, a degree, a health
protocol and a study-abroad campaign at the same time — without any of them
quietly falling off the edge.

**Live:** https://ecodevoyager.github.io/Founder-OS-/

No build step, no dependencies, no server, no analytics. One HTML file.

---

## Your data never leaves your browser

This repository is public, so it deliberately ships **empty**. There are no
names, amounts, medication names, document numbers or scores in the source.

Everything you type is written to `localStorage` under the key `founder-os.v3`
on the device you typed it on. It is not uploaded anywhere, because there is
nowhere for it to go — the page makes zero network requests after it loads.

Consequences worth knowing:

- Data is **per-browser and per-device**. Chrome on your laptop and Chrome on
  your phone are two separate copies.
- Clearing site data, or "clear cookies and site data", erases it.
- Private / incognito windows discard it when the window closes.

So: hit **Export** now and then. It downloads a JSON backup you keep yourself.
**Import** restores it, on any device.

---

## What's in it

| Tab | What it does |
|---|---|
| **Dashboard** | KPI strip, executive numbers, quarterly OKRs, weekly time budget, and a risk monitor that raises its own flags from your logged data |
| **Kanban** | Five columns, drag and drop, eight colour-coded tracks, priorities, due dates with live overdue counters. Ships with a starter board built from the research tracker |
| **Study Abroad** | 38-program application CRM with per-row status and notes, filters, a deadline timeline with countdowns, a document vault checklist, exam-prep targets and a visa funds-fit model |
| **Health** | Daily sleep / mood / anxiety / deep-work log, configurable medication checklist, 14-day sparklines, log streak, CSV export |
| **Finance** | Monthly ledger with derived net and save rate, funds-legitimacy checklist, savings goal with an ETA |
| **Build & Ship** | RenderKit validation funnel with derived conversion rates, remote-job pipeline, university semester blocks |
| **Weekly Review** | Wins / problems / top three / verdict, appended to a dated history |

### Derived, not typed

Anything the app can work out, it works out: cash runway, savings in EUR,
monthly net and save rate, savings-goal ETA, funds seasoning in months,
reply / close / end-to-end conversion rates, 14-day health averages, log
streak, days to every deadline, and the automatic risk flags.

### Automatic risk flags

The risk monitor watches your own data and speaks up on its own:

- sleep under 6h on 3+ of the last 7 logged days
- anxiety above 7 on 3+ of the last 7 logged days
- any kanban card past its due date
- three or more cards stuck in Blocked
- funds seasoned under three months

---

## Study-abroad data

The shortlist, gates, tuition figures and timeline are compiled from a research
tracker current to **2026-07-21**. All of it is public university information.

Windows marked *proj.* are prior-cycle patterns projected forward one year —
they are planning aids, **not** confirmed dates. Verify on the official page
before you act on any of them. Application calls move.

---

## Running it

Open `index.html`. That's the whole thing.

To edit: the file is one document — CSS at the top, markup in the middle,
script at the bottom. Reference data (columns, tracks, the starter board, the
CRM shortlist, the timeline, the checklists) sits in clearly-marked `const`
blocks near the top of the script, so you can retune the content without
touching the machinery.

## Keyboard

- `n` — new kanban card, while the Kanban tab is open
- double-click or `Enter` on a card — edit it

## Browser support

Any current browser. Uses `<dialog>` and CSS `color-mix` — both baseline
since 2023. No other modern-API dependencies.

## License

MIT
