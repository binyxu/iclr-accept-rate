# ICLR Accept Rate Explorer

> Search any research topic and instantly see its **acceptance rate**, **oral rate**, and year-over-year trend at ICLR — from 2020 to 2026.

**[Live Demo →](https://binyxu.github.io/iclr-accept-rate/)**

---

## What it does

Type a keyword (e.g. `diffusion`, `graph neural network`) and the tool will:

- Filter all ICLR papers whose **title / abstract / keywords / TL;DR** match
- Show the **acceptance rate** and **oral rate** for that topic, compared to the venue average
- Plot a **year-over-year trend line** (2020–2026)
- Display a **leaderboard** of the most-searched topics and their rates
- Support **Recent 3Y / 5Y** aggregated views with pooled statistics

## Search syntax

| Syntax | Meaning | Example |
|---|---|---|
| Plain text | substring match | `diffusion model` |
| Comma | OR (any term) | `diffusion, flow matching` |
| `OR` keyword | OR (any term) | `symbolic regression OR equation discovery` |
| `AND` keyword | both terms must match | `diffusion AND language` |
| `/regex/` | full regex | `/graph.*(network\|transformer)/i` |
| Mixed | combine freely | `diffusion AND generation, /symbolic.reg\|equation/` |

## Screenshots

| Search & stats | Year-over-year trend | Leaderboard |
|---|---|---|
| Search a keyword → see accept rate vs venue average | Hover the trend line to see per-year breakdown | Most searched topics ranked by acceptance rate |

## Data sources

- Paper metadata: [papercopilot/paperlists](https://github.com/papercopilot/paperlists)
- Years covered: **ICLR 2020 – 2026**
- Status labels used: `Oral` / `Spotlight` / `Poster` → accepted; `Reject` / `Withdraw` → not accepted
- Acceptance rate = (Oral + Spotlight + Poster) / total submissions
- Oral rate = Oral / (Oral + Spotlight + Poster)

## Tech stack

- Vanilla HTML / CSS / JS — zero dependencies, single file
- Google Apps Script as a lightweight backend (leaderboard & page-view tracking)
- Data fetched at runtime from GitHub raw JSON

## Local development

No build step needed. Just open `index.html` in a browser, or serve it with any static file server:

```bash
npx serve .
# or
python3 -m http.server 8080
```

## Star history

If you find this useful, a ⭐ on the repo helps others discover it!

---

*Data is best-effort. Always cross-check with the [official ICLR OpenReview](https://openreview.net/group?id=ICLR.cc) for authoritative numbers.*
