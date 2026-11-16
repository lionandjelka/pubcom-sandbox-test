# Volunteer author handoff — ISSC PubCom mock submission

Thank you for volunteering to test the ISSC publication-review workflow. This is a **fictional training manuscript** in a **public GitHub sandbox**. It is **not a real manuscript, official ISSC clearance, or journal review**. Do not upload confidential research, restricted Rubin data, private personal information, or nonpublic referee correspondence.

**Repository:** <https://github.com/lionandjelka/pubcom-sandbox-test>  
**Quick reference:** [role cards](ROLE_INSTRUCTIONS.md) · [review protocol](REVIEW_PROTOCOL.md) · [conversion guide](CONVERT_TO_MARKDOWN.md) · [summary template](Publications/summary_doc_template.md)

## What you receive and what you prepare

The organizer sends **two fictional manuscript files**: `manuscript_v1.pdf` (the paper-like presentation) and `manuscript_v1.md` (the same text for GitHub inline comments). You prepare `summary.md` yourself using the template. The first exercise intentionally tests whether you can follow instructions without a live walkthrough; ask for help and record points of confusion.

> **Format decision:** For this specific mock exercise submit **PDF + Markdown + summary**. The committee has *not* decided to make Markdown compulsory for every future real ISSC submission. If starting from LaTeX or PDF, use [CONVERT_TO_MARKDOWN.md](CONVERT_TO_MARKDOWN.md); if conversion fails, inform the Handler instead of altering scientific meaning to force conversion.

## A. Submit one paper through one Draft Pull Request

### 1. Check GitHub access

1. Sign into your own GitHub account and open the repository.
2. Confirm you can see the **Code** and **Pull requests** tabs.
3. If you cannot upload or create a branch, notify the coordinator with your GitHub handle and the exact missing control. Do not work around security settings using someone else's credentials.

### 2. Prepare `summary.md`

1. On `main`, open [`Publications/summary_doc_template.md`](Publications/summary_doc_template.md).
2. Click **Raw** or copy the content; create your own paper-specific copy under `Publications/mock-photoz-sbi-exercise-2026/summary.md`.
3. Fill in title, author contacts, abstract, section outline, data and software provenance, anticipated journal, and declared data rights.
4. Mark Category/Class/Timeline **provisional** until Handler screening; mark unknown fields `Pending Handler confirmation` rather than inventing values.
5. Clearly state `MOCK / TRAINING — fictional results`.

### 3. Create your publication branch

1. From the repository **Code** view, choose **Add file → Create new file**.
2. In the filename field enter the complete path `Publications/mock-photoz-sbi-exercise-2026/summary.md` and paste the prepared summary.
3. Scroll to **Commit changes** and select **Create a new branch for this commit**.
4. Use a unique name such as `mock-photoz-sbi-exercise-2026-<your-handle>`, substituting your handle and omitting angle brackets.
5. Commit. Confirm the branch selector shows **your branch**, not `main`.

An equivalent approach is to create the branch under **Branches → New branch**, then add files to it. There is no need to install Git or run command-line tools for this exercise.

### 4. Upload the PDF and Markdown files

1. Switch to your publication branch.
2. Enter the folder `Publications/mock-photoz-sbi-exercise-2026/`.
3. Choose **Add file → Upload files**.
4. Upload **both** `manuscript_v1.pdf` and `manuscript_v1.md` into that folder.
5. Verify the filenames and choose **Commit changes** on the **publication branch**.
6. Check the folder now contains `summary.md`, `manuscript_v1.pdf` and `manuscript_v1.md`.

**Do not create separate PRs for the summary and manuscript.** One paper = one publication branch = one PR. If you accidentally put a file in `main`, tell the coordinator rather than merging other changes without review.

### 5. Create the Draft Pull Request

1. Select **Pull requests → New pull request** or **Compare & pull request**.
2. Set **base = `main`** and **compare = your publication branch** (not a folder path).
3. Check that the only added files are the three mock submission files; investigate unrelated changes.
4. Title the PR `[MOCK SUBMISSION] Photo-z uncertainty calibration with SBI`.
5. Complete the auto-loaded PR checklist. You do **not** need to duplicate all information already recorded in `summary.md`.
6. Add short links to the manuscript and summary. For reliability, visit each file on **your branch**, copy its **full `github.com/.../blob/<branch>/...` URL**, and paste that URL into the PR description. Do not paste a bare relative folder path that opens GitHub's **Compare changes** screen.
7. Use the dropdown beside **Create pull request** and choose **Create draft pull request**.
8. Send the **PR URL** to the organizer / appointed Handler. **Do not invite reviewers**; the Handler will do so after screening.

### 6. Verify the PR before handing it off

- [ ] The page shows **Draft** status.
- [ ] The PR targets `main` from your publication branch.
- [ ] **Files changed** displays the summary, PDF and Markdown.
- [ ] The PDF file link actually opens the PDF.
- [ ] `summary.md` is complete enough for the Handler to assess intake.
- [ ] No sensitive or actual scientific material was posted to the public sandbox.
- [ ] Any missing feature / permission issue is recorded.

## B. Respond during review — you need not await permission for each reply

Once a reviewer has **submitted** feedback, you may answer directly in the relevant GitHub thread. You do **not** need to wait for the Paper Handler to release every individual comment. The Handler monitors the process, deadlines, scientific dispositions and follow-up requirements.

1. Open your PR **Conversation** and **Files changed** tabs to read the submitted review.
2. For every `Request:`, reply **within that original thread**: state what changed or why it was not changed, and refer to the relevant PDF/Markdown version and section.
3. Address `Suggestion:` and `Question:` comments where appropriate; never treat silence as approval.
4. For requests requiring new experiments, do not invent results. State which validation remains incomplete and qualify unsupported claims.
5. Add `manuscript_v2.md` and, if available, `manuscript_v2.pdf` to the **same branch and same PR**. Keep v1 files for comparison in this pilot.
6. Update the revision log in `summary.md` with v2/date, changes and links or references to the relevant discussions.
7. Add an author handoff comment: `MOCK AUTHOR RESPONSE COMPLETE — v2 added; please recheck the listed requests by [date/time/time zone].`
8. The reviewer rechecks and reports whether each concern is **addressed**, **partly addressed**, or **still open**. The Handler records any unresolved scientific requirement.

### What if you receive many separate email notifications?

In the first test the author received one email per separately posted reviewer comment. We now recommend that reviewers collect all inline comments with **Start a review → Add review comment → Submit review**. This reduces fragmented emails but may not force exactly one notification. See [REVIEW_PROTOCOL.md](REVIEW_PROTOCOL.md). For notification preferences, use your own GitHub **Settings → Notifications**; do not change another person's settings.

### What if the reviewer submits a single PDF report?

This is a proposed alternative under evaluation, not a replacement for the current pilot's Markdown workflow. The PDF report should have **numbered requests** (`R1.1`, `R1.2`, etc.). Post a corresponding **point-by-point author response** in the PR Conversation or attach a versioned response document. The Handler tracks every request and its disposition. Do not assume that attaching the PDF creates separate resolvable GitHub threads.

## C. Completing the mock exercise

Only the Handler prepares the **recommendation**, and only the designated Chair records the **separate decision**. Neither a completed GitHub comment nor a merged PR means the manuscript has passed journal peer review. The mock exercise may appropriately finish with **return for scientific revision** even when the GitHub procedure worked well.

Please tell the coordinator where you encountered unclear wording, unexpected permissions, missing notifications, or difficulty finding the latest file. Such feedback is the purpose of the pilot. The fictional manuscript must never be submitted to a journal or arXiv.
