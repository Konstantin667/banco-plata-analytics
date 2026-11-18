# Banco Plata — Business & Product Analytics Portfolio

Case studies from my work as a **Business Product Analyst at Banco Plata** (digital bank, Mexico City), Aug–Nov 2026.
I ran analytics for the **DSA (direct sales agents) acquisition channel**: field agents visit small businesses and open
Plata Empresa accounts for them. My job was to show where the funnel loses clients, why, and what to change in the
process and the product.

> **Confidentiality.** Everything here is rewritten for a public portfolio. Agent and client names, contacts,
> recordings, table names and raw company data are removed. Numbers are channel-level aggregates used only to show
> the method and the size of the effect.

## Results at a glance

| Area | What I did | Outcome |
|---|---|---|
| Channel ownership | Ran reporting and analysis for the DSA acquisition channel end to end | Meeting → application conversion up **3%** |
| Field sales reporting | Snowflake SQL + Python pipeline, HTML / Superset / Tableau dashboards | One source of truth for meetings, applications, accounts, plan and data quality |
| AI quality assurance (AQA) | LLM review of recorded sales meetings on 31 criteria, prompts and evals in Langfuse | Calibrated against human QA: **90–100% agreement on 16 of 29 compared criteria** |
| Sales patterns study | Compared best vs weak agents on 5,866 recorded meetings | Explaining onboarding steps is the strongest sign of an account: **92% vs 67%** |
| “Other” rejections | Classified free-text rejection reasons with a self-extending dictionary | **87%** were unfinished contacts, not rejections → visit survey redesign |
| Weekly report & alerts | Automated supervisor report (9 coaching criteria) and daily Slack alerts | Coaching focused on concrete agents, calls and minutes of audio |
| Telesales partner program | Funnel and error analysis for 23,751 calls, 7 agents | Survey/consent errors identified as the signal of “empty” registrations |

## Case studies

1. [DSA acquisition channel reporting](case-studies/01-dsa-channel-reporting.md)
2. [AI QA: LLM review of recorded sales meetings](case-studies/02-ai-qa-llm.md)
3. [How the best and the weakest agents sell](case-studies/03-sales-patterns.md)
4. [Inside “Other”: rejection free text and the visit flow redesign](case-studies/04-other-rejections-and-visit-flow.md)
5. [Weekly supervisor report and Slack alerts](case-studies/05-weekly-report-and-alerts.md)
6. [Telesales partner program performance](case-studies/06-telesales-partner-program.md)

Artifacts:
- [`artifacts/visit_screen_flow.html`](artifacts/visit_screen_flow.html) — interactive screen-flow map of the agent's
  visit survey in the app (open in a browser; labels in Russian).
- [`artifacts/aqa_calibration.md`](artifacts/aqa_calibration.md) — model vs human QA agreement by criterion.

## Stack

Snowflake (SQL) · Python (pandas, HTML report generators) · Superset · Tableau · LLM (GPT models) · Langfuse ·
GitLab · Claude Code · Slack bots · Jira & Confluence · Figma & Miro · Close & Crisp (client cases)

## How I work

1. **Start from the business question**, not the table: “why does a visit not turn into an application?”
2. **Build the funnel from raw events** and check data quality first (missing surveys, test visits, no client on audio).
3. **Look at what actually happens** — listen to / read the recordings at scale with an LLM, every claim backed by a
   quote and a timecode.
4. **Turn findings into one concrete change**: a coaching criterion, an alert, a survey screen, a sentence in the pitch.
5. **Automate the report** so the team sees the same numbers every week without asking.

---
Konstantin Rudnev · [LinkedIn](https://www.linkedin.com/in/konstantin-rudnev-a96727354) · [GitHub](https://github.com/Konstantin667)
