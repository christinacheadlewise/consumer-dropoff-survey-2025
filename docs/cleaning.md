---
layout: default
title: Data Cleaning
---

# How We Cleaned the Data

## What we removed

| Step | Removed | Running total |
|---|---|---|
| Started with | — | 1,513 responses |
| Removed abandoned (didn't finish) | 136 | 1,377 |
| Removed poor quality (very fast + low variability) | 1 net new | 1,376 |
| Removed declined consent | 45 | **1,331 final** |

Total removal rate: 12% — within normal range for survey data.

## How we identified poor quality responses

We used a **converging evidence** approach (Meade & Craig, 2012): no single indicator can get you excluded. You need to fail on 2+ independent quality checks.

| Check | What it measures | Threshold | Flagged |
|---|---|---|---|
| Speed | Completed impossibly fast | < 53 seconds | 77 (5%) |
| Response variability | Same answer pattern throughout | 5th percentile | 73 (5%) |
| Straightlining | Same answer code ≥80% of questions | 80%+ | 1 |
| Open-end quality | Gibberish or keyboard spam | Heuristic | 1 |

16 respondents failed on both speed AND variability — all completed in under 53 seconds with near-identical response patterns. 15 of these had also abandoned the survey (already removed).

The remaining 120 single-flag respondents were retained. Single-flag ≠ bad data; it could be someone who legitimately finished quickly or happened to pick similar answer codes.

## Missing data

Almost all missing data is **by design** — the survey has extensive branching logic where questions only appear based on prior answers. For example:
- Q5 (what was difficult?) only shows if you said signup was difficult
- Q7 (why a card?) only shows if you said your first task was the card
- Q13/Q14 only show if you said you didn't complete your task

No imputation was needed.

## What we added

After cleaning, we enriched each respondent with:
- **Lifetime revenue and volume** from `RPT_CORE_ANALYTICS.PROFILE_MONEY_MOVEMENT`
- **Adoption milestones** from `RPT_PRODUCT.CONSUMER_ONBOARDING_FLOW`
- **Conversion flag** (converted vs drop_off) based on Q11
- **Friction score** (0-4) combining difficulty, hesitation, and help-needed indicators
- **Sample adequacy flag** noting the drop-off sub-sample is underpowered for segmentation

## Pipeline

Data cleaning used Bryan Carroll's [Survey Quality Agent](https://github.com/bcarroll-wise/Quantitative-UXR).

[← Back to home](index.md)
