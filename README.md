# Founder OS

A single-file personal operating system for running companies, a degree, a health
protocol and a study-abroad campaign at once — without any of them quietly
falling off the edge.

**Live:** https://ecodevoyager.github.io/Founder-OS-/

18 modules, hand-rolled SVG charts, no build step, no dependencies, no server,
no analytics, no network requests. One HTML file.

---

## Your data never leaves your browser

This repository is public, so it deliberately ships with **no personal data**.
Everything you enter is written to `localStorage` on the device you typed it on.

Storage picks a backend once at boot, in this order:

1. `window.storage` — the Anthropic artifact host, when running there
2. `localStorage` — any normal browser: `file://`, GitHub Pages, anywhere
3. memory — private mode or blocked cookies; **session only**

The footer shows which one is live. If it says `session only`, nothing is being
saved — export before closing the tab.

Data is per-browser and per-device: your laptop and your phone hold two separate
copies. Clearing site data erases it. So **Settings → Export** now and then; the
JSON it produces restores through **Settings → Import** on any device.

---

## Modules

**Command** — Dashboard, Today (weekly time blocks), Kanban, Calendar

**Work** — Projects, Deep Work sessions, Finance, Jobs

**Life** — Study Abroad, University, Health, Journal, Reading, Networking

**Review** — CEO Review, Monthly, Vision, Settings

### Kanban

Six columns: Backlog → This Month → This Week → Doing → Blocked → Done.
Drag between and within columns on desktop; the ◀ ▶ buttons on each card do the
same on touch, where HTML5 drag-and-drop does not exist. Card order is explicit
and survives a reload. Cards carry a project, a due date with a live countdown,
and a note. Overdue cards read `12d late` rather than a negative number.

### Study Abroad

A row per target: country, university, program, exam required, admission
mechanism, status, priority, deadline and notes. Sorted by priority, with
countdowns. The exam-prep block tracks one shared syllabus across every entrance
test.

---

## Loading the prepared dataset

`my-data.json` (kept out of this repo — it is your data) holds a compiled
starting state: 39 study-abroad targets, 28 kanban cards, 20 calendar deadlines,
6 projects and a weekly plan. Load it with **Settings → Import JSON**.

Import overwrites every module present in the file, so export a backup first if
you already have data worth keeping.

Everything in it is compiled from research current to **2026-07-21**. Dates
described as projected are prior-cycle patterns carried forward a year — they
are planning aids, **not** confirmed calls. Verify on the official page before
acting on any of them.

---

## Running it

Open `index.html`. That is the whole thing.

To edit: CSS at the top, markup in the middle, script at the bottom.
`DEFAULTS` defines every module's shape, `NAV` the sidebar, `KANBAN_COLS` the
board, and `VIEW_RENDERERS.<key>` renders each view.

## Keyboard

Single-letter shortcuts jump between views — the sidebar shows each one.
`Enter` on a focused kanban card opens it.

## Browser support

Any current browser.

## License

MIT
