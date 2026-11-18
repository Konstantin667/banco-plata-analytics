# 2. AI QA: LLM review of recorded sales meetings

**Problem.** Every visit is recorded, but human QA could listen to only a small sample. Compliance risks (false product
claims, surveys filled without the client's consent) and coaching opportunities were invisible.

**Solution: AQA (automated quality assurance)**
- An LLM reads each transcript and answers a fixed checklist of **31 criteria** in three groups:
  - **V — validity of the recording**: audio exists, enough speech, someone from the business is present, recording is complete.
  - **H — violations**: no client on the recording, survey says more than the client agreed, false product information,
    promising products that do not exist, price not explained, pressure, suggesting false data, selling third-party services.
  - **OBS / S — observations and sales behaviour**: benefits named, closing attempt, next step agreed, steps explained after the link.
- **Every answer must be backed by a quote and a timecode**, so a supervisor can open the audio at the right minute.
- Prompts, versions and evaluation runs are tracked in **Langfuse**; each prompt change is compared on the same labelled set.
- Output: a daily report by agent with the phrase, the problem and a “listen from mm:ss” link, plus a list of clients to revisit.

**Calibration against human QA.** QA labelled the same meetings by hand; I compared the model criterion by criterion
and iterated on wording. Round 2: **16 of 29 compared criteria at 90–100% agreement** (recording validity, most compliance
checks). Criteria with low agreement (e.g. “credit now” claims, recording completeness) were rewritten or
moved to “needs human check”. Full table: [`../artifacts/aqa_calibration.md`](../artifacts/aqa_calibration.md).

**Design choices**
- Rules a human can verify beat “scores”: yes/no/na per criterion + quote.
- Known allowed statements (e.g. paying taxes from the account) are filtered out to avoid false alarms.
- Severity levels (INFO / NOTE / WARN / CHECK / ESCALATE) decide who gets notified.

**Stack.** Python · LLM API (GPT) · Langfuse · Snowflake · Claude Code
