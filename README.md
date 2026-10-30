# Hisaab
https://splid.unfo.workers.dev/
<div align="center">

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://readme-typing-svg.demolab.com?font=Press+Start+2P&size=44&color=F2EFE8&center=true&vCenter=true&width=640&height=84&repeat=false&pause=1000&lines=HISAAB">
  <img src="https://readme-typing-svg.demolab.com?font=Press+Start+2P&size=44&color=0C0C0D&center=true&vCenter=true&width=640&height=84&repeat=false&pause=1000&lines=HISAAB" alt="HISAAB" />
</picture>

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://readme-typing-svg.demolab.com?font=Press+Start+2P&size=13&color=7DDC82&center=true&vCenter=true&width=640&height=40&duration=2800&pause=1300&lines=WHO+OWES+WHOM,+AT+A+GLANCE.;NO+SIGN-UP.+NO+SERVER.;SPLIT+IT.+SETTLE+IT.+FORGET+IT.">
  <img src="https://readme-typing-svg.demolab.com?font=Press+Start+2P&size=13&color=226A28&center=true&vCenter=true&width=640&height=40&duration=2800&pause=1300&lines=WHO+OWES+WHOM,+AT+A+GLANCE.;NO+SIGN-UP.+NO+SERVER.;SPLIT+IT.+SETTLE+IT.+FORGET+IT." alt="Who owes whom, at a glance. No sign-up. No server. Split it. Settle it. Forget it." />
</picture>

<br/>

[![Open live demo](https://img.shields.io/badge/PRESS_START-OPEN_LIVE_DEMO-3fae44?style=for-the-badge&labelColor=0c0c0d)](https://splid.unfo.workers.dev/)

<br/>

![Stars](https://img.shields.io/github/stars/unfotable/splid?style=flat-square&labelColor=0c0c0d&color=3fae44&logo=github&logoColor=white)
![Last commit](https://img.shields.io/github/last-commit/unfotable/splid?style=flat-square&labelColor=0c0c0d&color=3fae44&logo=git&logoColor=white)
![Backend](https://img.shields.io/badge/backend-none-282420?style=flat-square&labelColor=0c0c0d)
![Build step](https://img.shields.io/badge/build_step-none-282420?style=flat-square&labelColor=0c0c0d)
![Data](https://img.shields.io/badge/data-stays_in_your_browser-282420?style=flat-square&labelColor=0c0c0d)

▀▄▀▄▀▄▀▄▀▄▀▄▀▄▀▄▀▄▀▄▀▄▀▄▀▄▀▄

</div>

<h3 align="center">░▒▓ &nbsp;ABOUT&nbsp; ▓▒░</h3>

<p align="center">
<b>Hisaab</b> (<i>हिसाब</i>, "the accounts") is a lightweight expense splitter for groups: trips, flatmates, dinners, anything shared.<br/>
Log an expense, pick a split, and a live balance graph shows exactly who owes whom.
</p>

```
╔═[ HISAAB ]════════════════════════════════╗
║  GENRE   : Expense splitter               ║
║  SPLITS  : Equal / custom / percent       ║
║  GRAPH   : Live SVG: direct + simplified  ║
║  BACKEND : None                           ║
║  BUILD   : None                           ║
║  STORAGE : localStorage (your browser)    ║
║  STACK   : React + htm + Tailwind         ║
╚═══════════════════════════════════════════╝
```

<br/>

<h3 align="center">░▒▓ &nbsp;FEATURES&nbsp; ▓▒░</h3>

- 👥 **Groups & members:** create any number of groups, add or remove people at any time
- ⚖️ **Flexible splits:** equal, custom amounts, or percentages, set per expense
- 🏷 **Categories:** food, travel, stay and misc, each with its own icon and color
- 🕸 **Live balance graph:** an animated SVG of who owes whom, in **Direct** (every real debt) and **Simplified** (fewest payments) views
- 🤝 **Settle up:** record full or partial payments; the graph and history update instantly
- 🧾 **Activity timeline:** a chronological log of every expense and settlement, editable and deletable
- 🧭 **Guided tour:** a coach-mark walkthrough on seeded demo data (the "Goa Trip" group)
- 🔒 **Zero backend:** everything lives in `localStorage`; nothing leaves the browser

<br/>

<h3 align="center">░▒▓ &nbsp;HOW IT SIMPLIFIES&nbsp; ▓▒░</h3>

Every expense updates a pairwise ledger between members, and settlements subtract from it. From that ledger Hisaab derives three things: the **direct edges** (real person-to-person debts), each member's **net balance**, and the **simplified payments**, the fewest transfers that zero everyone out.

A tiny example (illustrative numbers):

```
DIRECT (2 payments)            SIMPLIFIED (1 payment)

  A --500--> B --500--> C        A ------500------> C

  net balance:  A -500   B 0   C +500
```

The simplified view uses a greedy pass: sort debtors and creditors by amount, match the largest debtor with the largest creditor, repeat.

| Concept | Meaning |
| --- | --- |
| **Group** | Members, expenses and settlements together (e.g. "Goa Trip") |
| **Expense** | An amount, a payer, a category and a split across members |
| **Split** | `equal`, `custom` or `pct` (percentage) |
| **Settlement** | A recorded payment between two members, full or partial |
| **Net balance** | What a member is owed (+) or owes (−) across the group |

<br/>

<h3 align="center">░▒▓ &nbsp;FLOW&nbsp; ▓▒░</h3>

```mermaid
flowchart TD
    A([Open app]) --> B{Existing groups?}
    B -- No --> C[Demo group auto-seeded]
    B -- Yes --> D[Home: list of groups]
    C --> D
    D --> E[Open a group]
    E --> F[Balance tab]
    F --> G[Add expense]
    F --> H[Settle up]
    F --> I[Switch Direct / Simplified]
    G --> J[Graph and balances update instantly]
    H --> J
    I --> J
    J --> K[Activity tab: log, edit, delete]
    D --> M[Make it yours: wipe demo, create your own group]

    classDef start fill:#3fae44,stroke:#3fae44,color:#0c0c0d
    classDef ink fill:#282420,stroke:#f2efe8,color:#f2efe8
    classDef decide fill:#19191c,stroke:#8b8b92,color:#ededf0
    class A start
    class B decide
    class C,D,E,F,G,H,I,J,K,M ink
```

<br/>

<h3 align="center">░▒▓ &nbsp;QUICK START&nbsp; ▓▒░</h3>

Clone or download the project, then open `index.html` in a browser, or serve the folder with any static file server:

```bash
# Option 1: just open it
open index.html

# Option 2: serve it locally
npx serve .
```

That's it. On first load the app seeds a demo group ("Goa Trip") so there's something to explore right away.

```
.
├── index.html   # entry point: CDN script tags, Tailwind config and the app shell
├── app.js       # components, state, money math, demo data
├── styles.css   # form primitives, keyframe animations, range-input styling
└── logo_s.svg   # logo
```

<br/>

<h3 align="center">░▒▓ &nbsp;MAKE IT YOURS&nbsp; ▓▒░</h3>

- 🎨 **Colors & fonts:** edit the `tailwind.config` block in `index.html`
- 🏷 **Categories:** add or edit entries in the `CATS` object in `app.js`
- 🧑 **Avatar palette:** the `AV` array in `app.js` controls member colors
- 🧭 **Tour copy:** edit `TOUR_STEPS` in `app.js` to change the onboarding text

<br/>

<h3 align="center">░▒▓ &nbsp;DATA &amp; PRIVACY&nbsp; ▓▒░</h3>

> Hisaab stores everything under a single `localStorage` key, `hisaab.v2`. There is no server, no account and no network request involving your data. Clearing the browser's storage for the page resets the app to the seeded demo.

<br/>

<div align="center">

▀▄▀▄▀▄▀▄▀▄▀▄▀▄▀▄▀▄▀▄▀▄▀▄▀▄▀▄

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://readme-typing-svg.demolab.com?font=Press+Start+2P&size=12&color=7DDC82&center=true&vCenter=true&width=520&height=34&duration=2200&pause=1600&lines=PRESS+START;HAPPY+SPLITTING">
  <img src="https://readme-typing-svg.demolab.com?font=Press+Start+2P&size=12&color=226A28&center=true&vCenter=true&width=520&height=34&duration=2200&pause=1600&lines=PRESS+START;HAPPY+SPLITTING" alt="Press start. Happy splitting." />
</picture>

Built by [**@unfotable**](https://github.com/unfotable) &nbsp;·&nbsp; Also made: [**SYNCRO**](https://github.com/unfotable/syncro), notes, sheets and boards in one tab

</div>
- **Categories** — add or edit entries in the `CATS` object in `app.js`
- **Avatar palette** — the `AV` array in `app.js` controls member colors
- **Tour content** — edit `TOUR_STEPS` in `app.js` to change the onboarding copy
