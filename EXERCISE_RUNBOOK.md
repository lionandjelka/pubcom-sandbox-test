# PubCom exercise runbook: actual volunteer submission, then committee review

**Objective:** test publication intake, Handler appointment, two scientific reviews, author response, follow-up, Chair decision and archival traceability **on a PR submitted by someone outside PubCom**.

**Participants:** one volunteer corresponding author, one PubCom Chair/facilitator, one PubCom Paper Handler, two reviewers (preferably different accounts), and an optional observer. Existing historical PRs are **not** the exercise PR.

## Before the exercise (organizer)

**First, upgrade the repository:** upload the public documentation/templates package on a new setup branch and merge its documentation PR into `main` *before* the volunteer starts. This avoids pulling template edits into the same PR as the mock paper. The fictional manuscript and private reviewer answer key must **not** be uploaded to `main`.

**A day or two before the meeting:**

- Invite a volunteer author and email them the **separate author packet**. Share [author handoff](AUTHOR_HANDOFF.md) with them.
- Agree who is Chair, Handler and each reviewer. Check that **each person has a separate GitHub account** and appropriate permission to carry out their role.
- Ask the volunteer to commit `summary.md`, `manuscript_v1.md` and `manuscript_v1.pdf` under a unique `Publications/<slug>/` directory on their own branch and open a **Draft PR**, targeting `main`.
- Require the PR link before the meeting. If necessary, assign the Handler in a short pre-meeting message without initiating formal review.
- The Chair privately reviews the **facilitator answer key** supplied separately, not stored publicly in the repository.
- Check PR and reviewer access; Settings → Rules → Rulesets / branch protection as applicable. No rule is assumed to exist. Check whether reviewers have the *ability* to resolve conversations; if not the Handler can document and close after confirmation.

## Live session — 60 minutes

| Time | Lead | Action | Verifiable output |
|---|---|---|---|
| 0–5 min | Chair | Confirm aim, roles, PR link and mock-only status; assign/confirm Handler | Everyone opens the same author PR |
| 5–12 min | Handler | Read PR/files; check metadata, simulated data rights and manuscript v1; verify category/class/stream; record compressed mock deadline | Handler screening comment and labels |
| 12–15 min | Handler | Mark Draft PR **Ready for review**, request two reviewers and announce opening | Requested reviewers; `status: first review` |
| 15–28 min | Reviewers | Read PDF; comment **on Markdown manuscript lines**. At least two scientific `Request:` comments and one `Suggestion:` | Separate review comments by distinct accounts |
| 28–40 min | Author | Answer each thread; amend unsupported claims; commit `manuscript_v2.md` and update summary's revision log | Same PR shows v1 and v2, plus replies |
| 40–48 min | Reviewers | Examine v2; explicitly say what is resolved and what still requires work | Review follow-up, thread status |
| 48–53 min | Handler | Record each `Request:` outcome; recommend approval / conditional hold / return for revision | Formal Handler recommendation comment |
| 53–57 min | Chair | Post a **distinct decision comment** with reasons and conditions; this is not a real clearance | Chair decision in Conversation |
| 57–60 min | Observer / all | Identify permission, UI and policy issues; record next steps | Short debrief record |

**Mock deadline only:** The session's accelerated timing tests the mechanics; it does *not* satisfy the real publication manual's First Review or follow-up duration. For real reviews, the Handler records actual dates under the approved policy.

## What reviewers should actually inspect

Read the **manuscript content**, not merely the `summary.md` metadata. For this science case, test: sample independence; validity of train/test split; whether quantitative evidence supports stated calibration and faint-end claims; traceability of revised text. For specificity, cite manuscript section/lines. Avoid inventing missing data or giving automatic approval simply because language was softened.

## Correct scientific outcome is allowed to be “return for revision”

The exercise is successful even if the mock paper is **not** cleared. A review can document that missing independent validation requires further analysis. The Handler should separate resolved *wording* concerns from unresolved *scientific evidence* requests and recommend accordingly. The Chair should record a reasoned, clearly mock-only decision.

## After the meeting

1. In PR Conversation, label it clearly `TRAINING COMPLETED — NO SCIENTIFIC CLEARANCE` and link the Handler recommendation and Chair decision.
2. Remove outdated status labels and choose the most faithful status **only where current taxonomy supports it**. Do not use `status: concluded` to imply real scientific approval; explain completion in comments.
3. **Leave the PR open/close it as appropriate for the trial; do not automatically merge the fictional submission into `main`.** If preserving the PR in GitHub is the objective, closing without merge retains discussion history.
4. Fill the [debrief checklist](DEBRIEF_CHECKLIST.md) and decide what to adjust before real deployment.
