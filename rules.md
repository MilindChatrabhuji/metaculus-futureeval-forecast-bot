# Metaculus FutureEval & Bot Tournament Rules Sheet

Generated: 2026-11-02T08:24:00+05:30  
Updated: 2026-11-08T07:05:00+05:30 (TASK-0022 update per REVIEW-TASK-0013 issues 2, 3, 4, 5)  
Target Engine: `engines/forecast_bot`  

---

## 1. Current Season Name, Dates & Late-Entry Scoring
- **Tournament Series:** Metaculus AI Forecasting Benchmark / FutureEval Tournament Series (formerly AIB).
- **Current Active Cycle:** Fall 2026 FutureEval Bot Tournament (runs September 1, 2026 through December 31, 2026).
- **Upcoming Cycle:** Spring 2027 FutureEval (scheduled January – April 2027).
- **Late Entry Policy & Scoring:**
  - New bots may join at any time during an active tournament season.
  - Questions that opened and closed prior to a bot's registration or first prediction do not count against the bot as active failures; they are omitted from the bot's accuracy calculation or assigned a neutral prior baseline depending on minimum question coverage thresholds specified by Metaculus tournament admins.
  - Bots joining mid-season remain fully eligible for all open questions, future question drops, and concurrent bi-weekly MiniBench cash prizes.
- **Source URL:** https://www.metaculus.com/aib/ and https://www.metaculus.com/tournament/fall-futureeval-2026/

---

## 2. Prize Pool and Prize Distribution
- **Seasonal Prize Pool:** $50,000 USD per 4-month season across all developer-entered bots.
- **MiniBench Prize Pool:** $1,000 USD per bi-weekly round.
- **Annual Total:** Approximately $175,000 USD yearly across seasonal competitions and MiniBench cycles.
- **Prize Distribution Mechanism:** Prizes are awarded algorithmically using Metaculus's proper scoring rules (measuring calibration, log score / Brier score, sharpness, and accuracy relative to the Community Prediction and resolved real-world ground truth). Payouts are distributed across top-ranked bots according to leaderboard tournament scoring rules.
- **Source URL:** https://www.metaculus.com/aib/ and https://www.metaculus.com/tournament-rules/

---

## 3. Prize Eligibility & Bot Requirements
- **Human Age Requirement:** Developers must be 18 years of age or older.
- **"Commercial Bot" vs. Independent Bot Policy (Corrected per REVIEW-TASK-0013):**
  - **Commercial Bots:** Defined as bots created or sponsored by commercial entities, closed-source proprietary forecasting services, or venture-backed teams. **Full open-sourcing of code by the end of the season is required ONLY for commercial bots** wishing to claim cash prizes. Closed-source commercial bots may benchmark on leaderboards but cannot win cash.
  - **Independent / Research Bots:** Non-commercial, independent developers and researchers **do NOT have to open-source their code to win cash prizes**. Instead, non-commercial prize winners must share their source code or provide a detailed architectural methodology write-up with Metaculus staff and allow private inspection/verification upon request.
  - **Open-Source Incentive:** While not mandatory for independent bots, public open-source bots receive priority access to subsidized LLM API credits from Metaculus partners.
- **One Prize-Eligible Bot Per User:** Each participant or team is limited to **one prize-eligible bot**. Additional experimental bots may be run for research/benchmarking if explicitly registered/flagged, but only one bot per user is eligible for leaderboard prize payouts.
- **No Human-In-The-Loop:** The bot must run entirely autonomously. Human participants cannot view pending/open questions, inspect draft answers, preview forecasts on open or upcoming tournament questions, and manually adjust numbers or select forecasts prior to submission.
- **Rationale / Comment Requirement:** All prize-eligible bots are required to submit an explanatory comment/rationale alongside their numeric or probabilistic forecast directly on the question page.
- **No Blind Community Prediction Copying:** Bots may not programmatically scrape or mirror the Metaculus Community Prediction (CP) to bypass independent forecasting logic. Doing so leads to immediate disqualification.
- **Source URL:** https://www.metaculus.com/tournament-rules/ and https://www.metaculus.com/futureeval/participate/

---

## 4. Country & Jurisdiction Restrictions
- **Applicable Restrictions:** Competitions are open globally, except to individuals residing in countries or territories subject to United States comprehensive sanctions, trade embargoes, or export control regulations (such as Cuba, Iran, North Korea, Syria, Russia, and the Russian-occupied regions of Ukraine including Crimea, Donetsk, and Luhansk).
- **India Eligibility:** India is fully eligible to participate and receive tournament prize payouts, subject to standard local tax reporting and compliance with Indian foreign exchange/remittance laws.
- **Source URL:** https://www.metaculus.com/tournament-rules/

---

## 5. How to Register a Bot Account and Get an API Token
1. Maintain or create a primary human Metaculus account at https://www.metaculus.com/.
2. Access the Bot Participation portal at https://www.metaculus.com/futureeval/participate/ (or https://www.metaculus.com/aib/).
3. Register a dedicated bot account (naming convention typically incorporates a distinctive identifier or suffix).
4. Navigate to the bot settings / API profile page to retrieve the unique `METACULUS_TOKEN`.
5. Store the token securely as an environment variable (`METACULUS_TOKEN`), never hardcoding it in scripts or repository files.
- **Source URL:** https://www.metaculus.com/futureeval/participate/ and https://github.com/Metaculus/metac-bot-template

---

## 6. LLM & Search Credit Subsidies & Free-Tier Limits
- **Metaculus Provider Subsidies:** Metaculus partners with major AI providers (notably OpenRouter, OpenAI, Anthropic) to provide sponsored API credits for active competitors. Competitors request credits via the official Metaculus credit subsidy Google Form (https://forms.gle/aQdYMq9Pisrf1v7d8).
- **Zero-Cost Google AI Studio Route (Verified 2026-11-08 per REVIEW-TASK-0013 issue 3):**
  - **Active Free Model:** `gemini/gemini-flash-lite-latest` (or `gemini-3.8-flash`). Note: `gemini-1.5-flash` and `gemini-2.0-flash` have been retired by Google.
  - **Free Tier Rate Limits (per Google Cloud project):**
    - Requests Per Minute (RPM): **15 RPM**
    - Requests Per Day (RPD): **1,500 RPD** (resets daily at midnight Pacific Time)
    - Tokens Per Minute (TPM): **1,000,000 TPM**
  - **Official Documentation Source:** https://ai.google.dev/gemini-api/docs/rate-limits
  - **Privacy Note:** Google may use prompts sent on the free AI Studio tier to improve its products. This is acceptable for public forecasting questions, but private personal data must never be transmitted.

---

## 7. MiniBench Schedule and Prizes
- **Cadence:** Bi-weekly (every two weeks).
- **Prize:** $1,000 USD per round.
- **Purpose:** Fast turnaround benchmark that tests automated bots on shorter-horizon questions, allowing rapid validation of prompt adjustments and reasoning loops before or during longer seasonal tournaments.
- **Source URL:** https://www.metaculus.com/aib/

---

## 8. When and How Prizes are Paid
- **Timing:** Seasonal tournament evaluations resolve following the end of the competition period once ground-truth real-world events have closed and resolved. Final prize calculations typically conclude within 60 to 90 days post-season.
- **Payment Method:** Monetary prizes are issued as cash or cash equivalents (such as bank transfers, international wire, or virtual prepaid cards) at Metaculus's discretion.
- **Tax Documentation:** Prize recipients must submit standard tax identification documentation (e.g., IRS Form W-8BEN for non-US individuals, including Indian tax residents) and verify identity prior to remittance. Recipients are responsible for any applicable local taxes.
- **Source URL:** https://www.metaculus.com/tournament-rules/

---

## 9. Rules on Multiple Accounts
- **Single Individual / Single Group Limit:** Individuals or collaborating groups may only operate one prize-eligible account.
- **Sybil / Manipulation Ban:** Creating multiple accounts to take divergent positions, hedge probabilities, or artificially boost leaderboard standings is strictly prohibited and results in complete disqualification and account termination.
- **Source URL:** https://www.metaculus.com/tournament-rules/

---

## 10. Public GitHub Actions 60-Day Inactivity Rule
- **GitHub Policy:** Under GitHub Actions service terms, scheduled workflows (`on: schedule: cron: ...`) in public repositories are automatically disabled if the repository experiences **60 consecutive days of inactivity** (no commits or pushes).
- **Operational Requirement:** The bot's repository must implement a keep-alive mechanism to prevent scheduled workflow disablement, such as an automated periodic commit of a minimal run-log or health record by the workflow itself, or a monthly repository update.
- **Official Documentation:** https://docs.github.com/en/actions/managing-workflow-runs/disabling-and-enabling-a-workflow
