---
layout: default
title: Statistical Relationships
---

# Statistical Relationships

What predicts higher lifetime revenue? What predicts drop-off? How do friction points relate to each other?

---

## What predicts higher lifetime revenue?

### Strongest predictors (binary indicators)

| Indicator | Correlation | p-value | Median with | Median without |
|---|---|---|---|---|
| Aware of Wise card | +0.13 | <0.0001 | £30 | £25 |
| Experienced hesitation | +0.11 | 0.0001 | £33 | £26 |
| Is expat (2+ countries) | +0.09 | 0.002 | £30 | £23 |
| Regular transaction intent | +0.09 | 0.002 | £34 | £24 |
| Completed task | +0.06 | 0.03 | £28 | £12 |
| Had signup difficulty | -0.05 | 0.05 | £19 | £28 |

### Continuous measures

| Variable | Correlation | p-value | Direction |
|---|---|---|---|
| Completed task (Q11) | -0.18 | <0.0001 | Completing → higher revenue |
| Countries lived in | +0.12 | <0.0001 | More countries → higher revenue |
| Signup ease | +0.10 | 0.0002 | Easier signup → higher revenue |
| Age | +0.08 | 0.006 | Older → slightly higher revenue |

### Not predictive of revenue

- Prior provider experience (p=0.41)
- Needing external help (p=0.90)
- Frequency intent as a raw ordinal variable (p=0.28)

---

## What predicts drop-off?

| Predictor | Effect size (Cramér's V) | p-value |
|---|---|---|
| **Task type** | **0.19** | **<0.0001** |
| Signup ease | 0.10 | 0.014 |
| Countries lived in | 0.07 | 0.23 |
| Age | 0.06 | 0.55 |
| Prior provider | 0.02 | 0.50 |

Only task type has a meaningful effect. A Cramér's V of 0.19 is a small-to-medium effect — driven almost entirely by Invest users (47% drop-off vs ~10% for everything else).

---

## How do friction points cluster?

| Variable 1 | Variable 2 | Correlation | Meaning |
|---|---|---|---|
| Signup ease | Hesitation | -0.14 | Harder signup → more hesitation |
| Task completion | Help needed | -0.12 | Not completing → needed more help |
| Signup ease | Task completion | -0.09 | Harder signup → less likely to complete stated task |
| Age | Hesitation | +0.09 | Older → more likely to hesitate |
| Age | Help needed | -0.08 | Older → less likely to need help |

The friction cluster story: harder signup leads to hesitation, which leads to slower adoption — but not necessarily to lower value. Hesitation and difficulty are correlated but have **opposite** relationships with revenue.

---

## The "regularly" question — what the data actually shows

The team flagged concern about how respondents interpreted Q10 ("Was that a one-time thing, or do you need it regularly?").

### The signal

| Answer | Median revenue | Days to first job |
|---|---|---|
| One time | £19 | 0 days |
| Regular | £34 | 0 days |
| Not sure | £13 | 1 day |

### The concern

- "Regular" respondents already adopted at day 0 — they may be describing what they *already do*, not what they *intend* to do
- The survey was sent ~30 days after registration; many had already transacted multiple times
- The strong LTV signal (r=0.085, p=0.002) may be tautological: "I use Wise regularly" → of course they have higher LTV

### Recommendation

Treat Q10 as a **descriptive segment** (who are the regular users?), not a **predictive signal** (regularity causes higher LTV). If the team wants to use frequency intent as an onboarding signal, the question would need to be asked *before* first transaction, not 30 days after registration.

---

## Effect sizes in context

All survey-to-LTV correlations are in the **rho = 0.05–0.18 range**. These are real, statistically significant relationships in a large sample, but they explain only 1-3% of variance in revenue individually. Customer value is driven primarily by factors outside this survey (corridor, business vs personal needs, economic circumstances).

The survey's value is in identifying **addressable friction** and **prioritising which friction to fix** — not in predicting individual customer value.

[← Back to home](index.md)
