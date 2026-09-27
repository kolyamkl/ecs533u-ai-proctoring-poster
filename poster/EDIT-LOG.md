# Poster edit log

File edited: `poster/source/poster-v5.pen` (frame `V5 · Flow + matrix`, A3 portrait, 1123 x 1587 px).
Exports regenerated: `poster/ecs533u-poster-a3.png` (2x), `poster/ecs533u-poster-a3.pdf`.

No change to the grid, palette, fonts or type hierarchy. Every edit below stays inside the
existing design system: Space Grotesk for display, IBM Plex Sans for body, red `$p-red`
accent, paper `#F1F0E9`.

---

## Edit 1: Section 01 layout

Section 01 is now a two column row inside the same 1011 px content width:

| Zone | Width | Share |
|---|---|---|
| Figure column (illustration, 10 callouts, caption) | 607 px | 60% |
| Gutter | 50 px | 5% |
| Right column (Blocks A and B) | 354 px | 35% |

Inside the figure column: callout column 155 px on the left, the illustration, callout column
173 px on the right.

**The illustration was enlarged** (follow-up request). The original asset is a 1024 x 1024
JPEG that is mostly empty background: the drawing itself only occupies 53% of its width and
64% of its height, and the background is within 1 to 3 levels of the poster's paper colour,
so the placed rectangle was always much larger than the drawing and its edge was faintly
visible. A cropped, transparent-background PNG was generated from it
(`images/hero-figure.png`, 550 x 656, background keyed out by luminance, original JPEG kept
in the repo) so the placed box is now exactly the drawing.

The drawing is now 214 x 255 px on the sheet, against 143 x 171 px in the previous committed
version of this poster. That is 50% larger in each direction, and the invisible background
rectangle is gone.

## Edit 2: Source tags removed

All eight `BOTH` / `EXAMS` / `HACKERRANK` tags are gone. The tag text nodes were reused as
the new description lines, so nothing was left orphaned in the file.

## Edit 3: Callout labels and descriptions

Ten callouts, all of them fitting without crossing leader lines and without going below the
poster's existing minimum type size:

- Label: 15 px medium (unchanged from the original label size).
- Description: 11 px regular, `$p-grey`, directly under the label, 3 px apart.
  (The deleted tags were 10 px, so the smallest type on the poster did not get smaller.)

Distribution: four callouts left, five right, one below the figure. Leader lines were
recomputed so each label's vertical order matches its anchor's vertical order, which is what
keeps them from crossing.

| Label | Description | Position |
|---|---|---|
| Webcam face tracking | image capture every 2-3 seconds | left |
| Multiple face detection | flags a second person in frame | left |
| Gaze tracking | look away then type | left (new) |
| Keystroke rhythm analysis | typing bursts, pauses, mass deletions | left |
| Room scan | 360 degree sweep before the start of the test | right (kept red) |
| Full-screen lock / OS level lock | leaving full screen or test application is forbidden | right (renamed) |
| Tab-switching tracking | every focus change is timestamped | right |
| Screen capture | every 15s, every 5s once flagged | right (new) |
| Copy-paste logging | external paste blocked and recorded, internal allowed | right |
| Phone detection | flagged even if partly visible | below figure |

Two labels were also normalised to the wording in the brief's table: "Multiple-face
detection" to "Multiple face detection", and "Tab-switch tracking" to "Tab-switching
tracking".

## Edit 4: Two blocks in the right-hand column

Both use the poster's existing small-block treatment: heading, hairline rule, content.

**Block A, "Why this counts as AI"** (39 words). Four rows, red bold term at 13 px in an
aligned 86 px column, description alongside, closing line in 12 px italic.

The four bullets originally specified for this block (object detection, gaze estimation,
behavioural classifier, ML plagiarism model) were **replaced after review**: they restated
the ten callouts in the figure directly beside them, just under different names, so the block
paid for a third of the section's width without adding anything a reader could not already
see. It now carries the PEAS specification instead, which is the Lab 1 vocabulary and is the
one thing the figure cannot show:

| Term | Value |
|---|---|
| Performance | catch cheating, spare the honest |
| Environment | one candidate, one room, one screen |
| Actuators | flags, screenshots, an integrity score |
| Sensors | camera, screen, keystrokes, browser |

Only the Sensors row overlaps the figure, which is unavoidable in a PEAS table and is what
makes the framework legible. The closing line is unchanged and now reads as the summary of
the Sensors and Actuators rows: "Percepts in, actions out. It keeps state and adapts: one
flag makes it watch harder."

**Block B, "Three levels of lockdown"** (41 words). Red numeral, bold term, description on
the same line, closing line in 12 px italic.

## Edit 5: Caption

Replaced with: "Computer vision and behavioural models score the session. Nothing here proves
cheating. It produces suspicion, and a human decides."

It now sits under the figure at 607 px wide and is set at 15 px rather than 16 px, so it
holds at two lines instead of pushing the section down a third line.

## Edit 6: The "What happens when you are flagged" pipeline

**This one could not be applied as an edit to the existing object.** The five boxes were a
cropped AI-generated JPEG (`images/Gemini_Generated_Image_4f2mvx4f2mvx4f2m.jpg`), so the
sub-text inside them was pixels, not text.

The pipeline was rebuilt as live objects in the same visual language: five bordered boxes,
red border on OUTCOME, arrows between them, the red bracket under the last three, and the
red warning line beneath. Sub-text now reads:

- SIGNAL: face lost, tab switch, paste
- ML MODEL: scores the behaviour
- FLAGGED: integrity result: High or Medium
- HUMAN REVIEW: invigilator or recruiter
- OUTCOME: cleared / investigated / disqualified

Side effect worth knowing: the text is now vector, so it stays crisp at A3 and can be edited
again later. The image file is no longer referenced by the poster.

## Edit 7: The pull quote

Left exactly as it was, as instructed. See the source-verification section below.

## Edit 8: Em dash sweep

Ten em dashes replaced. No em dashes remain anywhere in the poster.

| Where | Was | Now |
|---|---|---|
| Quote source | exam — VU Amsterdam, 2022. | exam. VU Amsterdam, 2022. |
| 03 bullet 3 | bias audits — not independent | bias audits, not independent |
| Matrix caption | cheating — and accuses | cheating, and accuses |
| Debate YES head | YES — it protects fair testing | YES: it protects fair testing |
| Debate NO head | NO — it fails at both ends | NO: it fails at both ends |
| Debate YES body | jobs — it only works if | jobs: it only works if |
| Split note | split on this — come and argue | split on this. Come and argue |
| Reference 1 | (2022) — NPR, 25 Aug 2022. | (2022). NPR, 25 Aug 2022. |
| Reference 2 | Human Rights — Pocornie | Human Rights: Pocornie |
| Reference 5 | HackerRank — Proctor Mode | HackerRank: Proctor Mode |

The en dash in the date range "(2022–23)" in reference 2 was kept: it is a range, not an em
dash.

---

## Source verification flags

**1. "image capture every 2-3 seconds" (Edit 3, webcam callout).** This interval is the
authors' own wording, not something taken from HackerRank's published documentation. Either
cite it or swap it for the safer, near-identical-length alternative:

> captured every few seconds

**2. The pull quote "Face not found. Room too dark." attributed to a VU Amsterdam case,
2022 (Edit 7).** Not verified here, and not replaced, as instructed. If the exact wording
cannot be sourced, swap the block for this paraphrase, which has no quotation marks and
occupies the same two lines at the same size:

> The software never found her face.
>
> The errors that kept a student out of her exam. VU Amsterdam, 2022.

---

## Fit

Section 01 grew by 42 px: the extra caption line, the taller callout stack, and the larger
illustration. That was paid for by rebuilding the flow diagram 21 px shorter, by trimming
14 px of unused height off the 02/03/04 column band, and by the flexible spacer above the
bottom band. The poster still ends inside its 56 px bottom margin, with about 4 px of slack,
so nothing is clipped, but there is no room left for another line of body text anywhere
without taking it from somewhere else.

The illustration cannot go much larger without moving the Phone detection callout out from
under it: the drawing is now limited by the vertical space between the top of the section and
that bottom callout, not by the width of the column.

## Files

| File | State |
|---|---|
| `poster/source/poster-v5.pen` | Edited. **Unsaved in the Pen app at time of writing: press Cmd+S.** |
| `poster/source/images/hero-figure.png` | New. Transparent, cropped illustration. |
| `poster/source/images/Gemini_Generated_Image_n15aobn15aobn15a.jpg` | Kept, no longer referenced. |
| `poster/source/images/Gemini_Generated_Image_4f2mvx4f2mvx4f2m.jpg` | Kept, no longer referenced (the flow diagram it held is now live text). |
| `poster/ecs533u-poster-a3.png` | Re-exported at 2x (2246 x 3174). |
| `poster/ecs533u-poster-a3.pdf` | Re-exported. |

---

# Round 2: middle band restructure and Section 02

## Layout

The three column band became two columns plus a full width section:

| Block | Width | Height |
|---|---|---|
| 02 Ethical issues | 556 px (55%) | 336 px, sets the band |
| divider rule | 1 px | full band |
| 03 Current responses | 454 px (45%) | 268 px |
| 04 What next? | 1011 px, below both | 88 px, three recommendations in one row |

Numbering style, headings, red accent and divider rules are unchanged. Section 03's title
went from 24 px to 30 px to match 02 and 04 now that it has a wider column, and its three
bullets were given wider spacing so the shorter column does not read as an accident. Section
04's three bullets were reflowed from a stack into a three up row.

## Section 02: six cards, 2 x 3 grid

Six cards stacked vertically do not fit. At the sizes originally mandated (12 pt body,
10 pt evidence) the six measured **794 px of cards, 850 px with the section head**, against
roughly 340 px available on the sheet. Stacked at the reduced sizes they still need 464 px.

They fit as a **2 x 3 grid inside the left column**, two cards per row at 255 px each. That
keeps all six with a heading, a body and a source tag.

| Card | Height | Body | Source tag |
|---|---|---|---|
| 1 Bias you cannot prove | 84 px | 3 lines, 19 words | Pocornie v VU Amsterdam |
| 2 Your bedroom is now an exam hall | 84 px | 3 lines, 18 words | Ogletree v Cleveland State, 2022 |
| 3 Punished for having a body that moves | 100 px | 3 lines, 17 words, heading wraps to 2 lines | CDT: stimming and screen readers get flagged |
| 4 Biometric data, collected and leaked | 84 px | 3 lines, 19 words | ProctorU breach, June 2020: 444,000 records |
| 5 Flagged, with nowhere to appeal | 84 px | 3 lines, 20 words | HackerRank reports only High or Medium |
| 6 Consent you cannot refuse | 84 px | 3 lines, 20 words | Proctorio sued Ian Linkletter over seven links |

All six fit. None overflow.

Type: heading 13.5 px bold (10 pt), body 12 px (9 pt), source tag 10 px italic grey (7.5 pt).
The body and source are **below the 12 pt / 10 pt floor** set in the original brief, which the
follow-up instruction authorised. Each card carries the red square marker already used by the
bullets elsewhere, so the six read as one set.

Bodies were compressed from the supplied copy (35, 25, 30, 28, 28, 30 words) to 17 to 20
words. No fact, name, date or figure was added. The evidence sentences were cut to short
source tags, keeping the case or source name and, where it carried the point, the number.

## Space taken to pay for it

| Change | Saved |
|---|---|
| Title 76 px to 64 px (48 pt, the brief's floor), subtitle 20 to 18, header spacing tightened: header 177 px to 145 px | 32 px |
| Top margin block and band spacers tightened | 26 px |
| Flow diagram band spacing: 167 px to 148 px | 19 px |
| Section 04: bullets 18 px to 16 px, numeral 40 to 34 | 20 px |
| Section 05: debate text 18 px to 15 px, lead 26 to 22, row height released | 46 px |
| Matrix 192 px to 160 px, caption 13 px to 12 px | 32 px |
| References 10 px to 9.5 px | 6 px |
| Hero graphic 336 px to 321 px, callout columns re-spaced | 15 px |

**The illustration itself was not reduced.** It is still 214 x 255 px. Only the empty space
in the callout columns around it was tightened.

The sheet now ends exactly on its bottom margin: the footer runs to y1531 of 1531. There is
no slack left anywhere on the poster.

---

# Round 3: Section 03 filled, Section 02 restacked

## Layout

Both columns are now single vertical stacks of six cards on the same 63 px rhythm, so
issue and response read as pairs. Section 02 came out of its 2 x 3 grid to make that
possible. Section 03 carries seven slots: six response cards plus the gap slot.

| | Height |
|---|---|
| Section 02, six cards stacked, 12 px gaps | 468 px |
| Section 03, six cards plus gap slot, 8 px gaps | 526 px, sets the band |

## Section 03 cards

| Card | Height | Fit |
|---|---|---|
| 1 The EU AI Act names it directly | 63 px | fits |
| 2 A regulator fined a university, then spent four years defending it | 79 px | fits, heading wraps to two lines as expected |
| 3 The UK regulator audited hiring AI, politely | 63 px | fits |
| Gap slot | 44 px | fits, aligned to ethics card 5 |
| 4 Institutions walked away, unevenly | 63 px | fits |
| 5 Vendors fixed it themselves, and said so themselves | 63 px | fits |
| 6 Employers gave up on remote testing | 63 px | fits |

Same treatment as the left column: red square marker, bold heading 13.5 px, body 12 px,
source line 9.5 px italic grey. Bodies compressed to 17 to 19 words the same way the ethics
cards were, evidence lines cut to source tags. No fact, name, date or figure added.

## The gap slot

Sits at y300 inside its column. Ethics card 5, "Flagged, with nowhere to appeal", sits at
y300 inside its column. They are exactly level, which is why the ethics list gap was set to
12 px and the response list gap to 8 px. The slot is outlined in the red accent with no
fill, no heading and no marker, carrying only "No regulator. No appeal. No notice." in red.
Against six filled, marked, headed cards it reads as a deliberate hole rather than an
unfinished box.

## What paid for it

The band went from 336 px to 526 px. 190 px had to come from somewhere, and Section 01 was
chosen over dropping the flow band.

| Change | Saved |
|---|---|
| Section 01: callout labels 15 to 13 px, descriptions 11 to 10 px, label columns widened to 175 and 195 px, caption 15 to 12 px, PEAS and lockdown closing lines removed, block spacing tightened. Hero row 369 px to 278 px | 91 px |
| Debate row released from its fixed height, debate text 15 to 12 px, lead 22 to 20 px | 34 px |
| Card internals tightened across both columns, gap slot 56 to 44 px | 42 px |
| Matrix 160 to 130 px, caption 12 to 11 px | 30 px |
| Flow band: heading 20 to 18 px, boxes 66 to 58 px, quote 34 to 30 px, note 14 to 13 px | 11 px |
| Section 04 bullets 16 to 13 px, numeral 34 to 28 px | 12 px |
| Header, references and band spacers | 16 px |

**The illustration is now 164 x 196 px**, down from 214 x 255 px. That is the cost of the
twelve cards, and it is roughly where the poster's figure started before it was enlarged.

Two lines were lost from Section 01 that are worth knowing about: the PEAS closing line
("Percepts in, actions out...") and the lockdown closing line ("Only level 2 can be wrong
about you"). They were the only expendable content left in that section.

The footer lands on y1531 of 1531 with 12 px in the flexible spacer above the bottom band.

---

# Round 4: grids, and a visual flow band

## Sections 02 and 03 are now 3 x 2

Each column splits into two sub-columns of three cards.

| | Sub-columns | Contents | Height |
|---|---|---|---|
| 02 Ethical issues | 255 px each | cards 1, 2, 3 / cards 4, 5, 6 | 274 px of grid |
| 03 Current responses | 190 px each | responses 1, 2, 3 / response 4, gap slot, 5, 6 | 425 px of grid |

The gap slot stays in the second position of Section 03's right sub-column, which is the same
grid position ethics card 5 holds in Section 02's right sub-column. **It is no longer exactly
level with that card**: the response cards are taller than the ethics cards because their
sub-columns are 65 px narrower, so the rows drift. The slot still reads as a deliberate hole,
outlined in red with no heading and no marker, but the direct "opposite card 5" line of sight
that the stacked version had is gone. Restoring it would mean going back to stacks.

The grid freed 33 px, which went back into the illustration: **189 x 226 px**, up from
164 x 196 px.

## The flow band is now a diagram, not a paragraph

Removed: the red line "The candidate usually never sees the footage, the reason, or a route
to appeal", the red bracket under the last three boxes, and the whole VU Amsterdam pull quote
block ("Face not found. Room too dark." plus its source line).

The five step boxes now run the full 1011 px width, each carrying a 42 px lucide icon above
its label:

| Step | Icon |
|---|---|
| SIGNAL | activity |
| ML MODEL | cpu |
| FLAGGED | flag |
| HUMAN REVIEW | user-check |
| OUTCOME | scale, in red |

Box height went from 58 px to 97 px and the sub-text dropped to one line each, so the band is
mostly picture. Net cost 11 px.

## The matrix moved

The false positive matrix and its caption moved out of the bottom band and into the space
under Section 02's grid, where the ethics argument is. It was also cropped and keyed to a
transparent background (`images/matrix.png`, 785 x 795) the same way the illustration was, so
it no longer carries 23% empty margin and sits tight against its caption.

With the matrix gone from the bottom band, Section 05's debate runs the full width, which
took its two columns from three lines to two and saved 20 px.

Footer lands on y1531 of 1531, with 17 px between Section 04 and Section 05.

---

# Round 5: centred split, sources removed

- **The divider is now centred.** Section 02 and Section 03 are both 505 px wide with the
  hairline rule at x505, the exact middle of the 1011 px content width. Section 02 keeps its
  30 px right padding and Section 03 now has 30 px left padding and none on the right, so the
  gutter is symmetric about the rule and both columns have 475 px of live width. Card
  sub-columns are 230 px on the left and 231 px on the right, near enough identical.
- **The grey source lines are gone** from all twelve cards. Each card is now heading plus
  body. The gap slot is unchanged.
- That freed 47 px. 32 px went back into the illustration, which is now **205 x 245 px**, its
  largest yet. 15 px stayed in the spacer above Section 05.

Column heights are no longer equal: Section 02 runs 463 px because it carries the matrix
below its grid, Section 03 runs 366 px. The rule spans the full band, so the shorter column
reads as ending rather than as an error.

Sources removed from the cards, for the record, in case they are wanted in the script or the
handout: Pocornie v VU Amsterdam; Ogletree v Cleveland State 2022; CDT; ProctorU breach June
2020, 444,000 records; HackerRank High or Medium; Proctorio v Ian Linkletter; Annex III 3(d);
Garante 2021; ICO November 2024, 296 recommendations; 60,000 US students; the Proctorio
commissioned audit; Gartner 72.4%.

---

# Round 6: level columns, matrix removed, even blocks

- **The 2 x 2 true/false matrix and its caption are gone**, along with the transparent
  `matrix.png` reference. `images/matrix.png` and the original `Unknown` JPEG are still in the
  repo, unused.
- **Both grids are now real tables.** Each section holds three row frames of two cards,
  read left to right then down, so cards in a row share a top edge. Previously each column
  was two independent stacks, which is why Section 03 looked ragged: nothing lined up across
  its two halves.
- **Both columns end level at 426 px.** The rows are content-sized and the leftover height
  lives in the row gaps, not below the last row, so the visible text ends level too, not just
  the boxes.

| | Rows | Gap | Body |
|---|---|---|---|
| 02 Ethical issues | 90, 124, 90 | 41 px | 14 px |
| 03 Current responses | 95, 94, 79, plus the 43 px gap slot | 25 px | 12 px |

Section 02's copy is shorter, so at a shared 12 px its column came up 150 px short of
Section 03 and the filler had to go somewhere visible. Raising its body to 14 px fills the
column with text instead of air and gives the poster's core section the larger type, which is
the right way round. The gap slot is now a full width strip across the bottom of Section 03,
centred, still outlined in red with no heading.

Space released by dropping the matrix also brought back the two Section 01 closing lines that
Round 3 had cut ("Percepts in, actions out..." and "Only level 2 can be wrong about you"), and
put type back into Section 04 (13 to 15 px) and the debate (12 to 13 px).

Footer lands on y1531 of 1531 with 24 px between Section 04 and Section 05.

---

# Round 7: one line headings

Every card heading now fits on one line at 230 px, so no card carries a two or three line
title and the rows sit evenly.

| Section | Was | Now |
|---|---|---|
| 02 | Your bedroom is now an exam hall | Your bedroom is an exam hall |
| 02 | Punished for having a body that moves | Punished for moving |
| 02 | Biometric data, collected and leaked | Biometrics that get leaked |
| 02 | Flagged, with nowhere to appeal | Flagged, with no appeal |
| 03 | The EU AI Act names it directly | The EU AI Act names it |
| 03 | A regulator fined a university, then spent four years defending it | A regulator fined a university |
| 03 | The UK regulator audited hiring AI, politely | The UK audited, politely |
| 03 | Institutions walked away, unevenly | Institutions walked away |
| 03 | Vendors fixed it themselves, and said so themselves | Vendors marked their own work |
| 03 | Employers gave up on remote testing | Employers went back in person |

"Bias you cannot prove" and "Consent you cannot refuse" already fitted and are unchanged.

**One detail was lost, not moved:** response card 2's "then spent four years defending it".
Its body covers the fine, the ban and the vendor, but not the four year defence, so that point
now exists nowhere on the poster. If it matters for the pitch, it needs to go back into the
body.

With the headings shorter, both columns shrank and now level at **380 px with the same 26 px
row gap in each**, which is the one value where both columns land level with equal gaps:
288 + 2(26) = 262 + 3(26) = 340.

The 46 px that freed up went into the spaces between sections rather than into any one block,
so the sheet breathes a little after several rounds of squeezing: 12 px under the header rule,
8 px under the section 01 tag, 10 px before the flow band, 12 px before the band, 16 px before
Section 04, and 24 px before Section 05.

Footer still lands on y1531 of 1531.

---

# Round 8: three line blocks, tighter stacks

**Every card is now exactly 69 px**: one line of heading, three lines of body, no exceptions
in either column. Eight bodies were trimmed to hold three lines at the new size; the four
that already fitted are untouched.

**Row gaps went from 26 px to 16 px** in both columns.

**The gap slot moved below the band**, spanning the full 1011 px under both columns. That is
what finally makes the two columns identical: with the slot inside Section 03 that column was
always one block taller, which forced either uneven gaps or uneven card heights. Both columns
are now 279 px with the same card height and the same gap, and the slot reads as the closing
line of the whole 02/03 comparison rather than as an orphan in one column.

Compacting the blocks freed about 100 px. None of it went into padding:

| Where it went | |
|---|---|
| Card bodies 12 px to 13 px | the blocks are tighter but the text is larger |
| Section 01 callout labels 13 to 14 px, descriptions 10 to 11 px | the smallest type on the poster was 7.5 pt, now 8 pt |
| Illustration 205 x 245 to 212 x 253 | |
| Debate body 13 to 15 px, lead 20 to 24 px, split note 13 to 15 px | Section 05 had been squeezed hardest |
| Section 04 bullets 15 to 16 px | |
| Section spacers | 12 to 24 px between bands |

Bodies trimmed this round: ethics 1, 4, 5, 6 and responses 1, 2, 3, 6. Details worth noting,
all minor: response 2 lost "for using" (now "for Respondus"), response 3 lost "from names",
ethics 4 lost "keystroke biometrics" (now "keystrokes"), ethics 6 lost "Scrutiny is
expensive".

Footer lands on y1531 of 1531.

---

# Round 9: Section 04 rebuilt as a loop, Section 05 gains chips

Sections 01 to 03, the header and the references are untouched.

## Section 04 · What next?

The three bullets are gone, replaced by a three part band. The section number and title moved
into a narrow left sidebar (118 px) instead of sitting on their own full width head row; that
alone freed 40 px of height, which is the difference between a diagram you can read and one
squashed to a stripe.

**THE ARMS RACE** (red label, 452 px column). Two bordered boxes stacked vertically, joined by
two curved red arrows that form a clockwise loop: the right arrow bows out and runs top to
bottom, the left arrow runs bottom to top, each with a filled red arrowhead.

- MORE SURVEILLANCE / proctoring, keystroke & gaze tracking (lucide "eye")
- BETTER HIDING / Interview Coder: "undetectable" (lucide "eye-off")

Italic caption under the loop: "More watching hasn't meant less cheating: it feeds the tools
built to beat it."

**THE EXITS** (red label, 397 px column). Two bordered cards, heading left and body right so
each card is 44 px rather than the 60 px a stacked card would need:

- Audit & appeal
- Fix the test, not the watching

Both use the supplied copy word for word.

## Section 05 · The debate

- A level balance scale (lucide "scale", 26 px) sits next to "So should we use it?".
- Both paragraphs replaced with the shorter copy. At 13.5 px each side is exactly two lines,
  so the two columns are level at 97 px and the divider rule matches.
- A 24 px confusion matrix chip under each column, one cell filled: YES fills the top right
  cell in black (a cheat not flagged, the miss), NO fills the bottom left cell in red (an
  honest candidate flagged, the false positive). Labels at 9.5 px as supplied.
- Closing line now reads "Our group is split. Come and argue with us." The right aligned
  "Is fair testing worth being watched?" was already in the footer and is unchanged.

## Fitting it

Section 04 went from 88 px to 122 px, Section 05 from 196 px to 187 px, so the band needed
25 px more than it had and the sheet had 11 px of slack. The balance came out of whitespace
between bands, not out of any section's content: header rule 16 to 12, section 01 tag 12 to
10, flow band 18 to 14, the 02/03 band 20 to 16, Section 04 24 to 14, and the two spaces
around the footer rule 8 to 6. Section 05's own internal spaces came down by 2 px each.

Section 05 ends up shorter than before despite gaining the chips and the icon, because the
paragraphs dropped from three lines to two.

The gap between Section 04 and Section 05 is 14 px, so the page still fits with the flexible
spacer holding a real gap rather than collapsing to zero.

## Changes to the supplied copy

- Three em dashes replaced, per the standing house rule of no em dashes: `Interview Coder —
  "undetectable"` became `Interview Coder: "undetectable"`; `less cheating — it feeds` became
  `less cheating: it feeds`; `to millions — it only works` became `to millions: it only works`.
- The `↳` in "↳ THE EXITS" is not in Space Grotesk and rendered as a missing glyph box, so it
  is drawn as a red lucide "corner-down-right" icon at 12 px instead. The label reads the same.

## Flag

The chips were specified as echoing "the big matrix from section 02", but that 2x2 matrix was
removed in Round 7 at your request. The chips are now the only confusion matrix on the poster
and carry no axis labels, so they read as a glyph explained by the line beside them rather
than as a callback. If you want them to be self explanatory, the alternative is tiny axis
ticks (flagged / not flagged across the top, cheating / honest down the side), which costs
about 12 px per column.

Footer lands on y1531 of 1531.
