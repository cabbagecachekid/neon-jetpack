# Map Spec — Rows, Layout, Colors, Rewrite Examples

## Matrix structure

Columns = milestones, chronological left to right. Rows = layers of the experience, top to bottom:

| # | Row | Content |
|---|-----|---------|
| 1 | **MILESTONE** | Milestone name from the user's POV, past tense or decision language ("Realized…", "Decided…", "First…") |
| 2 | **What triggered it** | The event, prompt, or accumulation that caused this milestone |
| 3 | **Doing** | The user's actions around this milestone — screens/channels may appear here as context |
| 4 | **Thinking** | Internal monologue, in the user's own words where evidence exists |
| 5 | **Feeling** | One emotion word + intensity; feeds the emotion curve |
| 6 | **Evidence** | Verbatim quotes, data points, source tags — or a loud ASSUMED flag |
| 7 | **Risks / drop-off** | What could prevent the user from reaching the *next* milestone |
| 8 | **Opportunities** | Design/research/product moves, phrased as "How might we…" |

Above the matrix: an **emotion curve** — in FigJam, a connector line traversing the columns, height mapped to the Feeling row (high = positive). In markdown, a dedicated row scoring each milestone `1–5` with the emotion word (`3 · anxious`), legend noting high = positive.

Below the matrix: **legend** + **provenance note** (date, sources, author, version).

## Layout rules

### FigJam
- One section per milestone column, equal widths, generous gutters
- Row labels as a fixed left-hand column of text stickies so the matrix reads zoomed out
- Native objects only: sections, stickies, connectors. A single Mermaid diagram cannot express the swimlane matrix — reserve Mermaid for explicit quick-sketch requests.
- No emoji in node/sticky labels (breaks rendering)

### Markdown
- One table: header row = milestone names, first column = row labels
- Keep cells to fragments; break long evidence into multiple short lines with `<br>` only when unavoidable
- Put the legend and provenance note directly under the table in the same file

### Both
- Cell text is fragments, not paragraphs
- Verbatim quotes: quotation marks + source tag, e.g. `"I didn't even know it charged me" (P4, intent study)`
- Artifact naming: `journey-map-[product]-[persona]-YYYY-MM-DD-vX`; increment version, never overwrite
- Scaffold empty matrix → user check-in → fill one column at a time

## Color scheme — code by row, not by milestone (FigJam)

| Row(s) | Color family |
|--------|--------------|
| Milestone, Trigger | Neutral dark / gray |
| Doing, Thinking | Neutral light |
| Feeling | Warm (yellow/orange) |
| Evidence | Distinct cool (blue/teal) |
| Risks / drop-off | Red family |
| Opportunities | Green family |
| ASSUMED tag | Visually loud accent (e.g. signal red or acid yellow sticky tag) — must be unmissable |

In markdown, mark ASSUMED cells as `**ASSUMED**` in bold caps so they stay loud without color.

## Milestone rewrite examples

Use these to model the reframing conversation:

| User's draft | Problem | Reframed milestone |
|---|---|---|
| "Landed on dashboard" | Screen | "First saw the product do something useful with my data" |
| "Account created" | System event | "Committed enough to sign up" |
| "Viewed pricing page" | Screen | "Started weighing whether this is worth paying for" |
| "Connected calendar" | Action, not state change | "Decided to trust the app with my calendar" |
| "Trial ended" | Business event | "Realized the trial was about to charge me" (or "Discovered I'd been charged") |
| "Opened the app week 2" | Behavior log | "Came back on my own for the first time" |
