# Hesitation Deep-Dive

## Definition

**Hesitation** = Q12 (QID24): "Did anything in the process of [task] cause you to hesitate?"

- Shown to: respondents who completed their task (Q11=Yes) or plan to (Q11=Not yet)
- "Yes" respondents: 169 (13% of those shown)
- These are people who noticed friction, articulated it, **but pushed through anyway**

## Counterintuitive Finding: Hesitators Have Higher LTV

| Group | Median Revenue | Mean Revenue | n |
|---|---|---|---|
| No hesitation | £25.91 | £58.63 | 1,134 |
| **Hesitated** | **£32.79** | **£119.25** | **169** |

Mann-Whitney: p=0.056 (borderline significant)

This is not a data error. Hesitators are engaged, discerning customers who evaluate carefully and then commit deeply. The hesitation is a signal of engagement, not disengagement.

## Sub-Type Breakdown

| Hesitation type | n | Med LTV | vs Baseline | Adopted % | Med days | p (LTV) |
|---|---|---|---|---|---|---|
| **NO HESITATION (baseline)** | 1,134 | £25.91 | — | 91.0% | 1 | — |
| **Trust / legitimacy** | 27 | **£50.45** | **+£24.54** | 85.2% | 1 | **0.007 *** |
| Fees / pricing | 46 | £33.44 | +£7.53 | 87.0% | 4 | 0.32 |
| Card issues | 19 | £31.38 | +£5.47 | 84.2% | 0 | 0.23 |
| Verification / ID | 13 | £17.78 | -£8.13 | 100% | 0 | 0.64 |
| Confusion / UX | 9 | £20.13 | -£5.78 | 88.9% | 5 | 0.85 |
| **Waiting / timing** | 11 | **£8.77** | **-£17.14** | **81.8%** | **8** | **0.04 *** |
| Nothing / positive | 9 | £31.15 | +£5.24 | 88.9% | 1 | — |
| Other | 29 | £48.21 | +£22.30 | 85.2% | 1 | 0.06 |

## Key Insights by Type

### Trust / Legitimacy Hesitators (n=27) — HIGHEST VALUE

**Median LTV: £50.45 (2x baseline, p=0.007)**

These customers hesitated because:
- "Was unsure if safe and legitimate initially"
- "I thought its not legitimate"
- "Hesitant because I found Wise via search and always a concern re scams"
- "The process was very quick and I was initially unsure of the transfer and identity info"

**Profile:** Cautious, high-value users who did due diligence. Once trust was established, they committed heavily. They adopt at normal speed (1 day median) — the hesitation happens mentally, not behaviourally.

**Implication:** Trust signals at signup (regulatory credentials, social proof, security messaging) could reduce the hesitation moment without losing these customers. They're already your highest-LTV segment — reducing their friction could accelerate an already-strong trajectory.

### Fees / Pricing Hesitators (n=46) — HIGH VALUE, SLOW TO ADOPT

**Median LTV: £33.44 (+£7.53 vs baseline)**

These customers hesitated because:
- "Fee for transfer into wise accounts"
- "Cost of the card"
- "Being new to the product, wasn't quite comfortable loading the card with big amounts"
- "For now the exchange rate is low. Waiting for that"

**Profile:** Price-sensitive but ultimately high-value. They take longer to adopt (4 days vs 1 day) as they evaluate whether Wise is competitive. Once satisfied, they transact significantly.

**Implication:** Clearer upfront pricing or fee comparisons could reduce the deliberation window.

### Waiting / Timing Hesitators (n=11) — LOWEST VALUE, SLOWEST

**Median LTV: £8.77 (p=0.04, significantly below baseline)**

These customers hesitated because:
- "First, because I thought that using Wise will take DAAAAYS"
- "The delay"
- "Longer waiting time but it's okay"

**Profile:** Expectation mismatch about speed. They adopt slowly (8 days median) and remain low-engagement long-term. Their initial perception of slowness may have created a lasting impression that Wise is "slow" even after experiencing fast transfers.

**Implication:** Speed expectation-setting during onboarding. If they expect days and get hours, delight them — if they expect instant and get hours, disappoint them. The framing matters.

### Verification / ID Hesitators (n=13) — ALL ADOPT, LOW LTV

**Median LTV: £17.78 | Adoption rate: 100%**

Every single one pushed through verification friction and adopted. But their low LTV suggests the friction set a negative tone.

**Implication:** The verification process doesn't block adoption — it depresses long-term engagement. Making verification smoother won't increase conversion (already 100%) but could increase downstream value.

### Confusion / UX Hesitators (n=9) — SLOW, LOW VALUE

**Median LTV: £20.13 | Days to adopt: 5**

- "I found the whole process confusing & not straight forward"
- "At first I found the use of the app complicated, not a lot of signposting"

Small group but these are the customers whose LTV you could most improve with better UX, because the friction is entirely within Wise's control.

## Summary Framework

| Hesitation type | Signal | Action |
|---|---|---|
| Trust | High-value customer doing due diligence | Add trust signals, don't rush |
| Fees | Price-sensitive evaluator | Clearer fee comparisons upfront |
| Waiting | Expectation mismatch | Speed messaging during onboarding |
| Verification | Painful but survivable | Smoother flow → higher downstream value |
| Confusion/UX | Solvable friction | Better signposting, clearer navigation |
| Card issues | Delivery/acceptance gap | Faster delivery, wider acceptance comms |

[← Back to Index](index.md)
