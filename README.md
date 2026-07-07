# neon-jetpack

A skill pack for Claude (Claude Code, claude.ai, and the Agent SDK) that works like a newspaper copy desk: a team of editors that takes your human-facing work from draft to shipped — and keeps AI-assisted writing **honest and yours**.

It grew out of a real problem: while refining a resume and portfolio *with* AI, edits crept in that quietly inflated claims and sanded the author's voice into generic paste. neon-jetpack assumes the healthy case — you're collaborating with Claude on your own writing — and makes sure the result still says what you meant, claims only what's true, and sounds like you.

## The skills

| Skill | Job | Say |
|-------|-----|-----|
| **using-neon-jetpack** | The dispatcher. Routes any writing/review task to the right skill and defines how they chain. | (loads automatically at task start) |
| **line-edit** | Light-touch sentence polish: grammar, clarity, wordiness. Never a rewrite; hands back a clean version plus a list of judgment calls you can overrule. | "polish this," "proofread," "tighten this email" |
| **ai-written-check** | Flags mechanical machine-authorship tells — em dashes, triple-lists, "not X but Y," engineered cadence, universal claims — each with a concrete rewrite. | "does this sound like AI?" |
| **cringe-check** | Audits tone and positioning: solo-hero framing, JD parroting, prescribing a client's reality, overclaiming. | "does this sound cocky / try-hard?" |
| **full-review** | The orchestrator for high-stakes copy (resumes, proposals, portfolios). Runs six passes, delegating to the two checks above, plus honesty/anti-inflation, register, and fact verification. Diff table, sign-off gate. | "review my copy," "full review" |
| **ux-web-design-review** | Reviews a page or site against *evidence-backed* UX research (every claim cited), separating what works for humans from what's merely in fashion. | "review my site's UX" |
| **copyright-creative-work** | US copyright basics for your own creative work — registration prep, split sheets, what to do before releasing a song or publishing. Educational, not legal advice. | "I'm about to release this — how do I protect it?" |

## How they work as a team

- `full-review` **delegates** to `ai-written-check` and `cringe-check` — one source of truth per rule, no duplication.
- For a page going live: `ux-web-design-review` first (structure), then the copy passes (words).
- Creative work headed for release finishes with `copyright-creative-work`.
- Every skill obeys the same ground rules: sign-off before changes, never silently inflate a claim, preserve voice, and say which passes did *not* run.

## Install

**As a Claude Code plugin** (all six skills at once):

```
/plugin marketplace add cabbagecachekid/custom-claude-skills
/plugin install neon-jetpack@neon-jetpack
```

**A la carte:** copy any folder under `skills/` into `~/.claude/skills/` (Claude Code) or upload it as a skill on claude.ai. Each skill stands alone; `full-review` falls back to built-in brief notes if the two checks aren't installed.

## Design principles

Built to [Anthropic's skill-authoring best practices](https://platform.claude.com/docs/en/agents-and-tools/agent-skills/best-practices):

- **Progressive disclosure** — each `SKILL.md` is a lean checklist; catalogs, worked examples, and cited sources live in `references/` and load only when needed.
- **Composition, not duplication** — the orchestrator invokes the focused checks rather than restating them.
- **Reasoning, not bare rules** — every rule says *why*, so the model generalizes instead of pattern-matching.
- **No scripts** — these are judgment tasks; guidance is prose, not code.

## License

MIT
