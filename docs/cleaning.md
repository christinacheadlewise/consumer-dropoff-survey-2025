# Data Cleaning & Quality

## Pipeline

Used Bryan Carroll's [Survey Quality Agent](https://github.com/bcarroll-wise/Quantitative-UXR) — a converging-evidence pipeline where no single indicator is sufficient for exclusion.

## Exclusion Summary

| Step | Removed | Remaining |
|---|---|---|
| Raw responses | — | 1,513 |
| Abandoned (Finished=0) | 136 | 1,377 |
| 2+ quality flags (speed + IRV) | 1 (net new) | 1,376 |
| Declined consent (Q30=5) | 45 | 1,331 |
| **Final clean sample** | **182 total (12.1%)** | **1,331** |

## Quality Indicators Applied

| Indicator | Threshold | Flagged | Notes |
|---|---|---|---|
| Speed | < 53s (33% of median) | 77 (5.1%) | Below 33% of median completion time |
| Straightlining | >= 80% | 1 (0.1%) | Low relevance — questions are categorical, not scales |
| IRV (low variability) | 5th percentile | 73 (4.8%) | Same caveat — choice codes, not Likert |
| Open-end quality | Heuristic fail | 1 (0.1%) | "Nothing"/"No" treated as legitimate |
| Attention checks | N/A | — | No attention checks in survey design |

## Converging Evidence Rule

- 2+ independent flags → auto-exclude (16 respondents, all speed + IRV)
- 1 flag → retain (120 respondents)
- 15 of 16 multi-flagged overlapped with abandoned responses

## Missing Data

**Mechanism: Missing By Design (branching logic)**

All high-missingness columns are conditional survey questions that only display based on prior answers. No imputation needed.

| Pattern | Explanation |
|---|---|
| Q5 missing (86%) | Only shown if signup was difficult/neutral |
| Q7 missing (62%) | Only shown if wanted Wise card |
| Q8/Q9 missing (78-80%) | Only shown for send/receive intent |
| Q13/Q14 missing (98%) | Only shown if didn't complete task |

The 45 missing on core questions = respondents who declined consent (removed).
24 with missing Q30 skipped consent but completed the full survey (retained).

## Wave Analysis (Nonresponse Bias)

| Comparison | Early (Oct 22–Nov 3) | Late (Nov 3–Nov 25) | Difference |
|---|---|---|---|
| Signup ease (Q4) | 4.44 | 4.32 | d=0.14, negligible |
| First task (Q6) | More card-focused | More send-focused | d=0.14, negligible |

**Conclusion:** No meaningful nonresponse bias detected. No weighting recommended.

## Respondent Pool

- Age: Well distributed 18–65+ (no concentration)
- 58% found signup "extremely easy" — expected positive skew for registered customers
- 89% completed their task — sample skews toward converted (expected per research plan)

[← Back to Index](index.md)
