# 5. Weekly supervisor report and Slack alerts

**Goal.** Turn the findings into a weekly routine for supervisors, without them having to open a dashboard.

**Weekly report** (sent every Friday morning, built from the week's recordings)
- Channel summary: visits, visits with an analysed recording, conversations with the business, applications / accounts.
- Agents split into best / medium / weak **from that week's funnel** (agents with 20+ visits).
- **Coaching criteria** per agent, each with a threshold, an action (coach / field ride-along / QA check) and a suggested line for the pitch:
  1. Explained the steps after the link (share of applications) — below 70% → coach
  2. Application with nobody from the business on the recording — every case → QA listens
  3. Client agreed to open the account in their own words — every case → QA listens
  4. Mentioned the card, opening in minutes or cashback — below 40% → coach
  5. Mentioned no benefit at all — above 35% → field ride-along
  6. Gave a reason to decide today — below 25% → coach
  7. Passive agent — above 50% → field ride-along
  8. Owner absent: got their WhatsApp or an appointment — below 1 in 10 → field ride-along
- Each flag links to the exact recordings and minutes to listen to, so coaching starts from evidence.

Example of the week format: 2,081 visits → 1,406 with an analysed recording → 1,210 conversations → 53 applications / 37 accounts.

**Daily Slack alerts**
- Agents with many meetings but no applications, applications without a client on the recording, and other AQA
  flags that need a same-day check.

**Engineering.** Python jobs in **GitLab**, developed with **Claude Code**; Snowflake as the source; Slack bot for delivery.
