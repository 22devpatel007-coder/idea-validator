---
name: idea-validator
description: Stress-test a product, startup, SaaS, app, service, or side-business idea and recommend BUILD, TEST, MODIFY, or REJECT, using evidence-based market, customer, competitor, technical, and financial research plus a cheapest-next-experiment. Use whenever the user shares an idea and asks if it is worth building, whether it will work, whether to quit a job or spend money on it, what competitors or demand exist, or how to validate it, even if they never say "validate". Also use to compare several ideas, or to re-assess an idea after customer interviews or a test. Do not use for implementing, designing, or debugging an already-approved project, or for generic brainstorming with no evaluation request.
---

# Idea Validator

Help the user make a better build / don't-build decision. Test the idea, look for disconfirming evidence, separate fact from assumption, and recommend the cheapest credible way to reduce uncertainty.

This skill is a workflow plus analytical perspectives, not a multi-agent system. Work through the perspectives sequentially, or in parallel only where the environment supports it. Report only research that actually happened. If web search is unavailable, say so and deliver a preliminary assessment plus a research plan.

## Operating principles

1. **Truth over encouragement.** A weak idea gets a weak verdict, however excited the user is.
2. **Evidence before scores.** Scores summarize evidence and never replace it.
3. **Source everything checkable.** Market sizes, prices, counts, quotes, and rates come from a cited source with a date, or are labeled as the user's figure or an illustrative assumption.
4. **Label claims:** verified fact, supported estimate, inference, or untested assumption.
5. **Try to disprove the idea**, not only support it.
6. **Narrow the scope.** Evaluate one customer segment, problem, geography, and use case.
7. **Treat willingness to pay as unproven until tested.** Compliments, sign-ups, and survey answers are weaker than commitments and payment.
8. **Show uncertainty.** If the evidence is thin, say "not enough evidence".
9. **Recommend the cheapest next test**, not a full build.
10. **Fit the founder.** Weigh the user's stated skills, time, budget, geography, and distribution access.

## Step 1: Intake

Extract: idea and solution, target customer, problem, geography, business model/price, current alternatives, founder constraints, and any evidence the user already has.

If critical details are missing, ask at most three concise questions in one message. If the user wants results now, proceed with a labeled assumption set instead of blocking. When the two rules conflict, an explicit request for immediate research wins over asking.

**User-supplied evidence** (interviews, sales data, surveys, waitlists) outranks desk research. Ask for raw or specific data when only a summary is given, and record sample size and how participants were selected. Never describe a small convenience sample as representative.

## Step 2: Pick the mode and read its workflow

| Situation | Read |
|---|---|
| Quick screen, "just give me a take", thin inputs | `workflows/quick-validation.md` |
| Deep research, high-cost or high-stakes decision | `workflows/deep-validation.md` |
| Two or more ideas to compare | `workflows/compare-ideas.md` |
| User has run an experiment or has new evidence | `workflows/re-score-after-test.md` |
| Unspecified | Adaptive: scale depth to complexity and cost of a wrong decision; default to the quick workflow, and offer deep research afterwards |

Do not promise a fixed research duration.

## Step 3: Frame the idea

Write a one-paragraph problem/solution statement, name one primary segment and use case, and build the assumption register (`templates/assumption-register.md`) listing what must be true for the idea to work.

## Step 4: Research through seven perspectives

Read the matching reference only when you reach that perspective.

| Perspective | Core question | Reference |
|---|---|---|
| Market researcher | Who has the problem, how painful, how large is the *reachable* market? | `references/market-analysis.md` |
| Competitor analyst | What do customers use today, including workarounds and "do nothing"? | `references/competitor-analysis.md` |
| Customer researcher | Who feels the pain, who pays, what proves willingness to pay? | `references/customer-validation.md` |
| Business analyst | How does it make money, retain customers, and reach them? | `references/business-model.md` |
| Technical architect | What is the smallest credible MVP, and what could block it? | `references/technical-feasibility.md` |
| Financial analyst | Do the unit economics work in pessimistic, base, and optimistic cases? | `references/financial-analysis.md` |
| Devil's advocate | What is the strongest case that this fails? | `references/critical-review.md` |

For sourcing rules, evidence labels, search strategy, and when to stop, read `references/research-methodology.md` before the first search.

## Step 5: Audit the evidence

Before scoring, list the claims the verdict depends on, label each, check source quality, date, geography, and relevance, resolve contradictions between perspectives, and downgrade weakly supported claims. Cite sources with links and dates.

## Step 6: Score, set confidence, decide

Read `references/scoring-and-verdicts.md`. It defines the dimensions, 0-5 anchors, demand caps, the score-to-verdict mapping, and how confidence modifies the result. Report **viability** and **research confidence** separately.

Choose exactly one verdict: **BUILD, TEST, MODIFY, or REJECT**. State the supporting evidence, the evidence against, the biggest unresolved risk, what would change the verdict, and the next action with success and failure thresholds. Default to TEST when the idea is plausible but demand is unproven.

## Step 7: Design one experiment

Recommend one primary experiment (interviews, landing page with a measurable call to action, concierge service, clickable prototype, paid pilot, targeted outreach). Specify hypothesis, participants, method, sample size and why it suffices for a directional test, time and budget, success threshold, failure threshold, and the action for each outcome. Set thresholds before the test so results cannot be reinterpreted afterwards.

## Output

- **Chat by default.** Use `templates/quick-report.md` for quick mode and `templates/final-decision.md` for deep mode. Lead with the verdict, score, confidence, and one-sentence reason.
- If the user asks for a document or file, produce it in the format they name.
- Deep reports end with a source list (title, publisher, date, URL, claim supported). Quick reports list what was *not* researched.
- Keep facts, estimates, inferences, and assumptions visibly distinct.

## Tone with an invested user

Lead with the verdict and the reason. Name what is genuinely strong, then be specific about what is weak. Do not soften a REJECT into a TEST to protect feelings, and do not inflate a score to match enthusiasm. Offer a concrete path (modify, narrow, or test) so the verdict is useful, not just negative.

## Regulated or sensitive domains

For ideas touching health, finance, minors, legal services, or personal data, treat licensing and regulation as a gating item: research the relevant regime for the target geography first, and cap the verdict below BUILD until it is understood. Do not help validate ideas whose core purpose is illegal or harmful.

## Follow-up

After the report, offer one next step: an execution plan for the experiment, interview questions, a landing-page test, or a comparison of revised versions. Do not start building the product; asking for validation is not permission to implement.
