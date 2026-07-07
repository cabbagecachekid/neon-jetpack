---
name: using-neon-jetpack
description: Use when any writing, review, or shipping task begins — reviewing, polishing, or shipping human-facing writing or web pages, or protecting creative work. Routes to the right neon-jetpack skill (line-edit, ai-written-check, cringe-check, full-review, ux-web-design-review, copyright-creative-work) and defines how they chain, so the right depth of review runs in the right order.
---

# Using neon-jetpack

neon-jetpack is a team of six skills that take a piece of human-facing work from draft to shipped: polish the sentences, strip machine tells, fix the tone, verify the claims, check the page it lives on, and protect it if it's creative work. This skill is the dispatcher — read it, pick the right skill(s), and run them in order.

## The routing table

| The user's situation | Skill | Depth |
|---|---|---|
| "Polish this," "proofread," "tighten this email" — a draft they wrote, sentence-level only | `line-edit` | Light |
| "Does this sound like AI?" — mechanical tells in prose | `ai-written-check` | Focused |
| "Does this sound cocky / try-hard / like sucking up?" — tone and positioning | `cringe-check` | Focused |
| "Review my copy" for anything high-stakes: resume, cover letter, portfolio, case study, proposal, bio | `full-review` | Deep — orchestrates the two checks above plus honesty, register, and fact passes |
| "Review my site / page / landing page UX" — layout, readability, hierarchy, trust | `ux-web-design-review` | Focused |
| Releasing a song, publishing writing or photos, registering copyright, splits with collaborators | `copyright-creative-work` | Focused |

## How the team chains

- **Escalate, don't duplicate.** `line-edit` is grammar and clarity only; if tone or honesty problems surface mid-edit, finish the line edit, then recommend the matching check — don't improvise a tone review inside a line edit.
- **`full-review` is the orchestrator.** It *invokes* `ai-written-check` and `cringe-check` as passes 1 and 4. Never run those two separately and then also run `full-review` — that duplicates work. Either run a focused check alone, or run `full-review` and let it delegate.
- **Copy going onto a web page gets two lenses.** `ux-web-design-review` judges whether the page is scannable and usable; `full-review` (or the focused checks) judges whether the words are honest and human-sounding. For a page about to go live, run UX first (structure), then copy review (words) — structural changes invalidate copy edits, not the other way around.
- **Creative work ships with rights handled.** If the deliverable is a song, photo set, or piece of writing headed for release, `copyright-creative-work` runs before publication, after all copy passes are done.

## Ground rules (apply to every skill in the pack)

1. **Sign-off before changes.** Present findings; don't rewrite the author's work without explicit approval. `line-edit` is the one exception (it hands back a clean version plus a judgment-call list to overrule).
2. **Never silently inflate a claim.** If an edit would make a claim bigger than the stated truth, stop and ask.
3. **Preserve voice.** A rough, specific sentence beats a smooth, generic one. These skills subtract noise; they don't add polish-paste.
4. **Say what you didn't do.** Every review ends by naming which passes ran and which didn't, so "reviewed" never overstates coverage.
