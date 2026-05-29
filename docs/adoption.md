---
layout: default
title: Onboarding Flow Data
---

# What Does the Onboarding Flow Data Show?

We matched 1,329 of 1,331 survey respondents to `RPT_PRODUCT.CONSUMER_ONBOARDING_FLOW` in Snowflake. This gives us behavioural ground truth alongside self-reported survey answers.

---

## Overall picture

| Milestone | % of survey respondents |
|---|---|
| Shown intent | 98% |
| Verified KYC | 96% |
| **Adopted any job** | **90%** |
| Cross-currency job | 61% |
| MCA adopted | 85% |
| Send adopted | 36% |

Most survey respondents are well past the onboarding funnel. 90% have adopted at least one product.

---

## How fast do they adopt?

| Time to first job | n | % |
|---|---|---|
| Same day | 110 | 8% |
| 1–7 days | 228 | 17% |
| 8–14 days | 129 | 10% |
| 15–30 days | 131 | 10% |
| 31–60 days | 79 | 6% |
| 61+ days | 26 | 2% |

**Median: 1 day.** Most customers who adopt do so quickly.

---

## What makes people adopt faster?

| Factor | Faster (days) | Slower (days) | Significant? |
|---|---|---|---|
| **Aware of card** (send/receive users) | 0 days | 1 day | p=0.0002 |
| Hesitated | 3 days | 1 day | p=0.03 |
| Had signup difficulty | 2 days | 1 day | p=0.06 |
| Needed help | 1 day | 1 day | Not significant |
| Expat status | 1 day | 1 day | Not significant |

Card awareness is the strongest behavioural lever for adoption speed.

---

## The validation finding: Survey ≠ Reality

This is the most important table in this analysis:

| What they said in the survey | Actually adopted (per Snowflake) | Truly not adopted |
|---|---|---|
| "Yes, I completed my task" (n=1,184) | 91% | 9% |
| **"Not yet, but I plan to" (n=119)** | **81% have adopted** | **19% truly pending** |
| **"No" (n=26)** | **77% have adopted** | **23% truly not** |

### Why the discrepancy?

We checked the timestamps: **106 of 109 "not yet" respondents adopted *before* answering the survey** (median 61 days before). All 24 "No" respondents who adopted also did so before. This is not a timing artefact — they were not adopting after the survey.

The survey asked: *"Did you manage to [get a card / send money / receive money / etc.] using Wise?"*

The onboarding flow tracks: *"Has this customer completed any job adoption?"*

These measure different things:
1. A customer who came to send money but activated via MCA/card → says "No" to Q11, but has adopted in Snowflake
2. A customer who uses the balance/MCA but doesn't consider that "completing" what they came for
3. Only 3 respondents adopted *after* the survey — this is almost entirely a product-mismatch story, not a timing story

### What this means

**The "drop-off problem" is largely an intent-product mismatch problem, not an adoption failure.** These customers had already used Wise before they even took the survey — they just hadn't used it for the specific thing they originally came for. The ~106 who say "not yet" despite having already adopted are telling us their original need is still unmet.

**What this means on a product level:**

The onboarding flow is effective at getting people to activate *something* — 90% adopt, 92% via MCA. But the flow funnels nearly everyone through the same MCA activation path regardless of what they came for. A customer who arrived to send money to a family member, or to get a card for a trip, ends up activating a multi-currency account — and from their perspective, they haven't done what they came to do.

This creates a gap between internal success metrics (adoption = ✓) and customer-perceived success (original job = incomplete). The framing should shift from "how do we stop people leaving" to "how do we route people to their stated job faster." The opportunity is in intent-matched onboarding paths — not a single funnel that happens to activate MCA along the way.

---

## Friction → Adoption (by task type)

| Task | Adoption rate | Cross-currency | Days to adopt |
|---|---|---|---|
| Card | 89% | 62% | 2 days |
| Send | 92% | 69% | 1 day |
| Receive | 90% | 57% | 0 days |
| Invest | 93% | 30% | 0 days |
| Other | 91% | 53% | 1 day |

Invest users adopt quickly (93%!) but rarely go cross-currency (30%). They may be doing same-currency balance holds rather than true investment products.

---

## Activation type

| Type | % |
|---|---|
| MCA (multi-currency account) | 93% |
| Send money | 6% |
| Not activated | 1% |

Almost everyone activates via MCA — even those who came for send or receive.

[← Back to home](index.md)
