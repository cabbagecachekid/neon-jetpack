# Reading & Scannability — Corpus

The reference corpus for the **reading & scannability** dimension. SKILL.md has the workflow; this file has the principles, their mechanisms, real sources, and the boundaries of each. Load it when auditing copy, structure, or whether a page supports the way people actually read online.

Governing principle: **people don't read web pages, they scan them.** Design copy and structure to reward scanning — or accept that most of it won't be read. Every principle below traces to a named source; cite the source, not the vibe.

A note on the headline statistics: the famous "79% of users scan, 16% read word-by-word" figure is from Nielsen's 1997 eyetracking work — old, and the exact percentage shouldn't be quoted as if measured yesterday. **Prefer the current source:** Moran, K. (2020), *How People Read Online: New and Old Findings*, NNG, synthesizes **13 years of studies, 500+ participants, and 750+ hours of eyetracking** and confirms people scan rather than read — but deliberately states **no single percentage.** So cite the 2020 finding as "NN/g's eyetracking across 13 years confirms people scan rather than read," and do **not** attach a fresh number to it. The number-free phrasing is the honest one.

---

## 1. Users scan; word-by-word reading is the exception

- **Claim:** Most users scan pages for relevant bits rather than reading linearly.
- **Mechanism:** Reading on screen is effortful and the web is a foraging environment — people hunt for the scent of the information they came for, not prose to savor.
- **Source (current, preferred):** Moran, K. (2020), *How People Read Online: New and Old Findings*, NNG — 13 years of studies, 500+ participants, 750+ hours of eyetracking; states no single percentage. https://www.nngroup.com/articles/how-people-read-online/ · **Origin:** Nielsen, J. (1997), *How Users Read on the Web*. https://www.nngroup.com/articles/how-users-read-on-the-web/
- **Applies:** content pages, marketing pages, documentation, any text-heavy screen.
- **Doesn't / caveat:** deliberately immersive long-form (essays, fiction) where the reader has already committed. Cite the 2020 finding without a number; do not quote the 1997 "79%" as a current measurement.

## 2. Scan patterns are layout-dependent (F, and beyond)

- **Claim:** When scanning text-heavy pages, users' eyes tend to trace an **F**: two horizontal sweeps near the top, then a vertical scan down the left edge — content low and right gets little attention. But the F is only the *default for unstructured text*; layout reshapes the path. Eyetracking also identifies the **lawn-mower pattern** (back-and-forth across comparison tables / zigzag layouts) and the **pinball pattern** (erratic bouncing on complex search-results pages with mixed features).
- **Mechanism:** Each fixation is costly, so users sample where information density is highest and let the layout's structure guide the route. Give them no structure and they fall back to the F.
- **Source:** Nielsen, J. (2006), *F-Shaped Pattern for Reading Web Content*; Pernice, K. (2017), *…Misunderstood, But Still Relevant*; Moran, K. (2020), *How People Read Online* (lawn-mower and pinball patterns), NNG. https://www.nngroup.com/articles/f-shaped-pattern-reading-web-content-discovered/ · https://www.nngroup.com/articles/how-people-read-online/
- **Applies:** unstyled text blocks (F), comparison tables (lawn-mower), search/listing pages (pinball).
- **Doesn't / caveat:** the F-pattern is a symptom of *weak* formatting, not a law to design toward. Good hierarchy, headings, and highlighted keywords deliberately break the F and steer the eye. The fix is better structure, not accepting the default scan path.

## 3. Scannable, concise, objective writing measurably improves usability

- **Claim:** Rewriting web copy to be scannable, concise, and objective (no marketing fluff) raised measured usability substantially in controlled testing.
- **Mechanism:** Lower reading effort + higher information scent = faster task success and better recall.
- **Source:** Morkes, J. & Nielsen, J. (1997), *Concise, SCANNABLE, and Objective: How to Write for the Web*, NNG. The study reported large usability gains for scannable (+47%), concise (+58%), and combined-plus-objective (+124%) versions over the control. https://www.nngroup.com/articles/how-to-write-for-the-web/
- **Applies:** essentially all web body copy.
- **Doesn't / caveat:** the percentages are from one 1997 study with a small sample — cite them as "a measured improvement in that study," not as a universal constant. The *direction* is robust; the exact numbers are not gospel.

## 4. Inverted pyramid: conclusion first

- **Claim:** Put the most important information — the conclusion — at the top, then supporting detail in descending importance.
- **Mechanism:** Because users scan and often leave before the end, front-loading the payoff means they get it even if they read only the first lines. Borrowed from journalism for the same reason.
- **Source:** Nielsen, J. (1996), *Inverted Pyramids in Cyberspace*, NNG. https://www.nngroup.com/articles/inverted-pyramids-in-cyberspace/
- **Applies:** articles, product descriptions, landing-page sections, any block where the user wants an answer.
- **Doesn't:** narrative or suspense-driven content where withholding is the point.

## 5. Highlighted keywords, meaningful subheads, bulleted lists, one idea per paragraph

- **Claim:** Four formatting moves support scanning: highlight keywords (links count), use information-carrying subheadings (not clever ones), use bulleted lists, and keep each paragraph to one idea.
- **Mechanism:** Each gives a scanning eye a foothold — a place to stop, orient, and decide whether to read on. They turn a wall of text into navigable chunks.
- **Source:** Morkes & Nielsen (1997), *How to Write for the Web*, NNG (same study as #3). https://www.nngroup.com/articles/how-to-write-for-the-web/
- **Applies:** any multi-paragraph content.
- **Doesn't / caveat:** over-highlighting destroys the effect — if everything is bold, nothing is. Same with subheads every two lines. Density matters: emphasis works because it's scarce.

## 6. Plain language beats jargon — for experts too

- **Claim:** Plain, simple language improves comprehension and speed for *all* readers, including domain experts reading in their own field.
- **Mechanism:** Lower cognitive cost to decode means more capacity for the actual task. Experts aren't insulted by clarity; they're faster with it.
- **Source:** Nielsen Norman Group, *Plain Language Is for Everyone, Even Experts* (2017); grounded in Redish, J., *Letting Go of the Words* (2nd ed., 2012). https://www.nngroup.com/articles/plain-language-experts/
- **Jargon decision framework** (Moran, K. (2023), *Dealing with Technical or Professional Jargon*, NNG — no hard stats, a current qualitative source): for any specialized term, ask **(1) does the audience know it? (2) how important is it?** Then keep it (known + important), **gloss** it as `plain-language term (technical term)` — or the reverse when most readers know it — or replace it (unfamiliar + not essential). Experts still want the precise term of art; the framework targets *unfamiliar* jargon, not all domain vocabulary. https://www.nngroup.com/articles/technical-jargon/
- **Applies:** all functional web copy, including technical and B2B.
- **Doesn't:** precise terms of art that have no plain equivalent — keep the right word, just don't pad around it. (Rule of thumb: strip AI fluff, keep industry vocabulary.)

## 7. Line length (measure)

- **Claim:** Very long or very short line lengths slow reading; a comfortable measure is roughly 50–75 characters per line.
- **Mechanism:** Long lines make the eye lose its place on the return sweep; very short lines break rhythm with too many returns. The 50–75ch band balances both.
- **Source:** Baymard Institute, *Readability: The Optimal Line Length* (summarizes typographic research; ~50–75 chars, with ~66 a common ideal). https://baymard.com/blog/line-length-readability
- **Applies:** body-text columns, especially full-width text on large screens.
- **Doesn't / caveat:** assessable from a *screenshot or rendered CSS* (you need to see actual line width), not from raw copy. If you only have the text, say you can't judge measure.

---

## How to apply this dimension

- From **copy/text only:** judge #1, #3, #4, #5, #6 (scannability, conciseness, inverted pyramid, formatting structure, plain language). State you cannot judge #2 (F-pattern is about rendered layout) or #7 (line length needs rendered width).
- From a **screenshot:** add #2 and #7.
- Quote the source in the finding's *Principle + Source* column. Flag dated stats (#1, #3) as directional.
