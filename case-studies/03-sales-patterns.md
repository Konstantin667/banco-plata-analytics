# 3. How the best and the weakest agents sell

**Question.** Why do some agents convert 10× better than others with the same product and the same territory?

**Data and method**
- One month of DSA visits: 8,755 visits in surveys, 6,021 with a transcript, **5,866 reviewed by the model**.
- Agents with 60+ visits compared: **26 agents, 4,873 meetings** with a conversation.
- The LLM tagged each meeting with the AQA criteria plus a “sales approach” block: visit stages, benefits named,
  objections and answers, closing type, agent style, turning point — each backed by a quote.
- Groups were built **after** the model run, from the funnel (conversion = applications ÷ meetings):
  best (≥ 3.5% and ≥ 4 accounts), weak (≤ 1.2% and ≤ 2 accounts), medium (the rest). So the tagging was not fitted to the result.

**Findings**
- Conversion: best **5.6%**, medium **1.8%**, weak **0.5%**. Weak agents make almost half of all visits.
- All groups follow the same visit structure; the gap is in **what fills it**:
  the weak name no benefit in ~45% of meetings and make no closing attempt in ~44%.
- The medium talk the most — but about benefits a client can't relate to in two minutes (invoices, tax savings, the app).
- The best sell simply: free account, card in hand today, and **go straight to sign-up** (“I'll send you the link”).
- “I already have a bank” is the main objection; only the best answer it with a concrete benefit.
- **41–48% of visits end with the owner not on site**, and in 96–98% of them the agent leaves with no contact or time — the channel's largest untapped reserve.
- **An application becomes an account when the agent explains what happens next**: 92% of applications that became
  accounts had the onboarding steps explained vs 67% of those that did not. One sentence after sending the link.
- Conversion and compliance are separate: the best agents are not more compliant than the weak.

**Actions**
- Coaching criteria for supervisors (see case 5): explain the steps, ask for the owner's WhatsApp, give a reason to decide today.
- A list of applications with no client on the recording for QA review.

**Stack.** Snowflake · Python · LLM · Langfuse · deck in English for management
