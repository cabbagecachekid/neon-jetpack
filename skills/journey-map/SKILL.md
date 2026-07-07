---
name: journey-map
description: Use when the user wants to create, map, or visualize a user journey, customer journey, experience map, or milestone map — "map the journey," "build a journey map," "chart the experience from X to Y," or any request to represent a user's progression through a product over time. Also use when converting research findings, interview synthesis, or funnel data into a journey visualization, and even when the user's draft framing is screen-based ("map our onboarding screens"). Works in FigJam when a write-capable Figma connection exists (e.g. the claude.ai Figma connector), and falls back to a portable markdown matrix when it doesn't.
---

# Milestone-Based Journey Map

Build user journey maps organized around **user milestones, not screens**. You are a rigorous research partner, not a decorator: challenge weak milestone framing, distinguish evidence from assumption everywhere, and build incrementally so the user can course-correct.

## The milestone-not-screen rule (load-bearing — apply constantly)

A milestone is a moment of *meaningful progress or state change from the user's point of view* — something the user would name if asked "what happened?" A screen is just where an interaction occurred.

- Milestone: "First saw the product do something useful with my data," "Decided to trust the app with my calendar," "Realized the trial was about to charge me"
- NOT a milestone: "Landed on dashboard," "Opened settings," "Viewed pricing page"
- Sneaky middle case — **system/business events are not milestones either**: "Account created" is a system event; the user milestone is "Committed enough to sign up." Reframe these too.

**Test every proposed column:** if it names a UI surface or a system event instead of a change in the user's state, knowledge, emotion, or commitment, propose the user-framed rewrite. Screens and channels may appear only as *evidence or context inside* a milestone, never as the column itself.

## Workflow

### 1. Gather inputs (interview, one question at a time)

Collect, asking only for what's missing from the conversation:

- Product / journey name
- Persona or segment
- Journey scope (first milestone → last milestone)
- Draft milestone list, in rough order
- Evidence sources (studies, analytics, support tickets, quotes)
- Audience for the map (team readout, exec, portfolio)

As the milestone list comes in, apply the milestone test aloud: flag screens-in-disguise and system events, and propose rewrites. Cap the map at **5–8 milestones**; if the user lists more, help them merge milestones or split the journey into two maps.

### 2. Pick the canvas

Check what is actually available before promising a format. The test is **write capability, not the word "Figma"**: look for tools that can *create* FigJam objects (files, sections, stickies, connectors).

- **FigJam (via a Figma connection with creation tools)** — the full visual artifact. Available on claude.ai with the Figma connector, or any Figma MCP that exposes create/write tools.
- **Figma connections that do NOT count:** Figma's "Dev Mode MCP Server" (common in Claude Code) is read-and-inspect only — `get_design_context`, `get_metadata`, screenshots, Code Connect. It cannot create anything. If the only Figma tools present are read-only, or they exist but are unauthenticated, treat FigJam as unavailable, say so plainly, and offer the fallback rather than stalling or attempting the build.
- **Markdown matrix (always available)** — the same spec rendered as a markdown table (milestones as columns, the eight rows), written to a file the user names. This is the default when no write-capable Figma connection exists. It round-trips: a markdown map can be rebuilt in FigJam later without re-interviewing.
- **Self-contained HTML one-pager** — only if the user asks for a shareable visual and FigJam is unavailable.

State which canvas you're using and why in one sentence. Do not silently downgrade; if the user asked for FigJam and it's unreachable or read-only, tell them which situation they're in.

### 3. Confirm structure

Read `references/map-spec.md` for the full row definitions, layout, and color scheme before building. Summarize the planned structure (milestones as columns, the eight rows, emotion curve, legend) in one short paragraph and get a go-ahead.

### 4. Build incrementally

1. Name the artifact `journey-map-[product]-[persona]-YYYY-MM-DD-v1` (today's date; increment version on revision, never overwrite).
2. **FigJam:** build with native FigJam objects — sections for milestone columns, stickies for cells, connectors for the emotion curve. Do **not** render the whole map as a single Mermaid diagram; Mermaid cannot do the swimlane matrix. No emoji in node or sticky labels (they break rendering). Scaffold the empty matrix first (columns + row labels), show the user, then fill **one milestone column at a time**, checking in as you go.
3. **Markdown:** scaffold the empty table first (header row = milestones, first column = row labels), show it, then fill one milestone column at a time. Represent the emotion curve as a dedicated row using a 1–5 intensity scale plus the emotion word; note in the legend that high = positive.
4. Keep cell text short — fragments, not paragraphs. Verbatim quotes get quotation marks and a source tag like `(P4, intent study)`.

### 5. Enforce evidence discipline

Every Evidence cell gets a source tag, or a visually loud **ASSUMED** flag. Never fake certainty. If the Feeling row is speculation without evidence, say so and mark it. A journey map that hides its assumptions is a liability in a readout.

### 6. Close out

Verify the definition of done (below), tell the user the artifact name and location, and offer — don't auto-run:

- A one-paragraph narrative summary of the journey
- The top 3 opportunities, prioritized
- The list of ASSUMED cells as a research backlog

## Definition of done

- Every column passes the milestone-not-screen test
- Emotion curve present and consistent with the Feeling row
- Every Evidence cell has a source tag or an ASSUMED flag
- Legend + provenance note (date, sources, author, version) present
- Artifact named per convention; user told where it lives (FigJam file name, or file path for markdown/HTML) and confirmed they can see it

## Reference files

- `references/map-spec.md` — row definitions, layout rules, color scheme, and example milestone rewrites. Read it before scaffolding the matrix.
