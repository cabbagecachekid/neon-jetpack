# Trends vs Evidence — The Arbiter

The reference for separating **what users actually do** from **what's currently in style**. This is the file that makes the skill more than a vibes-checker. Consult it whenever a finding involves a stylistic or fashionable choice.

Governing principle: **popularity is not evidence.** A pattern being everywhere right now tells you about design culture, not about user behavior. Some trends are evidence-aligned, some are neutral, and some actively fight the research. Tag each accordingly — and when a trend conflicts with evidence, name the conflict and cite the evidence it violates.

How to tag:
- **[Evidence]** — the corpus has a named source supporting it.
- **[Convention]** — common practice, weak or no behavioral evidence. Not automatically bad; just not *proven*. Say so.
- **[Convention vs Evidence conflict]** — fashionable AND contradicted by research. The highest-value finding this skill produces. Always cite the violated principle.

---

## Worked conflicts (fashionable patterns the evidence pushes back on)

### 1. Low-contrast / thin light-gray body text

- **The trend:** light gray text on white, hairline font weights, "subtle" type — read as modern and minimal since the mid-2010s.
- **The evidence against:** low contrast measurably hurts legibility and excludes low-vision and older users and anyone in bright light. WCAG 1.4.3 sets a **4.5:1** minimum for normal text (3:1 for large). NNG: *Low-Contrast Text Is Not the Answer* documents the usability harm. https://www.nngroup.com/articles/low-contrast/ · https://www.w3.org/WAI/WCAG21/Understanding/contrast-minimum.html
- **Verdict:** [Convention vs Evidence conflict]. Flag any body text below 4.5:1. Assessable from a screenshot or rendered CSS colors, not raw text.

### 2. Hamburger / hidden navigation on desktop

- **The trend:** collapsing primary nav behind a hamburger icon even on wide screens, for a clean look.
- **The evidence against:** hidden navigation is less discoverable and less used than visible navigation; hiding primary destinations adds a click and removes the information scent. NNG testing on hidden vs. visible navigation found visible (or combo) nav outperforms hidden, especially on desktop where space exists. (See NNG, *Hamburger Menus and Hidden Navigation Hurt UX Metrics*.)
- **Verdict:** [Convention vs Evidence conflict] on desktop where space allows visible nav. On small mobile screens the tradeoff is more defensible (space-constrained). Tie the verdict to viewport.

### 3. Icon-only navigation without labels ("mystery meat")

- **The trend:** unlabeled icons for nav/actions, for minimalism.
- **The evidence against:** most icons are ambiguous without a text label; users hover/guess, which is recognition-over-recall failing (see `cognitive-load.md` #3). NNG: *Icon Usability* — icons need visible text labels except for a tiny set of universally understood ones (home, search, print, close). https://www.nngroup.com/articles/icon-usability/
- **Verdict:** [Convention vs Evidence conflict] for anything beyond the universal handful. Recommend a label.

### 4. Placeholder text as the only field label

- **The trend:** using a field's gray placeholder instead of a persistent label, for a clean minimal form.
- **The evidence against:** placeholders vanish on focus/typing, taxing working memory, hurting error recovery, and failing recognition-over-recall. NNG: *Placeholders in Form Fields Are Harmful*. https://www.nngroup.com/articles/form-design-placeholders/
- **Verdict:** [Convention vs Evidence conflict]. Recommend a persistent visible label.

### 5. Auto-rotating carousels / sliders for key content

- **The trend:** hero carousels that auto-advance through messages.
- **The evidence against:** users largely ignore them (banner blindness on the slider region), often miss slides 2+, and motion/auto-advance creates control and accessibility problems. NNG: *Auto-Forwarding Carousels and Accordions Annoy Users and Reduce Visibility*. https://www.nngroup.com/articles/auto-forwarding/
- **Verdict:** [Convention vs Evidence conflict] when used for content that matters. If the message is important, don't bury it in a rotating slot.

### 6. Scroll-jacking / parallax that hijacks scrolling

- **The trend:** custom scroll behavior, scroll-triggered takeovers, heavy parallax, for "immersive" feel.
- **The evidence against:** overriding the user's expected scroll model breaks Jakob's-law familiarity (`cognitive-load.md` #6), causes disorientation, hurts performance and accessibility, and removes user control.
- **Verdict:** [Convention vs Evidence conflict] when it overrides standard scrolling. Light, non-blocking parallax that doesn't hijack control is closer to [Convention] / neutral. Judge by whether the user keeps control.

### 7. Oversized full-screen hero pushing content below the fold

- **The trend:** a giant full-viewport image/video hero with the actual message and CTA below it.
- **The evidence against:** above-the-fold attention weighting (`visual-hierarchy.md` #6, NNG *Scrolling and Attention*) means a content-free hero spends the user's most valuable attention on decoration. Users do scroll, so it's not fatal — but it's a costly default.
- **Verdict:** usually [Convention vs Evidence conflict] in degree — flag if the first viewport communicates nothing about what the site is or does.

---

## Trends that are evidence-aligned (don't reflexively flag these)

Not every trend is bad. Tag these [Convention] *supported by* [Evidence], and don't ding them:

- **Generous whitespace / breathing room** — aligns with grouping and comprehension (`visual-hierarchy.md` #4). (Caitlin's own taste leans this way; it's also defensible on evidence.)
- **Large, legible type and big tap targets** — aligns with readability and Fitts's law (`visual-hierarchy.md` #5).
- **Sticky/visible primary navigation** — supports recognition over recall and findability.
- **Skeleton screens / progress feedback** — supports the "visibility of system status" heuristic.
- **Plain-language microcopy** — directly evidence-backed (`reading-and-scannability.md` #6).

---

## The arbiter's rule of engagement

1. Identify whether the choice under review is a recognizable trend.
2. Check this file and the dimension corpora for evidence for or against.
3. Tag: [Evidence] / [Convention] / [Convention vs Evidence conflict].
4. For a conflict, **name the violated principle and cite it** — that citation is what separates this from a taste opinion.
5. When you have no corpus evidence either way, say so: "this is a stylistic choice; I have no behavioral evidence for or against — treat as taste." Don't manufacture a citation. (Citation honesty, SKILL.md guardrail #1.)
