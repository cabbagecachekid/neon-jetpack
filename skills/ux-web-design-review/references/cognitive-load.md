# Cognitive Load — Corpus

The reference corpus for the **cognitive load** dimension: how much mental effort a design demands, and how to lower the part that isn't the user's actual task. SKILL.md has the workflow; this file has the principles, mechanisms, sources, and the misapplication traps.

Governing principle: **working memory is small and attention is expensive — spend the user's mental budget on their goal, not on operating your interface.** Cognitive load that doesn't serve the task is waste.

This dimension carries the corpus's most-misapplied principle (Miller's 7±2). Honesty about that misapplication is itself a feature of the skill — see #2.

---

## 1. Hick's law: more choices, slower decisions

- **Claim:** The time to make a decision increases (logarithmically) with the number and complexity of options.
- **Mechanism:** Each additional option adds to the set the user must consider and discriminate among. More forks = more deliberation.
- **Source:** Hick, W. E. (1952) and Hyman, R. (1953) — the Hick–Hyman law. Applied to UX in NNG and general HCI guidance.
- **Applies:** navigation breadth, menu length, number of CTAs, plan/pricing tables, form option sets.
- **Doesn't / caveat:** it's about *decision* time among comparable choices, not a blanket "fewer is always better." Grouping and good labels can make many options manageable (a well-categorized menu beats a short confusing one). Don't use Hick to justify hiding things users need.

## 2. Chunking and working-memory limits — and the 7±2 trap

- **Claim:** People process information better in small, meaningful chunks than as long undifferentiated strings.
- **Mechanism:** Working memory holds only a few items at once; chunking packs more meaning into each slot.
- **Source:** Miller, G. (1956), *The Magical Number Seven, Plus or Minus Two*. Modern estimates put the limit lower — about **4 chunks** for adults (Cowan, N. (2001), *The magical number 4 in short-term memory*).
- **Applies:** grouping form fields, breaking long numbers/IDs into chunks, structuring content into digestible sections.
- **Doesn't / MISAPPLICATION FLAG:** **"7±2" is routinely misused to cap menu items or nav links. That's wrong.** Miller's number is about short-term memory span for items you must *hold in mind*, not the number of persistent, visible, scannable options on a screen — those don't tax working memory the same way (Nielsen has explicitly debunked the "7±2 navigation" myth). When you see "we limited the nav to 7 because of Miller," that's a [Convention] dressed as [Evidence] — call it out.

## 3. Recognition over recall

- **Claim:** Make options, actions, and information visible so users recognize them, rather than forcing them to remember things from elsewhere in the interface.
- **Mechanism:** Recognition is cognitively cheaper than recall — the cue does the retrieval work. Hidden state forces the user to hold context in working memory.
- **Source:** Nielsen, J., *10 Usability Heuristics for User Interface Design*, heuristic #6 ("Recognition rather than recall"). https://www.nngroup.com/articles/ten-usability-heuristics/
- **Applies:** showing entered data back, visible navigation, persistent labels, autocomplete, breadcrumbs.
- **Doesn't:** rarely — but recognition aids have a space cost; balance against clutter (#5) and hierarchy.

## 4. Progressive disclosure

- **Claim:** Show the few options most users need first; move advanced or rare options to a secondary layer revealed on demand.
- **Mechanism:** Defers the cost of complexity until it's wanted, keeping the common path simple without removing power.
- **Source:** Nielsen, J. (2006), *Progressive Disclosure*, NNG. https://www.nngroup.com/articles/progressive-disclosure/
- **Applies:** settings, advanced search, onboarding, dense forms, feature-rich tools.
- **Doesn't / caveat:** only works if the split matches real frequency-of-use. Hiding something users need *often* (see the hamburger-nav critique in `trends-vs-evidence.md`) is progressive disclosure misapplied — it just adds a click and hides the scent.

## 5. Minimize extraneous cognitive load

- **Claim:** Reduce the mental effort that isn't intrinsic to the task — visual clutter, inconsistent patterns, ambiguous labels, unnecessary steps.
- **Mechanism:** Total cognitive load = intrinsic (the task) + extraneous (the interface friction). You can't cut the intrinsic, so cut the extraneous.
- **Source:** Nielsen Norman Group, *Minimize Cognitive Load to Maximize Usability*; grounded in Cognitive Load Theory, Sweller, J. (1988). https://www.nngroup.com/articles/minimize-cognitive-load/
- **Applies:** everywhere — it's the umbrella principle for this dimension.
- **Doesn't:** "minimize" isn't "remove everything" — stripping needed information or affordances *raises* load by forcing recall and guessing.

## 6. Jakob's law: meet existing mental models

- **Claim:** Users spend most of their time on *other* sites, so they expect yours to work like the ones they already know. Familiar patterns lower the load of learning your interface.
- **Mechanism:** A matched mental model means the user reuses existing knowledge instead of building new — near-zero learning cost.
- **Source:** Nielsen, J., *Jakob's Law of the Internet User Experience* (popularized via NNG / lawsofux.com). 
- **Applies:** placement of nav, cart, search, logo-links-home, form conventions, icon meanings.
- **Doesn't / caveat:** this is the evidence-based counterweight to novelty for its own sake. Novel interaction is justified only when it clearly beats the familiar pattern on the user's task — not because it looks fresh. This principle is the bridge to `trends-vs-evidence.md`.

---

## How to apply this dimension

- Assessable from **copy/text** (label clarity, step count described), **HTML/CSS source** (nav structure, form complexity, disclosure patterns), **URL fetch** (structure, option counts), and **screenshot** (visible clutter, recognition cues). Note which signals each input gives you.
- **Watch for [Evidence]-washing:** Hick's law and Miller's number are the two most cited-to-sound-rigorous and most misapplied. When someone invokes them to justify a choice, verify the claim actually matches what the research says (#1 caveat, #2 flag) before tagging it [Evidence].
