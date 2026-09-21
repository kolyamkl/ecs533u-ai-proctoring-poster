# Placeholder inventory / fill-in checklist

Every ID below appears as a visible, labelled box on the poster.
**Budgets are physical, not stylistic**: each "MAX n w" is the number of words that
actually fit at the poster's type sizes. Overrunning a budget clips the box.

| ID | Section | Type | Budget | What goes in it |
|---|---|---|---|---|
| `H-1` | Header | Admin field | `[NAME]` | Student name |
| `H-2` | Header | Admin field | 4 names | Group members |
| `H-3` | Header | Image slot | logo | QMUL logo (29.6 x 10 mm) |
| `H-4` | Header | Text line | 5 items | Group no. + the four names |
| `S1.1` | 1 System Overview | Text | **24 w** | What the system is, why it counts as AI |
| `S1.2` | 1 System Overview | Text | **9 w** | Where it is used: sectors, companies, scale |
| `V1` | 1 System Overview | Flow diagram | 9 items @ ~3 w | Before / During / After, 3 sensors or models per stage |
| `V2` | 1 System Overview | Inset table | 4 rows @ **5 w** | PEAS: Performance, Environment, Actuators, Sensors |
| `V3` | 2 Ethical Analysis | Stat callout | number + **12 w** | One headline figure and a one-line caption |
| `E1` | 2 Ethical Analysis | Card text | **16 w** | Bias and Accuracy |
| `E1-EV` | 2 Ethical Analysis | Evidence line | **7 w** | Source + reference number |
| `E2` | 2 Ethical Analysis | Card text | **16 w** | Privacy and Surveillance |
| `E2-EV` | 2 Ethical Analysis | Evidence line | **7 w** | Source + reference number |
| `E3` | 2 Ethical Analysis | Card text | **16 w** | Accountability and Transparency |
| `E3-EV` | 2 Ethical Analysis | Evidence line | **7 w** | Source + reference number |
| `E4` | 2 Ethical Analysis | Card text | **16 w** | Consent and Power Imbalance |
| `E4-EV` | 2 Ethical Analysis | Evidence line | **7 w** | Source + reference number |
| `V4` | 3 Responses and Gaps | Table | 8 cells @ **8 w** | Current response + Gap, one row per issue E1 to E4 |
| `S3.1` | 3 Responses and Gaps | Text | **14 w** | The single biggest gap, one line |
| `R1` | 4 Future Improvements | Rec block | **11 w** | Fixes E1 |
| `R2` | 4 Future Improvements | Rec block | **11 w** | Fixes E2 |
| `R3` | 4 Future Improvements | Rec block | **11 w** | Fixes E3 |
| `R4` | 4 Future Improvements | Rec block | **11 w** | Fixes E4 |
| `D1` | 5 Where We Disagreed | Callout | **33 w** | The contentious question + the two positions |
| `REF1` to `REF6` | 6 References | Harvard entry | **26 w** each | Two lines each, one consistent style |

**Total fillable body text: about 340 words**, plus roughly 155 words of references.

## Why the budgets are lower than the brief's maxima

The brief's per-box maxima add up to roughly 680 words. At the mandated type sizes
(title 48 pt, headings 24 to 30 pt, body 14 to 18 pt) with four visuals, seven sections
and 12 mm margins, an A3 sheet holds about 340 words of body text. The numbers above are
what measurably fits and were verified by filling every box with dummy text at its stated
budget and checking for clipping.

If the group needs more words in a given box, take the space from another box: the row
heights in `poster-layout.html` (`grid-template-rows`) are the single place to rebalance.

## Deliberate deviations from the brief

1. **Header is about 17 percent, not 10 percent.** A 48 pt title (the mandated minimum)
   wraps to two lines at A3 width and, with the four-field admin block, cannot fit in 10 percent.
2. **Dense secondary text is 11 pt, not 14 pt.** Table cells, evidence lines, the stat
   caption, `S3.1` and `D1` use 11 pt. Main prose (`S1.1`, `S1.2`, `E1` to `E4`, `R1` to `R4`)
   stays at 14 pt as required.
3. **Six references, not eight or ten.** Six entries fit as two readable lines each;
   eight would clip. The brief allows 6 to 10.
4. **Table cells are capped at 8 words, not 12.** Twelve words forces a second line and
   the table then overruns Section 3.
