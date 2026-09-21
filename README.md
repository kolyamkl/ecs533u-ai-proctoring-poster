# AI Proctoring in High-Stakes Assessments - A3 poster layout

Layout template for **ECS533U Introduction to AI** (Queen Mary University of London),
Lab Week 1, Exercise 1.3. Group submission.

Case study: HackerRank's Proctor Mode, an automated AI proctoring system used in
technical hiring assessments and directly transferable to online exams.

> This repository contains the **layout only**. Every content box is an empty, labelled
> placeholder for the group to fill in. No statistics, quotes or references are invented here.

## Files

| File | What it is |
|---|---|
| `poster-layout.html` | The deliverable. Self-contained A3 portrait page, inline CSS, `@page { size: A3; margin: 0 }`. Open in a browser and print or export to PDF. |
| `PLACEHOLDERS.md` | Inventory of every placeholder: ID, section, type, word budget. Use it as the fill-in checklist. |
| `untitled.pen` | pen.dev canvas source for the same design. |

## Printing

Open `poster-layout.html` in Chrome, then Print. Set **A3**, **Portrait**,
**Scale 100% / Actual size**, and **Background graphics ON**. Save as PDF.

## Layout and reading flow

The poster reads top to bottom in one column so a presenter can walk it left hand down
the sheet. The header carries the admin block, a two-line 48 pt title and the group names.
Section 1 sets up the system: a short definition beside a "where used" note, then a
Before / During / After flow diagram with a PEAS inset, so the machinery is visual rather
than described. Section 2 is the largest block and opens with a dark full-width statistic
band, the single thing to point at first, followed by a 2x2 grid of issue cards. Each issue
carries a code, a colour and an icon (E1 to E4) that is reused as a chip in the Section 3
table and as a coloured tab on the matching Section 4 recommendation, so "issue, gap, fix"
can be traced across three sections by colour alone. The disagreement callout sits directly
above the references as the hand-off into Q&A.

## Design system

- **Grid**: 12 mm margins, 4.2 mm gutters, single column, seven rows.
- **Type**: Archivo (display) and Inter (body). Title 48 pt, section headings 26 pt,
  main prose 14 pt, dense secondary text 11 pt, references 9.5 pt.
- **Colour**: navy `#14456E` primary, amber `#C2600B` accent, neutral greys.
  The four issue codes use a colour-blind safe set, and each is triple-coded by
  colour **and** icon **and** number so it never depends on hue alone:
  E1 `#0072B2`, E2 `#B45F06`, E3 `#04786A`, E4 `#7B4EA3`.
- No em dashes anywhere in the text.

## Space allocation

| Area | Share | Brief asked for |
|---|---|---|
| Header | 17.0% | ~10% |
| 1 System Overview | 16.9% | ~15% |
| 2 Ethical Analysis | 26.8% | ~30% |
| 3 Current Responses and Gaps | 14.3% | ~20% |
| 4 Future Improvements | 11.6% | ~13% |
| Where we disagreed | 4.0% | ~5% |
| References | 9.4% | ~7% |

Section 2 remains the largest block by a wide margin. See `PLACEHOLDERS.md` for why the
header runs over and the word budgets run under the brief's figures.
