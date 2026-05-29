# Job Adoption Analysis

Data from `RPT_PRODUCT.CONSUMER_ONBOARDING_FLOW` matched to 1,329 of 1,331 survey respondents.

## Overall Adoption Rates

| Metric | n | % |
|---|---|---|
| Has adopted any job | 1,199 | 90.2% |
| Has cross-currency job | 807 | 60.7% |
| Has shown intent | 1,308 | 98.4% |
| Has verified KYC | 1,271 | 95.6% |
| Send has adopted | 478 | 36.0% |
| MCA has adopted | 1,134 | 85.3% |

## Activation Type

| Type | n | % |
|---|---|---|
| MCA (multi-currency account) | 1,233 | 92.6% |
| Send money | 80 | 6.0% |
| Not activated | 16 | 1.2% |

## First Product Adopted

| Product | n | % |
|---|---|---|
| Other (MCA/card activation) | 1,157 | 88.4% |
| Send | 80 | 6.1% |
| Receive | 68 | 5.2% |
| Spend | 3 | 0.2% |
| Assets | 1 | 0.1% |

## Days to First Job Adoption

| Metric | Value |
|---|---|
| Median | 1 day |
| Mean | 8.2 days |
| p25 | 0 days (same day) |
| p75 | 9 days |

| Time to adopt | n | % |
|---|---|---|
| Same day | 110 | 8.4% |
| 1–7 days | 228 | 17.4% |
| 8–14 days | 129 | 9.9% |
| 15–30 days | 131 | 10.0% |
| 31–60 days | 79 | 6.0% |
| 61–90 days | 20 | 1.5% |
| 91–365 days | 6 | 0.5% |

## Friction Points → Adoption

### Signup Difficulty x Adoption

| Group | Adoption rate | XCcy rate | Med days | n |
|---|---|---|---|---|
| Had difficulty (Q5) | 85.8% | 52.6% | 2 | 192 |
| No difficulty | 91.0% | 62.1% | 1 | 1,139 |

Chi-square (adoption): p=0.037 *
Mann-Whitney (days): p=0.061

### Task Intent x Adoption

| Task | Adopted | XCcy | Send adopted | Med days |
|---|---|---|---|---|
| Card | 89.1% | 61.5% | 15.6% | 2 |
| Send | 92.2% | 69.4% | 69.4% | 1 |
| Receive | 90.3% | 57.4% | 55.4% | 0 |
| Invest | 93.3% | 30.0% | 23.3% | 0 |
| Other | 90.6% | 53.0% | 20.5% | 1 |

Invest users adopt quickly but have the lowest cross-currency rate (30%).

### Hesitation x Adoption Speed

| Group | Adopted | XCcy | Med days |
|---|---|---|---|
| No hesitation | 91.0% | 60.8% | 1 |
| Hesitated | 87.4% | 65.3% | 3 |

Hesitators take slightly longer but achieve HIGHER cross-currency adoption (65% vs 61%).

### Frequency Intent x Adoption

| Frequency | Adopted | XCcy | Med days | Med Rev |
|---|---|---|---|---|
| One time | 93.9% | 58.8% | 0 | £19.49 |
| Regular | 90.9% | 67.5% | 0 | £33.54 |
| Not sure | 89.1% | 52.5% | 1 | £13.45 |

⚠ See [Q10 interpretation note](correlations.md#note-on-q10-regularly-interpretation)

## Friction → Adoption Speed Correlations

| Indicator | r_pb | p | Yes med days | No med days |
|---|---|---|---|---|
| **Card aware** | **-0.104** | **0.0002 **** | **0** | **1** |
| Hesitated | +0.061 | 0.026 * | 3 | 1 |
| Had difficulty | +0.043 | 0.12 | 2 | 1 |
| Is expat | -0.049 | 0.08 | 1 | 1 |
| Needed help | +0.031 | 0.26 | 1 | 1 |

Card awareness is the strongest predictor of faster adoption.

## Critical Validation: Self-Report vs Behavioural Data

| Survey answer (Q11) | Actually adopted (data) | Not adopted |
|---|---|---|
| "Yes" (n=1,184) | 1,081 (91%) | 103 (9%) |
| "Not yet, but plan to" (n=119) | **98 (81%)** | 21 (19%) |
| "No" (n=26) | **20 (77%)** | 6 (23%) |

**Key finding:** 81% of self-reported "not yet" and 77% of "no" respondents HAVE adopted per Snowflake data.

**Why the discrepancy?**
1. Q11 asked about their **specific first intent** (Q6) — "did you manage to [send money / get card / etc.]?"
2. Behavioural data measures **any** job adoption
3. Many customers adopted a different product than intended
4. Some adopted after completing the survey (survey sent ~30 days post-registration, data is current)

**Implication:** The true non-adopter population is ~27 customers (those with HAS_ADOPTED=0), not the 147 self-reported "drop-offs." The problem is not adoption failure — it's intent-product mismatch and delayed activation.

[← Back to Index](index.md)
