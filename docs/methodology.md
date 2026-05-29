---
layout: default
title: Methodology & Limitations
---

# Methodology & Limitations

## Study design

| | |
|---|---|
| What | Self-administered online survey (Qualtrics) |
| Who | New Wise consumer customers who registered ~30 days prior to survey |
| Where | US, UK, Philippines (English only) |
| When | Data collected 22 October – 25 November 2025 |
| How recruited | Email via CRM |
| Incentive | Prize draw: 5 chances to win £100 GBP equivalent |
| Sample | 1,331 after cleaning (from 1,513 raw) |
| Target | 385 minimum — achieved 3.5x target |

## What we enriched with

Survey responses were matched to Snowflake via `user_id`:

| Source | What it gives us |
|---|---|
| `RPT_CORE_ANALYTICS.PROFILE_MONEY_MOVEMENT` | Lifetime volume, revenue by product (send/spend/receive) |
| `RPT_PRODUCT.CONSUMER_ONBOARDING_FLOW` | Job adoption dates, KYC milestones, activation type, first product |

Match rate: 99.8% (1,329 of 1,331)

## Statistical tests

| Test | When we used it |
|---|---|
| Spearman correlation | Ordinal survey answers vs continuous revenue |
| Point-biserial correlation | Yes/no indicators vs continuous revenue |
| Mann-Whitney U | Comparing two groups on revenue (non-parametric) |
| Kruskal-Wallis H | Comparing 3+ groups on revenue (non-parametric) |
| Chi-square | Categorical × categorical (e.g., task type × conversion) |
| Cramér's V | Effect size for chi-square tests |

We used non-parametric tests throughout because revenue data is heavily right-skewed. Medians rather than means are reported for the same reason.

All tests: α = 0.05. * = p<0.05, ** = p<0.01, *** = p<0.001.

---

## What this data can tell you

- Which friction points correlate with lower lifetime value
- What proportion of customers experience each type of friction
- Whether specific segments drop off at different rates
- What customers say in their own words about what went wrong
- How self-reported experience maps to actual behavioural data

## What this data cannot tell you

- **Causation.** We can't tell whether friction *causes* lower LTV or whether lower-intent customers *perceive* more friction. The relationships are correlational.
- **Who we didn't reach.** Only ~1% of invited customers responded. True non-converters (completely disengaged) are systematically underrepresented.
- **Regional differences.** We can't split by country because the survey didn't ask which country respondents are in (and we didn't include country from Snowflake in the enrichment).
- **Why people abandoned registration.** This survey only reached people who *successfully registered*. Pre-registration drop-off is invisible here.

---

## Known limitations

### 1. Self-selection bias
The biggest caveat. People who respond to a survey about Wise are more engaged with Wise than those who don't. Our sample has 89% task completion — much higher than the ~31% conversion rate in the population. The "drop-off" perspective is underrepresented.

### 2. Drop-off sub-sample is underpowered
- Target for segmented analysis: 100+ per segment × 6 segments = 600
- Achieved: 147 drop-offs total
- Margin of error for drop-off findings: ~8% (vs 5% target)
- **Do not segment within the drop-off group** — use comparisons between drop-off (n=147) and converted (n=1,184) instead

### 3. Q10 interpretation ambiguity
The "regular transaction" answer may be retrospective ("I already use Wise regularly") rather than prospective ("I plan to use it regularly"). This affects how we interpret the frequency-LTV relationship. See [Statistical relationships](correlations.md#the-regularly-question--what-the-data-actually-shows).

### 4. Q11 doesn't match behavioural data
81% of "not yet" respondents have actually adopted. The question measured intent-specific completion, not general adoption. Findings about "drop-offs" based on Q11 should be interpreted with this caveat.

### 5. Q15 question confusion
Several respondents who said "No" to Q11 (didn't complete task) then answered Q15 (reasons not to use Wise) with "I am using it" or "don't understand question." The Q11→Q15 path may have confused some respondents about what they were being asked.

### 6. No attention checks
The survey didn't include attention check questions. We mitigated this with the converging evidence quality pipeline, but some low-effort responses may have passed through.

### 7. English-only
The research plan included US, UK, and Philippines. All three markets have English speakers, but non-English-speaking customers in these markets are excluded. India (a planned Phase 2 market) was not included.

---

## How to use this data responsibly

1. **Use the comparison** (converted vs drop-off, n=1,184 vs n=147) — it has adequate power
2. **Don't sub-segment the drop-offs** (n=147 split 6 ways = ~25 per cell)
3. **Treat hesitation sub-types as directional** (n=9 to n=46 per type)
4. **Cross-reference with behavioural data** before acting on survey-only findings — as the Q11 validation shows, self-report and behaviour can diverge
5. **Use the open-ends for hypothesis generation**, not for sizing — "27% mentioned verification" tells you it's a theme, not that it affects 27% of all customers

[← Back to home](index.md)
