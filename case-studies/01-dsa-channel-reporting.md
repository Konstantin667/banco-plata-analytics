# 1. DSA acquisition channel reporting

**Context.** Field agents (“ambassadors”) visit small businesses, fill a visit survey in the app and send the owner a
sign-up link. Data lived in several places: survey events, meetings with audio, the origination funnel and HR records.
Nobody had one view of the channel.

**What I built**
- A **Snowflake SQL + Python pipeline** that assembles one record per visit from step-by-step survey events (JSON
  payloads merged in time order), joins meetings, audio transcripts, the application funnel and agent directories.
- An **agent-level report**: visits → conversations → applications → accounts, conversion, plan run-rate, visit
  timing and data-quality flags (no survey, test visits, no client on audio, visits far from the business location).
- Dashboards in **Superset / Tableau** and a self-contained HTML report refreshed on a schedule.

**Data-quality checks I added**
- Visits without a usable recording or with nobody from the business on it.
- Applications logged without a client present.
- Duplicate or test visits; time-zone normalisation (UTC → Mexico City) before any daily cut.

**Impact.** One source of truth for the channel used by supervisors and management; the basis for every study below.
Together with the coaching changes, meeting → application conversion grew by **3%**.

**Stack.** Snowflake · SQL · Python (pandas) · HTML/JS report generator · Superset · Tableau · GitLab
