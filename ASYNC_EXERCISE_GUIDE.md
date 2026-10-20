# ISSC PubCom — asynchronous mock publication review

**Pilot format:** one fictional manuscript, one volunteer submitting author outside PubCom, one Paper Handler, two reviewers and one PubCom Chair. The exercise spans **10 working days**, with no live meeting required. A short **optional recorded repository tour (5–7 minutes)** can be shared before Day 1.

> **TRAINING ONLY.** This repository is public. Do not upload real unpublished manuscripts, proprietary Rubin data, sensitive reviewer discussions, or personal records. A successful GitHub exercise is not authorization to submit a paper. The compressed schedule below tests the *workflow only*: it does **not** meet or replace any formally required ISSC review period. The current approved ISSC publication policy takes precedence.

## Start here — who reads what

- **Volunteer author:** [author handoff](AUTHOR_HANDOFF.md) and [role cards](ROLE_INSTRUCTIONS.md); obtain the **separate** mock-author packet from the organizer.
- **Paper Handler:** [role cards](ROLE_INSTRUCTIONS.md), [review protocol](REVIEW_PROTOCOL.md) and [runbook](EXERCISE_RUNBOOK.md).
- **Reviewers:** [role cards](ROLE_INSTRUCTIONS.md) and [review protocol](REVIEW_PROTOCOL.md).
- **Chair:** this guide, the [runbook](EXERCISE_RUNBOOK.md) and the **separate private** facilitator notes (never upload the answer key to this public repository).
- **Observer:** [debrief checklist](DEBRIEF_CHECKLIST.md).

**Timing note:** older role cards / author handoff refer to a live “meeting” or “session.” For this pilot, read such references as **your assigned asynchronous stage**. The scientific tasks and responsibilities are unchanged; **the timeline in this guide and the updated runbook replaces the old 60-minute timetable**.

## Before Day 1 — Chair / organizer

1. Confirm the [repository](https://github.com/lionandjelka/pubcom-sandbox-test) has the latest instructions on `main` and the volunteer knows how to open a **Draft Pull Request (PR)**. The Chair chooses a **kickoff date**; do not assume a calendar date from this document.
2. Assign **one volunteer author, one Paper Handler, Reviewer 1 and Reviewer 2**, all using different GitHub accounts where possible. Determine which participants have permission to create branches, request reviewers, apply labels, comment, and resolve threads. If review-request permissions are limited, the Handler should arrange access *before* Day 2.
3. Send the author the **separate submission ZIP** containing `summary.md`, `manuscript_v1.md`, and `manuscript_v1.pdf`. Do **not** preload the manuscript into `main` and do **not** circulate the private scientific answer key to reviewers.
4. Choose one communication channel for **notifications and reminders** (for example an agreed email thread plus GitHub @mentions) and one time zone for the pilot, such as **Europe/Belgrade**. In the kickoff message, supply **actual calendar dates and a cutoff time** for each stage. Working days exclude weekends and any holidays the team chooses to observe.
5. Share a short recorded tour (optional): locate README → open a PR → `Files changed` → comments/replies → status labels → separate Handler recommendation and Chair decision. The prior [demo PR #6](https://github.com/lionandjelka/pubcom-sandbox-test/pull/6) is for illustration; the new paper requires its **own PR**.

## Ten-working-day schedule

**Day 1 is the author's submission day.** Day 2 is the Handler's screening/activation day. Count weekdays only and publish calendar deadlines *before* starting; if a holiday or withdrawal occurs, revise dates explicitly in the PR, not silently.

| Working day | Responsible | Required action | Evidence to leave in GitHub |
|---|---|---|---|
| **Day 1** | Volunteer author | Upload `summary.md`, `manuscript_v1.md`, `manuscript_v1.pdf` together on a dedicated branch; open **one Draft PR** against `main`. | Draft PR URL; PDF, manuscript and summary visible under `Files changed` |
| **Day 2** | Chair and Handler | Chair confirms Handler. Handler checks classification, access, author/contributor fields, version and data-rights statements; assigns two reviewers, labels and mock deadlines; marks **Ready for review**. | Screening comment; review invitations; `status: first review`; explicit deadline |
| **Days 3–5** | Reviewers 1 and 2 | Independently read PDF and review `manuscript_v1.md` line by line. Post actionable `Request:`, `Suggestion:` and/or `Question:` comments. | Two separately submitted reviews or explicit “no concerns” replies; reviewer 1 methods, reviewer 2 validation |
| **Day 5** | Handler | Check responses; remind missing reviewers, summarize incoming items; close comment window or document extension. | Dated end-of-review comment and next deadline |
| **Days 6–7** | Volunteer author | Reply **in each thread**, upload `manuscript_v2.md` in the **same PR** and update the summary revision log. Do not fabricate numbers. | Version v2, cross-references to comments, author completion note |
| **Days 8–9** | Reviewers, Handler | Recheck v2; mark requests addressed / partially addressed / unresolved. Handler documents any follow-up, objections and adjudication. | Reviewer confirmations; current status label and issue-tracking comment |
| **Day 10** | Handler, Chair | Handler writes recommendation with unresolved conditions. Chair posts **separate mock decision**. Close or retain the training PR **without automatically merging** it. | Handler recommendation, dated Chair decision, clear `TRAINING ONLY — NOT REAL CLEARANCE` conclusion |

**Important:** Days 3–5 are a *training* First Review window, not a permitted replacement for the existing manual's longer streams. The follow-up is also compressed solely for testing. For real submitted papers, the approved review windows must be applied.

## Notification and non-response protocol

The **Paper Handler owns the clock**, not the author or reviewer. Every stage change should be visible in the **PR Conversation** and communicated using the agreed channel:

- **Day 2 opening notice:** PR URL, PDF and Markdown links, confirmed assigned reviewers, category/class/stream (for simulation), deadline with date/time/time zone, where and how to comment, and reminder that this is fictitious.
- **Day 4 or early Day 5 reminder:** nudge any reviewer who has not responded; avoid pressuring reviewers to approve.
- **Day 5 handoff:** summarize questions and `Request:` comments and give the author the Day 7 cutoff.
- **Day 7 handoff:** author posts v2 link and maps each request to their response; Handler notifies original commenters of recheck deadline.
- **Day 9 close of follow-up:** Handler documents item dispositions, including missing responses.
- **Day 10 final notice:** Chair's decision, whether further scientific work is needed, and exercise debrief link.

**If a participant does not respond:** (1) Handler sends one explicit reminder; (2) at the recorded deadline, Handler logs “no response” and asks the Chair whether to extend, replace reviewer, or complete the *workflow test* with a recorded gap; (3) the Chair records any change to deadlines or participants. **Silence does not count as approval**, and unresolved scientific requests must not be marked resolved for convenience.

## Precise GitHub workflow

1. **Author:** new branch → copy mock materials to `Publications/mock-photoz-sbi-exercise-2026/` → Draft PR. Do not choose `main` as the commit destination and do not reuse PRs #5 or #6. See [author handoff](AUTHOR_HANDOFF.md).
2. **Handler:** read the **PDF**, summary and reviewable Markdown. After screening, mark PR Ready, choose the **Reviewers** sidebar, and apply the relevant category/class/timeline and **one current** status label. A GitHub @mention is a useful notification but is **not** the same as a formal review request.
3. **Reviewers:** open **Files changed** → `manuscript_v1.md` → hover a line → **+** → **Start a review** → **Review changes → Comment → Submit review**. In the exercise, use `Comment` rather than GitHub's technical `Request changes` or `Approve`, unless explicitly testing those controls.
4. **Author:** answer the *same thread*, make a commit containing `manuscript_v2.md`, update `summary.md` with version/date and a change log; notify Handler when done. The v1 file remains for comparison.
5. **Reviewer recheck:** reference v2 section/line; if comments cannot attach to an unchanged file's diff, use the **Conversation** tab with an explicit version and section. Resolve only after an issue is genuinely addressed, or leave it open and state what remains.
6. **Handler + Chair:** distinguish addressed **wording** from resolved **scientific evidence**. Handler's recommendation is not the Chair's decision. The Chair posts a separate reasoned training decision. A green GitHub approval or merge is **not** ISSC publication clearance.

**Technical warning:** GitHub does not necessarily block merging while threads are unresolved; that depends on branch rules configured under Settings. The Handler should manually verify scientific closure irrespective of platform enforcement.

## Minimum reviewer objectives

Reviewer 1 examines whether the training/test split excludes **the same simulated source across realizations**. Reviewer 2 examines whether empirical coverage and uncertainty analysis support the **68%/95% posterior-calibration claims**. At least one optional presentation suggestion should also be tested. Comments should address the actual manuscript, not just its summary metadata. Reviewers should not know the Chair's private answer key.

## Ready-to-copy status messages

**Handler opens review (Day 2):**

> MOCK REVIEW OPEN — PR #[number]. Manuscript version v1 dated [date]. Reviewers: @[reviewer1] and @[reviewer2]. Please read the PDF and comment on the Markdown manuscript using `Request:`, `Suggestion:` or `Question:`. First-review responses due **[date, time, time zone]**. This is a training exercise, not an official ISSC review or clearance.

**Author submits revision (Day 7):**

> MOCK AUTHOR RESPONSE COMPLETE — v2 added on [date] as `manuscript_v2.md`; the change log in `summary.md` links each request to the response. Please recheck by **[date, time, time zone]**. Claims requiring new experiments have not been presented as validated results.

**Handler recommendation (Day 10):**

> MOCK HANDLER RECOMMENDATION — [return for revision / conditional hold / exercise-only procedural completion]. Requests addressed: [list]. Outstanding scientific evidence: [list]. Nonresponses/other process exceptions: [list]. Recommendation and reasoning: [brief explanation]. This is a training recommendation only.

**Chair's separate decision (Day 10):**

> MOCK PUBCOM DECISION — [return for revision / conditional hold / exercise-only procedural completion], recorded [date]. Rationale: [brief]. Conditions still outstanding: [list]. **Training exercise completed; this is not ISSC authorization for a real submission or publication.**

## Completion criteria and debrief

The pilot succeeds as a **workflow test** when the volunteer submits without PubCom doing it for them; the Handler starts and tracks review; two distinct reviewers submit comments; the author replies and commits a new version; reviewers or Handler record scientific dispositions; Chair posts a distinct reasoned decision; and all records remain findable without an oral explanation. **A return-for-revision decision is a valid and often scientifically appropriate outcome.**

Use the [debrief checklist](DEBRIEF_CHECKLIST.md). Record actual elapsed days, missed notifications, permission problems, confusing review UI, time spent, manuscript-version confusion, and what must change before a controlled real-publication pilot. Do not automatically merge the fictional paper into `main`.
