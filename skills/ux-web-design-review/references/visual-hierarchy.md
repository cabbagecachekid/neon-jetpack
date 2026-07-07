# Visual Hierarchy — Corpus

The reference corpus for the **visual hierarchy** dimension: how visual properties direct attention and group meaning. SKILL.md has the workflow; this file has the principles, mechanisms, sources, and limits.

Governing principle: **the eye goes where contrast sends it.** Size, weight, color, and space are not decoration — they're the instructions a user's pre-attentive vision follows before they read a single word. Most "this page feels off" reactions are a hierarchy that points at the wrong thing.

**Input note:** almost everything here requires a *rendered* view — a screenshot, or a faithful read of rendered CSS. You cannot judge visual hierarchy from copy text alone. From raw HTML/CSS source you can infer some of it (declared font sizes, weights, colors) but not the actual rendered result. Say so.

---

## 1. Size, weight, and color establish rank

- **Claim:** Larger, heavier, higher-contrast elements read as more important and draw the eye first; the visual "loudness" of an element should match its actual importance.
- **Mechanism:** Pre-attentive processing detects contrast in size/value/color in milliseconds, before conscious reading. Hierarchy hijacks that to set a reading order.
- **Source:** Nielsen Norman Group, *Visual Hierarchy in UX: Definition* and related NNG visual-hierarchy guidance. https://www.nngroup.com/articles/visual-hierarchy-ux-definition/
- **Applies:** every screen with more than one element competing for attention.
- **Doesn't / caveat:** if everything is emphasized, nothing is — flatness is a failure mode just as much as chaos. The test is whether importance *order* is visually obvious.

## 2. Gestalt grouping: proximity, similarity, common region

- **Claim:** Elements that are close together, look alike, or share an enclosed region are perceived as belonging together — regardless of the underlying markup.
- **Mechanism:** The visual system organizes the field into groups automatically (Gestalt psychology). Layout that fights these groupings creates confusion the user can't articulate.
- **Source:** Nielsen Norman Group, *Gestalt Principles* series (e.g. *Proximity, Uniform Connectedness, and Continuation*; *Common Region*), grounded in classic Gestalt psychology (Wertheimer, Koffka, 1920s–30s). https://www.nngroup.com/articles/gestalt-proximity-uniform-connectedness/
- **Applies:** grouping labels with fields, related cards, nav clusters, spacing between sections.
- **Doesn't:** rarely "wrong" — these are perceptual laws — but they can conflict (proximity vs. a dividing line). When they conflict, the stronger cue wins; name which you're relying on.

## 3. A clear focal point / single primary action

- **Claim:** A screen should have one dominant focal point — usually the primary action or the key message — that wins the first fixation.
- **Mechanism:** Attention is finite and serial at the point of entry. Competing equal-weight elements create a "decision before the decision" and slow everything down.
- **Source:** NNG visual-hierarchy guidance (above) and the cognitive-load literature (see `cognitive-load.md`, Hick's law).
- **Applies:** landing pages, hero sections, any screen with a goal.
- **Doesn't:** dense dashboards and tools where the user's task varies — there the hierarchy serves wayfinding, not a single CTA.

## 4. Whitespace separates, groups, and aids comprehension

- **Claim:** Adequate spacing — between paragraphs, around text, between groups — improves grouping clarity and is associated with better comprehension.
- **Mechanism:** Space is the cheapest grouping signal (Gestalt proximity) and reduces visual crowding, which lowers the effort of parsing the page.
- **Source:** Nielsen Norman Group commentary on whitespace and legibility; the often-cited comprehension figure traces to Lin, D. (2004), a readability study reporting a comprehension improvement from margin/whitespace manipulation.
- **Applies:** text-heavy pages, content density decisions, "this feels cramped/cluttered" calls.
- **Doesn't / caveat:** **flag the stat honestly.** The popular "whitespace increases comprehension by ~20%" line is a secondhand citation of Lin (2004) and gets repeated loosely. Use it as "research associates generous whitespace with better comprehension," not as a precise, guaranteed 20%. Also: whitespace has a cost — too much pushes content below the fold (see #6).

## 5. Target size and spacing (Fitts's law)

- **Claim:** The time to acquire a target shrinks with larger targets and shorter distances; small or tightly-packed clickable elements are slower and more error-prone, especially on touch.
- **Mechanism:** Fitts's law (1954) — movement time is a function of distance to and size of the target. Small tap targets force precision the motor system pays for in time and errors.
- **Source:** Fitts, P. M. (1954), *The information capacity of the human motor system…*; applied in NNG touch-target guidance. Practical floor often cited: ~44×44px (Apple HIG) / ~48×48dp (Material) minimum touch target.
- **Applies:** buttons, links, nav, form controls, anything tappable — judged from a screenshot or rendered sizes.
- **Doesn't:** the platform minimums are guidelines, not laws; the *principle* (bigger/closer = faster) is the law.

## 6. Above the fold still matters (but isn't a hard cutoff)

- **Claim:** Users pay disproportionate attention to content visible without scrolling; the area above the fold gets the majority of viewing time. But people *do* scroll, so the fold is a weighting, not a wall.
- **Mechanism:** The first viewport sets expectations and decides whether the visit continues; attention decays down the page.
- **Source:** Nielsen Norman Group, *Scrolling and Attention* (reports users spend the majority of viewing time above the fold, with attention dropping sharply below). https://www.nngroup.com/articles/scrolling-and-attention/
- **Applies:** hero sections, deciding what the first viewport must communicate, judging whether a giant image has buried the actual message.
- **Doesn't / caveat:** "the fold" varies by device — assess against a stated viewport. Don't over-rotate into cramming everything up top; clear hierarchy that invites scrolling beats a stuffed hero.

---

## How to apply this dimension

- **Requires a screenshot** (or a faithful rendered view) for #1, #2, #3, #4, #6. From source CSS you can infer declared sizes/weights/colors for #1 and #5 but not the rendered composition.
- If given only copy/text: **say you cannot assess visual hierarchy** and ask for a screenshot. Do not infer hierarchy from prose.
- When a hierarchy choice is a known trend (oversized hero image, ultra-minimal flat UI with no affordance cues), cross-check `trends-vs-evidence.md`.
