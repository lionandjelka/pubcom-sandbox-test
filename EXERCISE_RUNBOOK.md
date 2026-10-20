# PubCom mock publication review — asynchronous runbook

**Format:** 10 **working days**, no live committee meeting required. The volunteer author submits a **fictional paper** through a Draft Pull Request; PubCom then processes that PR asynchronously. The authoritative step-by-step plan is [ASYNC_EXERCISE_GUIDE.md](ASYNC_EXERCISE_GUIDE.md). For responsibilities, use the unchanged [role cards](ROLE_INSTRUCTIONS.md) and [review protocol](REVIEW_PROTOCOL.md).

> **This replaces the previous 60-minute live-session runbook for this pilot only.** The short test schedule is **not** the formal ISSC publication-review timetable. The approved current ISSC policies govern real papers, authorship, data rights and clearance. This is a public training repository; use fictional/safe materials only.

## Organizer — before kickoff

- [ ] Decide Day 1 and write the **actual calendar deadline and agreed time zone** for every stage (working days exclude weekends and agreed holidays).
- [ ] Confirm the documentation upgrade is on `main`, but **do not upload the mock manuscript into `main`**.
- [ ] Assign a separate volunteer author, Chair, Handler, R1, and R2, with usable GitHub accounts and appropriate permissions.
- [ ] Give the volunteer the **separate author packet** (summary, Markdown manuscript and PDF), plus [AUTHOR_HANDOFF.md](AUTHOR_HANDOFF.md).
- [ ] Keep the Chair's **private answer key** out of this public repository; share a 5–7 minute orientation recording only if helpful.
- [ ] Announce the agreed notification channel, due dates and time zone to all participants.

## Workflow and owner handoffs

| Day | Owner | Required output | Handler's next notification |
|---|---|---|---|
| **1** | Volunteer author | One **Draft PR** with `summary.md`, `manuscript_v1.md`, `manuscript_v1.pdf` in a dedicated `Publications/<slug>/` directory | Acknowledge receipt and confirm PR URL |
| **2** | Chair / Handler | Handler assigned; intake completeness checked; PR marked Ready; classifications/status applied; two reviewers invited; deadlines recorded | Announce First Review start and cutoff |
| **3–5** | R1 and R2 | Independent written comments on **manuscript** lines, including actionable `Request:` items | Day 4/5 reminder as needed; compile requests |
| **6–7** | Volunteer author | Replies in the actual review threads; `manuscript_v2.md` in **same PR**; `summary.md` revision log updated | Notify reviewers of recheck deadline |
| **8–9** | R1 / R2 / Handler | Reviewers recheck; Handler lists resolved, outstanding and unacknowledged issues | Close follow-up and notify Chair |
| **10** | Handler then Chair | Separate Handler recommendation and dated Chair mock decision; process completion recorded | Post final training-only status and debrief |

## At each stage, the Handler documents

- **Opening:** one category/class/timeline and current status label, reviewers, current PDF/Markdown versions, due dates with time zone.
- **First Review close:** list each scientific request with author response deadline and any nonresponding reviewer.
- **Author revision handoff:** cite the v2 file and summary revision log and @mention relevant commenters.
- **Follow-up close:** table `Request | author action | reviewer confirmation | outstanding work`, including unanswered comments.
- **Final recommendation:** distinguish scientific adequacy from whether the GitHub workflow functioned. The Chair writes a **separate decision comment** with reasons and conditions.

**Handling silence:** send a dated reminder; if the deadline is missed, document nonresponse and let the Chair decide whether to extend the training window or record a test limitation. No reply is **never** equivalent to scientific approval. Do not quietly resolve an unresolved request or infer PubCom clearance from GitHub's Approve/merge controls.

## How this ends

- Post `TRAINING COMPLETED — NO REAL SCIENTIFIC CLEARANCE` in the PR Conversation, with direct links to the Handler recommendation and Chair decision.
- Keep the fictional submission PR as an auditable training record. **Do not automatically merge it** into `main`; if appropriate, close it without merge after comments are complete.
- Record issues using [DEBRIEF_CHECKLIST.md](DEBRIEF_CHECKLIST.md): access, notifications, discoverability, comment resolution, version control, responsibilities, and timeline feasibility.
- Retain the old [DEMO_WALKTHROUGH.md](DEMO_WALKTHROUGH.md) and [PR #6](https://github.com/lionandjelka/pubcom-sandbox-test/pull/6) as independent historical practice examples.
