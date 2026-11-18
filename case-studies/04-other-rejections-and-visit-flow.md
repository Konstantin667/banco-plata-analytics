# 4. Inside “Other”: rejection free text and the visit flow redesign

**Problem.** In the visit survey, agents often chose **“Other”** as the rejection reason and typed free text in Spanish.
The biggest rejection reason in the dashboard was effectively unknown.

**What I built**
- A report generator that pulls every “Other” record from Snowflake and **classifies the free text** with a keyword
  dictionary (`key / group / label / pattern`) stored in JSON next to the generator — adding a row adds a category
  on the next refresh, no code change.
- **Auto-discovery of new reasons**: unrecognised texts are grouped by identical wording; anything repeated above a
  threshold is promoted to a “new pattern” category for the build and shown with a ready-to-paste JSON row.
- Dynamics per category (day / week), filters by entity type, drill-down to records.

**Finding.** About **87%** of “Other” records (740 at the time) were **unfinished contacts** — owner not on site,
come back later, sent the link — not genuine rejections. The survey had no answer for these situations, so agents used “Other”.

**Product change: visit survey flow**
- Mapped the full visit flow in the agent app, screen by screen, from “Time to pitch” to the outcome
  ([`../artifacts/visit_screen_flow.html`](../artifacts/visit_screen_flow.html)), working in **Figma and Miro** with Product and Design.
- Proposed explicit branches for unfinished contacts (owner absent → capture contact / appointment) and routed the
  remaining “Other” to the account-type question, so rejections in the data became real rejections.
- Wrote the **agent field guide** (Spanish, mobile format) explaining the new flow.
- Requirements and tasks in **Jira / Confluence**.

**Stack.** Snowflake · Python · regex/keyword classifier · HTML report · Figma · Miro · Jira · Confluence
