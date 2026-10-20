# Role cards — ISSC PubCom mock submission review

**Everyone:** use the *same new PR opened by the volunteer author*; never reuse the old demo PRs. The [exercise runbook](EXERCISE_RUNBOOK.md) lists the timing. This public test contains entirely fictional data.

## Volunteer corresponding author — before meeting + response round

**Before:** download the separate author packet, follow [Author handoff](AUTHOR_HANDOFF.md), create one publication branch and open **one Draft PR** with `summary.md`, `manuscript_v1.md`, and `manuscript_v1.pdf`. Title it `[MOCK SUBMISSION] Photo-z uncertainty calibration with SBI`. Make the PR link available to the Handler.

**At meeting:** answer individual comment threads; when possible add `manuscript_v2.md` **to the same branch**. In v2, honestly identify tests that still need to be carried out rather than inventing coverage statistics. Update `summary.md` revision log and cite affected sections in your replies. Do not resolve a `Request:` merely because you have responded.

**Complete when:** reviewers can compare manuscript versions and see your specific replies.

## Paper Handler — controls the process

**Screening:** check author contact, manuscript access, first version/date, abstract, section outline, category justification, class, timeline stream and data-rights declaration. For the *simulation*, you may use `Mandatory`, `class: a — paper`, `Standard` provided the category rationale is marked **fictional**. Tell the author if anything is missing.

**Open:** choose **Ready for review**, add reviewer accounts under the PR's **Reviewers** sidebar, apply one category/class/timeline plus `status: first review`. Explain the *mock* comment deadline. Do not confuse an `@mention` with a formal review invitation.

**Close:** after replies and revision, make a mini-table in Conversation listing every `Request:` → author's action → reviewer confirmation → unresolved scientific requirement. If feedback remains, record follow-up/conditions instead of resolving blindly. Post a **recommendation** to the Chair, distinguishing scientific adequacy from the success of the workflow test. Where feasible, avoid being both author and final reviewer.

## Reviewer 1 — train/test independence

1. Open submitted PR → **Files changed** → `manuscript_v1.md` → §2–3.
2. Hover a changed line and press **+** → **Start a review**. Add a concrete scientific concern with `Request:` prefix and state the remedy or evidence needed. The main issue to consider is independence of training and testing for different noise realizations of the same simulated galaxy.
3. In **Review changes**, choose **Comment** → **Submit review**. For this exercise do not choose platform **Approve** or **Request changes** unless asked to test them.
4. After v2, reply in the same thread to say whether the response is sufficient. Resolve only if satisfied and permitted; otherwise tell the Handler explicitly.

## Reviewer 2 — posterior validation and clarity

1. Open PR → **Files changed** → manuscript §4–5; also examine abstract and conclusions.
2. Add a `Request:` focused on evidence for claimed 68% / 95% calibration, the independent test set, and uncertainty / magnitude-stratified results.
3. Add a `Suggestion:` for figure, baseline description or reporting clarity. Use **Review changes → Comment → Submit review**.
4. Re-read v2 and mark each point as addressed, partially addressed or still outstanding. Do **not** accept fabricated numerical results.

## PubCom Chair — responsible for the recorded outcome

1. Assign Handler and reviewers in the exercise plan and ensure no inappropriate self-approval.
2. Read the Handler's written recommendation and check that each material concern has a disposition.
3. Write a **separate dated Conversation comment**: `MOCK PUBCOM DECISION — return for revision / conditional hold / cleared for exercise purposes`, reasons, open conditions and responsible person(s). Clarify `No authorization for real submission or publication`.
4. Ensure the training PR has a clear disposition; do not interpret GitHub **Approve** or merging as a committee vote.

## Observer / timekeeper — optional

Record time, access problems, confusing UI controls, review thread discoverability, role overlap, how revisions are linked, and where real-policy guidance is required. Use [debrief checklist](DEBRIEF_CHECKLIST.md).

## GitHub button ≠ committee action

| GitHub action | What it records | What it does **not** establish |
|---|---|---|
| Draft PR | Author is preparing a change | No formal review started |
| Ready for review | GitHub PR accepts review requests | No automatic publication review clock |
| Review → Comment | Feedback by an individual | No final PubCom outcome |
| Review → Request changes | Reviewer has chosen an adverse platform review state | Not necessarily a policy-defined rejection or merge block |
| Review → Approve | GitHub reviewer approves a PR diff | Not PubCom Chair's authorization |
| Resolve conversation | An inline discussion is marked resolved | Does not prove scientific evidence was supplied |
| Merge | The branch was incorporated into base branch | Does not confer publication permission |
