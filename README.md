# Consumer Onboarding Drop-off Survey 2025

## For the team: asking questions about this data

This repo contains the findings from the consumer onboarding drop-off survey (Oct–Nov 2025). You can ask Claude questions about the results without needing to touch the data yourself.

### How to use

1. Open this project in Claude Code (or open the folder in VS Code with the Claude Code extension)
2. Ask your question in plain language — e.g. "What were the main reasons people didn't convert?" or "How does signup difficulty relate to LTV?"
3. Claude will answer from the pre-computed findings

### What you can ask

- What the survey found (distributions, themes, comparisons)
- How friction points relate to lifetime revenue
- What the behavioural data shows about adoption
- Methodology, sample size, limitations
- Whether a specific finding is statistically significant

### What Claude won't do

- Show you raw data or individual responses
- Run new statistical analysis or queries
- Access Snowflake, CSV files, or any data source
- Create new charts or custom cuts

If your question isn't covered by the existing findings, Claude will give you a formatted message to paste into the [analysis request Slack thread](https://wise.slack.com/archives/G5EAY3A2K/p1780065856485829). Christina will pick it up from there.

### Why it works this way

The survey contains responses from real customers with user_ids attached. Restricting raw data access ensures we handle it responsibly while still making the insights broadly available to the team.

---

## For Christina: what's in this repo

- `docs/` — GitHub Pages site with full analysis ([live site](https://christinacheadlewise.github.io/consumer-dropoff-survey-2025/))
- `.claude/skills/dropoff-survey-insights.md` — the skill file that powers team Q&A
- `Consumer_Drop_off_survey_cleaned.csv` — cleaned dataset with LTV + adoption enrichment (gitignored)
- `Consumer_Drop_off_survey.qsf` — Qualtrics survey definition

### Data collection

- **Period:** 22 October – 25 November 2025
- **Sample:** 1,331 cleaned responses (US, UK, Philippines, English only)
- **Enrichment:** Matched to Snowflake lifetime revenue + onboarding flow data (May 2026)
