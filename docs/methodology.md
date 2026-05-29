# Methodology & Limitations

## Study Design

| Parameter | Value |
|---|---|
| Method | Self-administered online survey (Qualtrics) |
| Population | New Wise consumer customers who registered ~30 days prior |
| Markets | US, UK, Philippines |
| Language | English only |
| Period | Oct 22 – Nov 25, 2025 |
| Incentive | Prize draw: 5x £100 GBP equivalent vouchers |
| Distribution | Email via CRM |

## Sample

| Metric | Value |
|---|---|
| Raw responses | 1,513 |
| After cleaning | 1,331 |
| Target (per research plan) | 385 minimum |
| Achieved | 3.5x target |

## Data Enrichment

Survey responses were matched to Snowflake data via `user_id`:
- **LTV data** from `RPT_CORE_ANALYTICS.PROFILE_MONEY_MOVEMENT` (lifetime volume, revenue by product)
- **Adoption data** from `RPT_PRODUCT.CONSUMER_ONBOARDING_FLOW` (job adoption timestamps, KYC milestones, activation type)

Match rate: 1,329 of 1,331 (99.8%)

## Statistical Tests Used

| Test | When used |
|---|---|
| Spearman rank correlation | Ordinal survey variables → continuous LTV |
| Point-biserial correlation | Binary indicators → continuous LTV |
| Mann-Whitney U | Two-group comparisons (non-parametric, for skewed revenue data) |
| Kruskal-Wallis H | Multi-group comparisons (non-parametric) |
| Chi-square test of independence | Categorical × categorical associations |
| Cramér's V | Effect size for chi-square |

All tests use α = 0.05. Revenue data is heavily right-skewed; medians and non-parametric tests are used throughout.

## Limitations

### Sample Bias

1. **Self-selection bias** — only ~1% of invited customers responded. Respondents are likely more engaged with Wise than non-respondents.
2. **Survivorship** — only captures customers who successfully registered. Those who abandoned during registration are invisible.
3. **89% said they completed their task** — sample heavily skews toward converted customers. The 147 "drop-offs" are underpowered for segmented analysis (n=147 vs 385 target for this group specifically).

### Measurement Limitations

4. **Q10 ("regularly") interpretation** — the team identified that this term may be interpreted retrospectively rather than prospectively. Behavioural data supports this concern (respondents answering "regular" had already adopted at median 0 days).
5. **Q11 (self-reported completion) doesn't match behavioural data** — 81% of "not yet" respondents have actually adopted per Snowflake. The question may be measuring intent-specific completion rather than general adoption.
6. **No attention checks** — survey included no embedded attention check questions. Converging evidence approach used as mitigation.
7. **Q15 responses indicate question confusion** — several respondents answered "I am using it" or "don't understand question" when asked why they decided not to use Wise.

### Analysis Limitations

8. **Correlational, not causal** — all relationships reported are associations. We cannot determine whether friction causes lower LTV or whether lower-LTV customers perceive more friction.
9. **Small sub-group sizes** — hesitation sub-types range from n=9 to n=46. Individual type-level findings should be treated as directional.
10. **No regional breakdown** — the survey was English-only across US/UK/PH but we cannot identify which market respondents are from via survey data alone (no country question in active survey flow).

### Drop-Off Sample Adequacy

| Metric | Target | Achieved |
|---|---|---|
| Overall sample | 385 | 1,331 ✓ |
| Drop-off sub-sample | 385 | 147 ✗ |
| Margin of error (drop-offs) | 5% | ~8% |
| Per-segment minimum | 100 | Not achievable with n=147 |

**Recommendation:** Drop-off findings are directional. Comparison between converted (n=1,184) and drop-off (n=147) has adequate power. Segmentation within the drop-off group does not.

## Data Cleaning Pipeline

See [Data Cleaning & Quality](cleaning.md) for full details.

- Converging evidence approach (Meade & Craig, 2012)
- No single indicator sufficient for exclusion
- 2+ independent flags required for removal
- Overall exclusion rate: 12.1% (within normal 10-20% benchmark)

## Reproducibility

- Cleaned data: `Consumer_Drop_off_survey_cleaned.csv`
- Survey definition: `Consumer_Drop_off_survey.qsf`
- Cleaning pipeline: Bryan Carroll's [Survey Quality Agent](https://github.com/bcarroll-wise/Quantitative-UXR)

[← Back to Index](index.md)
