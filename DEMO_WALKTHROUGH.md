# Demo: one publication, end to end

A complete walkthrough of the ISSC review process as it would play out on GitHub, mapped
step-by-step to the Publication Review Manual (v1.0). Everything below is **fictional** —
names, handles, and dates are invented — but every action is a real thing you would do in
this repository. The cover page used here is [`Publications/EXAMPLE_photoz_sbi.md`](Publications/EXAMPLE_photoz_sbi.md).

**Scenario.** A paper, *"Calibrating Photometric Redshift Uncertainties for LSST with
Simulation-Based Inference,"* prototyped at the ISSC Photo-z Interest Group hackathon.
Because it was fostered by an ISSC activity, it is **Category 1 · Mandatory**, **Class a · Paper**,
**Timeline ii · Standard**.

---

## Stage 0 — Registration  *(Manual §3, steps 1–3)*

**Author → PubCom (Slack #issc-pubcom):**

> Hi PubCom — requesting internal review. Title: *Calibrating Photometric Redshift
> Uncertainties for LSST with SBI.* Authors: Rivera, Okonkwo, Sundaram. Abstract attached.
> Preliminary **1 · Mandatory**, **a · Paper**. We'd like **@lindqvist-photoz** invited as an
> expert reviewer. Author contacts: @rivera-astro (ISSC) and @okonkwo-ml.

**Chair → authors:** assigns **@handler-hermine** as Paper Handler.

**Paper Handler → authors:** confirms the work is in ISSC remit, keeps Category 1 / Class a,
and — because it's a standard-length paper — sets **Timeline ii · Standard (2-week First Review)**.
Reminds them of the next steps.

*(Optional: a [registration issue](.github/ISSUE_TEMPLATE/register-publication.md) is opened for a public record, labeled `status: registered`.)*

---

## Stage 1 — Author opens the review PR  *(Manual §3, steps 4–6)*

1. **Branch:** `Branches → New branch` → `photoz-sbi-calibration` off `main`.
2. **Cover page:** copies `Publications/summary_doc_template.md`, fills every field (see the
   [completed example](Publications/EXAMPLE_photoz_sbi.md)) — note the **enumerated section
   outline** at the bottom, which reviewers will key their comments to — saves it as
   `Publications/EXAMPLE_photoz_sbi.md`, and commits.
3. **Draft PR:** `New Paper` template, pastes the cover-page text into the description under the
   checklist. **Assignees:** @rivera-astro, @okonkwo-ml, @handler-hermine. **Reviewers:** none yet.
   Opens it as a **Draft**.

> **PR #42 · [Draft] Photo-z uncertainty calibration with SBI**
> Author checklist ticked · category/class/timeline filled · outline enumerated · opened as draft ✔

---

## Stage 2 — Paper Handler opens the First Review  *(Manual §3, steps 7–8)*

@handler-hermine:
- checks procedural compliance — cover page complete, link resolves, outline present ✔
- applies labels: `Mandatory` · `class: a — paper` · `Standard` · `status: first review`
- converts **Draft → Ready for review**
- adds the requested expert **@lindqvist-photoz** to **Reviewers**
- emails the ISSC:

> *Subject: [ISSC review] Photo-z uncertainty calibration with SBI — comments by May 19*
> A new Category-1 paper is open for review: PR #42 [link]. Abstract: […]. Publication: [Overleaf link].
> Standard stream — First Review closes **19 May 2025**. All ISSC members are welcome to comment.

---

## Stage 3 — First Review  *(Manual §3, step 9)*

Reviewers comment. Note the two comment types and the 👍 upvotes.

**@lindqvist-photoz** — line comment on *Files changed*, §5 Calibration metrics:

> **Request:** PIT alone can hide dispersion errors — please add a coverage test at the 68%
> and 95% levels, otherwise the calibration claim isn't fully supported.  👍 4

**@bui-stats** — under *Conversation*:

> Suggestion: Fig. 3 would read better with the baseline and SBI curves on shared axes. 👍 1

**@okoro-cosmo** — line comment, §6 Results:

> **Request:** State the spectroscopic sample size and selection — the faint-end gain depends on it. 👍 3

The most-upvoted comment (Lindqvist's, 👍 4) is the priority to resolve.

---

## Stage 4 — Authors respond & revise  *(Manual §3, steps 10–11)*

Authors reply in each thread, quoting and tagging the reviewer:

> @lindqvist-photoz — added 68%/95% coverage in new Table 2; SBI is within 1σ at both levels,
> the baseline is over-confident at 95%. Thanks — this materially strengthened §5, and we'd like
> to **offer you co-authorship**.

> @okoro-cosmo — added N=8,412 spec-z with the selection function in §2; faint-end gains hold.

> @bui-stats — merged Fig. 3 onto shared axes. 👍

They upload **v2** of the PDF at the Overleaf link and ping @handler-hermine.
The co-authorship offer to @lindqvist-photoz is logged in the thread *(Manual §3, step 5)*.

---

## Stage 5 — Paper Handler closes the First Review  *(Manual §3, steps 12–13)*

@handler-hermine emails reviewers to re-review and resolve.
- @okoro-cosmo: satisfied → resolves their own comment.
- @bui-stats: suggestion, addressed → resolved.
- @lindqvist-photoz: hasn't clicked resolve by the deadline. Authors say it's addressed.
  Because a `Request:` is in play, the Handler **carries it into a Follow-up Review** rather than
  force-resolving. Label → `status: follow-up review`.

---

## Stage 6 — Follow-up Review  *(Manual §3, "Follow-up Review")*

Same steps (9–13) against **v2**. @lindqvist-photoz reads the new Table 2:

> Coverage table resolves it — calibration claim now supported. Resolving. Happy to accept the
> co-authorship offer.

No new `Request:` comments are raised, so no second follow-up is needed.
*(Had a reviewer raised a brand-new Request the Handler agreed with, one more follow-up could run — but no more than that.)*

---

## Stage 7 — Release & final decision  *(Manual §3, step 8; §1 step 8–9)*

@handler-hermine sets `status: released` and writes the recommendation:

> All `Request:` comments resolved; one suggestion adopted. Recommend approval. Reviewers
> @lindqvist-photoz, @okoro-cosmo, @bui-stats engaged; @lindqvist-photoz added as co-author.

**PubCom Chair** records the final decision on the PR:

> Approved. Cleared for submission to ApJ.

---

## Stage 8 — ISSC attribution & close  *(Manual §3, final paragraph)*

Because this is **Category 1 · Mandatory**, the author list gains the collaboration line:

> R. Rivera, N. Okonkwo, P. Sundaram, **E. Lindqvist**, *and The LSST Informatics and Statistics
> Scientific Collaboration*

*(An **Encouraged** paper would carry the same collaboration author line; an **Optional** paper
would instead add an acknowledgement thanking the ISSC for the internal review — no ISSC authorship.)*

The final version is posted to the PR, label → `status: concluded`, and the PR is **merged**.
Only now may the authors submit to the publisher.

---

## Manual → GitHub cheat-sheet

| Manual step | Who | GitHub action |
|-------------|-----|---------------|
| Register (title/authors/abstract/cat/class) | Author | Slack/email to PubCom (optional registration issue) |
| Assign Paper Handler | Chair | — |
| Set category/class/timeline | Paper Handler | Confirm on cover page + labels |
| Branch + cover page + draft PR | Author | New branch, commit `Publications/<name>.md`, open Draft PR |
| Open First Review | Paper Handler | Draft→Ready, add reviewers, email ISSC, `status: first review` |
| Post comments | Reviewers | Line/Conversation comments, `Request:` prefix, 👍 upvote |
| Respond + offer co-authorship + revise | Author | Reply in threads, upload revision |
| Close First Review | Paper Handler | Reminder email; original commenter resolves; Handler adjudicates |
| Follow-up (repeat ≤ once more) | All | Repeat against revised version, `status: follow-up review` |
| Release + recommend | Paper Handler | `status: released`, recommendation comment |
| Final decision | Chair | Decision comment |
| ISSC attribution / acknowledgement | Author | Update author line / acknowledgement, `status: concluded`, merge |
