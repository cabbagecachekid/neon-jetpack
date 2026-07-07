# Trust & Credibility — Corpus

The reference corpus for the **trust & credibility** dimension: whether a site reads as believable and safe to act on. SKILL.md has the workflow; this file has the principles, mechanisms, sources, and limits.

Governing principle: **users decide whether to trust a site in seconds, largely from surface cues — and design quality is one of those cues.** Credibility is earned by competence signals (clear contact, working links, honest claims, real evidence) and lost by sloppiness, hype, and dark patterns.

**Dating note (read before citing #1):** the canonical source here, the Stanford Web Credibility Guidelines, is from 2002. It is still the most-cited framework and its findings hold up directionally, but the *visual specifics* of 2002 are dated. Cite the *principle* (design quality affects perceived credibility), flag the *year*, and don't quote 2002 aesthetic advice as current.

---

## 1. Visual design quality shapes perceived credibility

- **Claim:** A large share of users' credibility judgments about a site come from its overall visual design and "look" — appeal, professionalism, layout — often before they evaluate the actual content.
- **Mechanism:** Surface competence is a fast, cheap proxy for underlying trustworthiness. A polished, coherent design signals "this organization is competent," which transfers to its claims.
- **Source:** Fogg, B.J. et al. (2003), *How Do Users Evaluate the Credibility of Web Sites?*, Stanford Persuasive Technology Lab — found "design look" was the most-mentioned factor (~46% of comments) in users' credibility assessments. Companion: the *Stanford Web Credibility Guidelines* (2002), 10 guidelines. https://credibility.stanford.edu/guidelines/
- **Applies:** first-impression / landing pages, any site asking for trust (signup, purchase, data).
- **Doesn't / caveat:** 2002-vintage — the *finding* (design affects credibility) is durable; the era's specific visual recommendations are not. Don't conflate "looks current/on-trend" with "credible" — see `trends-vs-evidence.md`; a trendy site can still read as untrustworthy if claims are hollow.

## 2. Show real-world competence and contact

- **Claim:** Make it easy to verify there's a real, accountable organization behind the site — physical/contact info, named people, evidence of expertise, working links.
- **Mechanism:** Verifiability raises trust; signals that the entity is real and findable reduce perceived risk. Broken links and missing contact do the opposite.
- **Source:** *Stanford Web Credibility Guidelines* (2002), guidelines on showing real-world presence, expertise, and honest, error-free operation. https://credibility.stanford.edu/guidelines/
- **Applies:** about pages, footers, contact, portfolios, anything where "is this person/org legit" matters.
- **Doesn't:** sometimes deliberately minimal personal sites — but even then, a dead link or typo costs credibility disproportionately.

## 3. Social proof, used honestly

- **Claim:** People look to others' behavior and judgments to decide what's trustworthy — testimonials, client logos, real reviews, usage numbers.
- **Mechanism:** Social proof (Cialdini) — under uncertainty, we infer correct action from what similar others do. Reduces perceived risk of being the only one trusting.
- **Source:** Cialdini, R. (1984), *Influence: The Psychology of Persuasion* — the social-proof principle; widely applied in conversion/UX literature.
- **Applies:** landing pages, pricing, signup, portfolios (real clients/work).
- **Doesn't / caveat:** **honesty guardrail** — fabricated, vague, or anonymous social proof ("trusted by thousands!") *erodes* trust when it reads as hollow. Specific and verifiable beats voluminous and generic. Flag inflated or unverifiable social proof as a credibility risk, not a win. (This aligns with the skill's anti-overclaim stance.)

## 4. Error and empty states that help, not blame

- **Claim:** Good error messages say what happened, in plain language, and how to recover; good empty states orient a new user instead of showing a void.
- **Mechanism:** Failure moments are where trust is most fragile. A blaming, cryptic, or dead-end state signals the system doesn't have the user's back; a helpful one signals competence and care.
- **Source:** Nielsen, J., *10 Usability Heuristics*, heuristic #9 ("Help users recognize, diagnose, and recover from errors") and #5 (error prevention). https://www.nngroup.com/articles/ten-usability-heuristics/
- **Applies:** forms, search-no-results, first-run empty screens, 404s, failed actions.
- **Doesn't / input caveat:** often not visible in a static screenshot of the happy path — note that you can't assess error states without seeing them, and recommend checking them.

## 5. Honest affordances and signifiers

- **Claim:** Interactive elements should look interactive, and non-interactive ones shouldn't; the visual signifier must match the actual behavior.
- **Mechanism:** Affordances and signifiers (Norman) tell users what they can do. When buttons don't look clickable, or text looks like a link but isn't, users mis-predict the system and lose confidence.
- **Source:** Norman, D. (2013), *The Design of Everyday Things* (revised ed.) — affordances and signifiers.
- **Applies:** buttons, links, cards, anything tappable; flat/minimal designs that strip click cues.
- **Doesn't / caveat:** strongly connected to the **flat-design** critique in `trends-vs-evidence.md` — removing all affordance cues for aesthetic minimalism is a fashionable choice that measurably hurts discoverability of what's clickable.

---

## How to apply this dimension

- **Screenshot / URL:** assess #1, #2, #5 (look, contact/links present, affordance clarity), and #3 if social proof is shown.
- **Copy/text:** assess the honesty/specificity of #3 (social proof claims) and the tone of #4 (error/empty copy) if provided.
- **Always flag what you couldn't see:** error states, form-failure handling, and link health usually aren't visible in one screenshot — name them as unassessed.
- Cite Stanford as **(2002)** every time, with the "directional, dated specifics" caveat.
