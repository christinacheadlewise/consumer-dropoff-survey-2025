---
layout: default
title: Hesitation Deep-Dive
---

# Not All Hesitation Is Bad

13% of customers (169 people) said something caused them to hesitate during the process. Counterintuitively, hesitators have **higher lifetime revenue** than non-hesitators (£33 vs £26, p=0.056).

But when you break hesitation into types, the picture gets more nuanced. Some types of hesitation signal a high-value customer doing due diligence. Other types signal a problem that depresses long-term value.

---

## How we defined hesitation

Q12: *"Did anything in the process of [their task] cause you to hesitate?"*

This was only shown to people who completed their task or plan to. So these are customers who **pushed through** whatever made them pause — we're measuring overcome friction, not abandonment.

---

## The breakdown

| Hesitation type | n | Median LTV | vs No hesitation (£26) | Days to adopt | Adopt rate |
|---|---|---|---|---|---|
| **Trust / legitimacy** | **27** | **£50** | **+£24 (p=0.007)** | **1 day** | **85%** |
| Other (unclassified) | 29 | £48 | +£22 (p=0.06) | 1 day | 85% |
| Fees / pricing | 46 | £33 | +£8 (p=0.32) | 4 days | 87% |
| Card issues | 19 | £31 | +£5 (p=0.23) | 0 days | 84% |
| Confusion / UX | 9 | £20 | -£6 (p=0.85) | 5 days | 89% |
| Verification / ID | 13 | £18 | -£8 (p=0.64) | 0 days | 100% |
| **Waiting / timing** | **11** | **£9** | **-£17 (p=0.04)** | **8 days** | **82%** |

---

## What each type means for the product

### Trust hesitators → Reassure them (highest value)

> *"Was unsure if safe and legitimate initially"*
> *"Hesitant because I found Wise via search and always a concern re scams"*
> *"I thought its not legitimate"*

These are cautious, high-value people doing due diligence before committing money to a new platform. Once they're satisfied, they engage heavily. They adopt at normal speed (1 day) — the hesitation happens in their head, not in their behaviour.

**Design implication:** Trust signals during onboarding (regulatory badges, security messaging, social proof from similar users) help these customers resolve their mental checklist faster. Don't remove friction; add reassurance alongside it.

---

### Fees/pricing hesitators → Show the value (high value, slow start)

> *"Fee for transfer into wise accounts"*
> *"Cost of the card"*
> *"Being new to the product, wasn't quite comfortable loading the card with big amounts"*

They take longer to adopt (4 days vs 1 day) as they compare Wise to alternatives. But once they decide Wise is competitive, they transact significantly.

**Design implication:** Upfront fee comparison or "you saved £X vs your bank" framing could compress the deliberation window. These customers are already doing the maths — help them.

---

### Waiting/timing hesitators → Fix their speed expectations (lowest value)

> *"First, because I thought that using Wise will take DAAAAYS for the money to be received"*
> *"The delay"*
> *"Longer waiting time but it's okay"*

They expected Wise to be slow, and this first impression seems to stick. They adopt slowly (8 days), use the product less, and generate the lowest revenue of any group. Even after experiencing fast transfers, they may carry a "slow" mental model.

**Design implication:** Speed expectation-setting matters at onboarding. "Your transfer will typically arrive in minutes/hours" before they initiate — not after. If they arrive expecting days and it takes hours, that's a positive surprise. If they arrive expecting instant and it takes hours, that's a disappointment. Frame accordingly.

---

### Verification hesitators → They all push through, but disengage after

> *"Having to get a long line of identifying data right (ie iban, etc)"*
> *"I was unsure and still am unsure if I can use the PayId"*

100% adoption rate — every single one made it through. But their lifetime revenue (£18) is below baseline (£26). The friction doesn't block them; it sets a tone.

**Design implication:** Verification is a necessary step you can't remove. But the experience of verification (how long it takes, how clear the status is, what happens during the wait) shapes downstream engagement. A smoother verification won't increase conversion — it could increase lifetime value.

---

### Confusion/UX hesitators → Fixable friction (small group)

> *"I found the whole process confusing & not straight forward"*
> *"Not a lot of signposting and I had to figure out myself"*
> *"It was hard to navigate the website to understand the best way to use wise"*

Only 9 people, but these are the ones whose friction is entirely within Wise's control. They take 5 days to adopt and land below-average on LTV.

**Design implication:** Classic UX improvements — better navigation, clearer signposting, progressive disclosure. Small group but zero external dependency.

---

## Summary for prioritisation

| Type | Fix it? | Why |
|---|---|---|
| Trust | **Reassure, don't remove** | These become your best customers once convinced |
| Fees | Clarify pricing earlier | Compresses deliberation, already high-value |
| Speed/timing | Set expectations upfront | Lowest-value group — perception fix, not product fix |
| Verification | Make the wait clearer | Won't change conversion, may lift downstream value |
| UX confusion | Standard UX improvements | Small impact, easy wins |
| Card delivery | Logistics optimisation | Outside onboarding flow |

[← Back to home](index.md)
