# 6. Telesales partner program performance

**Context.** A telesales queue called businesses to join a partner (referral) program: register, enter the platform,
invite other businesses who then open accounts.

**Scope.** One month: **23,751 calls**, 12,816 evaluated (≥ 20 s), 8,080 conversations, **7 agents**.
Report in three languages (ES / EN / RU) for the local team and management.

**Funnel.** 786 partners registered → 11.5% entered the platform → 8.7% sent invitations → 0 invited accounts yet.
Partners enter the platform a median of 8 days after the call (likely after the onboarding call).

**Findings**
- **Survey and consent errors** — the agent writes the client's answer for them and moves on without an explicit
  “yes” — are the main signal of **“empty” registrations**: more registrations, almost no platform entries or invitations.
- The total error rate does **not** explain results; the type of error does (reward-related or amount errors don't hurt activation).
- Proposed one agent metric that joins registration and activation: **active partners per 100 clients**.

**Stack.** Snowflake · Python · LLM review of calls · HTML report
