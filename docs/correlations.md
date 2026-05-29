# Correlational Analysis

## Spearman Correlations: Survey Variables → Lifetime Revenue

| Variable | rho | p | Significance |
|---|---|---|---|
| Completed task (Q11) | -0.182 | <0.0001 | *** |
| Countries lived in (Q2.1) | +0.116 | <0.0001 | *** |
| Signup ease (Q4) | +0.101 | 0.0002 | *** |
| Age (Q1) | +0.077 | 0.006 | ** |
| Frequency intent (Q10) | -0.046 | 0.28 | ns |
| Help needed (Q19) | +0.031 | 0.26 | ns |
| First task (Q6) | -0.018 | 0.52 | ns |

## Spearman Correlations: Survey Variables → Lifetime Volume

| Variable | rho | p | Significance |
|---|---|---|---|
| Countries lived in (Q2.1) | +0.176 | <0.0001 | *** |
| First task (Q6) | +0.139 | <0.0001 | *** |
| Completed task (Q11) | -0.147 | <0.0001 | *** |
| Signup ease (Q4) | +0.086 | 0.002 | ** |
| Age (Q1) | +0.043 | 0.12 | ns |

## Point-Biserial Correlations: Binary Indicators → Revenue

| Indicator | r_pb | p | Yes median | No median | Direction |
|---|---|---|---|---|---|
| Card-aware (send/receive) | +0.128 | <0.0001 *** | £30.45 | £25.38 | Awareness → higher |
| **Hesitated** | **+0.109** | **0.0001 **** | **£32.79** | **£25.65** | **Hesitation → higher** |
| Is expat (2+ countries) | +0.086 | 0.002 ** | £30.18 | £23.15 | Expat → higher |
| Regular intent (Q10=2) | +0.085 | 0.002 ** | £33.54 | £24.21 | Regular → higher |
| Completed task (Q11=1) | +0.060 | 0.03 * | £28.27 | £12.16 | Completed → higher |
| Had signup difficulty | -0.054 | 0.05 | £19.42 | £27.51 | Difficulty → lower |
| Used provider before | -0.044 | 0.11 | £28.99 | £25.75 | ns |
| Needed external help | -0.003 | 0.90 | £24.21 | £26.69 | ns |

## Inter-Variable Correlations

Which friction points cluster together?

| Var 1 | Var 2 | rho | p |
|---|---|---|---|
| Ease (Q4) | Hesitated (Q12) | -0.136 | <0.001 *** |
| Completed (Q11) | Help needed (Q19) | -0.124 | <0.001 *** |
| Ease (Q4) | Completed (Q11) | -0.089 | 0.001 ** |
| Age (Q1) | Hesitated (Q12) | +0.085 | 0.003 ** |
| Age (Q1) | Help needed (Q19) | -0.081 | 0.003 ** |
| Countries (Q2.1) | Ease (Q4) | -0.070 | 0.011 * |

**Key cluster:** Harder signup → more hesitation (rho=-0.14). But hesitators end up with higher LTV — they pushed through.

## What Predicts Drop-Off? (Effect Sizes)

| Predictor | Chi² | p | Cramér's V |
|---|---|---|---|
| **First task (Q6)** | **49.58** | **<0.0001** | **0.193 *** |
| Signup ease (Q4) | 12.53 | 0.014 | 0.097 * |
| Countries lived in | 6.85 | 0.23 | 0.072 |
| Age group | 4.97 | 0.55 | 0.062 |
| Used prior provider | 0.46 | 0.50 | 0.019 |

Only task type (V=0.19) approaches a "medium" effect. All other predictors are small or non-significant.

## Note on Q10 ("Regularly") Interpretation

The "regular transaction" answer correlates with higher LTV (r_pb=0.085, p=0.002) and faster adoption (median 0 days vs 1 day). However:

- The survey was sent to customers who registered ~30 days prior
- By the time they answered, many had already transacted multiple times
- "Regularly" may have been interpreted as "I already do this regularly" rather than "I intend to do this regularly"
- Behavioural data (DAYS_TO_FIRST_JOB = 0 for "regular" respondents) supports this: they'd already adopted before the survey arrived
- **Recommendation:** Treat Q10 as a descriptive segment, not a predictive signal. Follow-up interviews could clarify how participants interpreted the question.

[← Back to Index](index.md)
