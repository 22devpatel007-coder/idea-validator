# Scoring and Verdicts

## Contents
1. Dimensions and weights
2. Rating anchors
3. Demand caps
4. Score-to-verdict mapping
5. Overrides
6. Confidence
7. Worked example

## 1. Dimensions and weights

Rate each dimension 0-5. Weighted points = rating / 5 x weight.

| # | Dimension | Weight |
|---|---|---:|
| 1 | Problem severity and frequency | 20 |
| 2 | Demand / willingness-to-pay evidence | 20 |
| 3 | Reachable market and timing | 10 |
| 4 | Differentiation versus alternatives | 10 |
| 5 | Business model and unit economics | 15 |
| 6 | Customer acquisition feasibility | 10 |
| 7 | Technical and operational feasibility | 10 |
| 8 | Founder fit (skills, time, budget, distribution access) | 5 |
| | **Total** | **100** |

## 2. Rating anchors

Ratings of 4 or 5 require cited evidence. An untested assumption cannot score above 3.

| Dim | 1 (weak) | 3 (moderate) | 5 (strong) |
|---|---|---|---|
| Problem | Rare or mild; customers shrug | Real but intermittent; workarounds tolerated | Frequent and costly; customers already spend time or money on it |
| Demand | No behavioral evidence (untested) | Follow-up meetings, prototype use, signed intent | Repeat payment, or several paying customers |
| Market | Tiny or unreachable segment; poor timing | Reachable segment large enough for a small business | Large reachable segment with a clear tailwind |
| Differentiation | Feature parity with strong incumbents | Meaningful edge for one segment, easy to copy | Valued edge that is hard to copy or neutralize |
| Business model | No clear payer, or margins thin | Plausible pricing; break-even reachable but sensitive | Clear payer, healthy margin, retention drivers evident |
| Acquisition | No known channel to the buyer | One credible channel, untested cost | Proven low-cost channel the founder controls |
| Technical/ops | Hard unknowns or heavy support burden | Moderate complexity, known dependencies | Straightforward MVP, low ongoing burden |
| Founder fit | Missing key skills, time, or budget | Gaps coverable with effort | Skills, time, and access match the task |

Use 0 when evidence contradicts the dimension, and 2 or 4 for in-between cases.

## 3. Demand caps

Demand evidence ladder: 0 = evidence contradicts demand; 1 = none yet; 2 = stated interest only; 3 = commitments or meaningful behavior; 4 = early payment; 5 = repeat payment.

| Demand rating | Maximum total score | BUILD allowed? |
|---|---:|---|
| 0 | 64 | No |
| 1-2 | 79 | No |
| 3-5 | 100 | Yes, if no other override applies |

Apply the cap after summing, and show both the raw and the capped total when they differ.

## 4. Score-to-verdict mapping

Start from the capped total, then apply overrides and confidence.

| Capped total | Default verdict |
|---|---|
| 80-100 | BUILD (narrow MVP), only if demand >= 3 and confidence >= Medium; otherwise TEST |
| 65-79 | TEST |
| 45-64 | MODIFY: change the segment, problem, offer, channel, or model. Use TEST instead if the only major weakness is untested demand |
| 0-44 | REJECT in its current form |

## 5. Overrides

These cap the verdict regardless of score:
- Serious legal, safety, or platform blocker: no BUILD; MODIFY or REJECT.
- Critical technical blocker or no credible way to reach the buyer: no BUILD.
- No plausible way to capture value: no BUILD; usually REJECT or MODIFY.
- Regulated domain not yet researched: no BUILD.

## 6. Confidence

Report Low / Medium / High, with reasons: source quality, recency, directness of customer evidence, competitor and substitute coverage, completeness of financial inputs, unresolved contradictions. Do not convert to a percentage.

- **Low:** BUILD is not allowed, and the score is shown as a range reflecting the plausible swing of the least-evidenced dimensions (e.g. 55-70).
- **Medium / High:** a single score is fine.

A score is a structured judgment, not a probability of success.

## 7. Worked example (illustrative)

Ratings: problem 4, demand 1, market 3, differentiation 2, business model 3, acquisition 3, technical 4, founder fit 4.
Points: 16 + 4 + 6 + 4 + 9 + 6 + 8 + 4 = 57. Demand is 1, so the cap is 79 and does not bind. Total 57 falls in 45-64, but the main weakness is untested demand, so the verdict is **TEST**, with the experiment aimed at moving demand from 1 to 3.
