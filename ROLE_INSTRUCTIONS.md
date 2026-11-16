# Role cards — ISSC PubCom mock submission review

**Everyone:** work on the **same new PR opened by the volunteer author**. Do not reuse old demo PRs. Use the [asynchronous exercise guide](ASYNC_EXERCISE_GUIDE.md) for timing and [review protocol](REVIEW_PROTOCOL.md) for detailed review instructions. The current public sandbox contains **fictional training data only**; it is not official scientific or journal clearance.

## Volunteer corresponding Author — submission and response

**Before the exercise:** follow [AUTHOR_HANDOFF.md](AUTHOR_HANDOFF.md). Create a single publication branch; prepare `summary.md` using the template and upload `manuscript_v1.pdf` plus the matching reviewable `manuscript_v1.md` in the same folder. The current mock format is PDF **and** Markdown; this is not yet a universal requirement for real manuscripts. If conversion from LaTeX or PDF is necessary, use [CONVERT_TO_MARKDOWN.md](CONVERT_TO_MARKDOWN.md).

- Open **one Draft PR** against `main` named `[MOCK SUBMISSION] Photo-z uncertainty calibration with SBI` and send its URL to the Handler.
- The summary carries metadata; the PR description needs only links, a short introduction and the checklist. Use complete GitHub file links from the publication branch to avoid redirection to **Compare changes**.
- Do **not** self-appoint scientific reviewers or start formal review before screening.

**During review:** once comments have been **submitted**, answer directly **in their original threads**, without waiting for the Handler to authorize each reply. Explain revisions or reasons for disagreement; do not manufacture missing coverage statistics. Add `manuscript_v2.md` (and ideally `manuscript_v2.pdf`) **to the same branch and PR**; update the summary revision log. A response alone does not resolve a substantive `Request:`.

**Complete when:** reviewers can identify each answer and compare the manuscript versions; the Handler can tell which requests remain outstanding.

## Paper Handler — intake, facilitation, and scientific disposition

**Screening:** check corresponding author, initial manuscript PDF and reviewable text, version/date, abstract, section outline, category justification, class, timeline, reviewer expertise/conflicts, rights and confidentiality. For the fictional pilot a sample `Mandatory` / `class: a — paper` / `Standard` classification may be used if clearly designated as **training**, not an actual policy determination. Request missing metadata rather than inventing it.

**Open the review:**

1. After intake, mark the Draft PR **Ready for review**, if authorized.
2. Apply one Category, Class, Timeline and **current** Status label.
3. Request reviewers through the **Reviewers** sidebar. An `@mention` is not a formal reviewer request.
4. Post the PR URL, manuscript version, reviewers and exact deadline/date/time zone.
5. Remind reviewers to use **Start a review → Add review comment → Submit review** to avoid unnecessary per-comment emails.

**While review is active:** authors and reviewers can interact directly after review submission. The Handler **does not gatekeep each reply**. Monitor deadlines, send a reminder if needed, adjudicate disputed scientific requests, identify non-responses, and coordinate any additional expertise. A reviewer PDF report is an **option under evaluation**, not the default for this mock exercise; if used, number requests and track point-by-point responses.

**Conclude:** prepare in PR Conversation a small table `Request | Author response | Reviewer follow-up | Outstanding condition`. Do not mark unvalidated claims scientifically resolved merely because a discussion was answered or a GitHub thread was closed. Make a **separate written recommendation** to the Chair. Do not confuse your ability to close/merge the PR with authority to approve a manuscript.

**Technical safeguard:** verify with the repo owner who may edit labels, resolve threads, close PRs, merge PRs and administer branch protections. The sandbox's public visibility and available rules are not an official ISSC permission model.

## Reviewer 1 — train/test independence

1. Read the submitted PDF and Markdown manuscript, focusing on §2–3.
2. In the PR select **Files changed → `manuscript_v1.md`**. Hover the relevant line and click **+**.
3. Type an actionable `Request:` concerning whether multiple noise realizations of the same galaxy appear in training and testing, and what remedy or qualification is needed.
4. Choose **Start a review**, **not** a single immediately published comment. Continue reading and add more issues using **Add review comment**.
5. Finish via **Review changes / Submit review → Comment → Submit review**. Do not use GitHub **Approve** or **Request changes** in this pilot unless the facilitator explicitly tests those platform states.
6. After the Author commits v2, reply in the original threads with `Addressed`, `Partially addressed` or `Still outstanding` and give reasons. Resolve only if the concern is actually addressed and your account is permitted to do so; otherwise tell the Handler.

## Reviewer 2 — posterior validation and clarity

1. Read the PDF and manuscript §§4–5 plus abstract/conclusions.
2. In **Files changed**, use a pending review to add a `Request:` on 68% / 95% coverage evidence, uncertainty, test-set independence, or magnitude-dependent performance.
3. Add at least one nonblocking `Suggestion:` about clarity of figures, MDN baseline description or reporting completeness.
4. **Submit all comments together** as a GitHub **Comment** review. This reduces multiple author notifications but does not guarantee only one email.
5. Recheck v2; do not accept invented quantitative results. Clearly identify which scientific claims remain unvalidated.

**Alternative to test later:** read the PDF and prepare a **single numbered referee-report PDF** as a PR Conversation attachment. The author supplies numbered responses and the Handler tracks each item. See [REVIEW_PROTOCOL.md](REVIEW_PROTOCOL.md). PubCom has **not** decided to adopt this instead of Markdown.

## PubCom Chair — independent internal process decision

1. Assign the Paper Handler and ensure sufficient independent reviewer expertise; avoid improper self-approval.
2. Read the Handler's recommendation and scientific-disposition table; confirm each material concern was considered.
3. Post a **separate dated PR Conversation comment** beginning `MOCK PUBCOM DECISION — return for revision / conditional hold / exercise-only process completion`, stating reasons, unresolved conditions and responsible persons.
4. State explicitly `Training only: no authorization for real publication or journal submission is conferred by this mock exercise.`
5. Decide whether to close the mock PR without merge or retain it as evidence. Do **not** treat technical GitHub approval or merge as a committee vote.
6. For future official deployment, seek administrator advice on privacy, cross-collaboration membership, authority to close/merge PRs, and any limitations of personal GitHub accounts. No official migration has been approved.

## Observer / timekeeper — optional

Record elapsed time, unclear instructions, difficulty with the branch and file links, access controls, review requests, email notifications, PDF/Markdown discrepancies, thread resolution, role overlap and the location of the final decision. Use [DEBRIEF_CHECKLIST.md](DEBRIEF_CHECKLIST.md) and share findings with the coordinator.

## GitHub controls versus ISSC scientific decisions

| GitHub control | What it records | What it does **not** mean |
|---|---|---|
| Draft PR | Author preparing proposed branch changes | Formal review has started |
| Ready for review | Platform can receive requested reviews | The ISSC policy clock started automatically |
| **Start a review** | Reviewer is collecting pending comments | Author has been notified of each pending item |
| **Submit review → Comment** | Complete review comments released | Scientific acceptance or a Chair decision |
| **Request changes** | GitHub's adverse review state | Automatically an ISSC rejection |
| **Approve** | GitHub reviewer supports merging diff | ISSC or journal approval |
| **Resolve conversation** | Discussion marked resolved in GitHub | Scientific evidence is necessarily adequate |
| Close / Merge PR | Repository history/state changed | Permission to publish or editorial acceptance |

## Important operational notes

- For this first mock, the Author, Handler and Reviewers should use **separate accounts where possible**. A coordinator's solo demonstration must label role-switch comments as **simulated** and cannot imitate an independent review approval.
- Anyone with read access can generally comment on a PR, but branch editing, labels, reviewer requests, resolutions, closing and merging may need higher repository permissions. **Verify actual settings**, don't infer controls from labels.
- For real manuscripts, reviewers' confidentiality, collaboration data rights and authorship provisions need appropriate policies and restricted access. The existing sandbox is public.
- Reviewer comments do **not automatically confer** authorship or builder recognition. Current approved ISSC and journal standards govern.
