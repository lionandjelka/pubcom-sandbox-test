# Instructions for the volunteer mock-paper author

**Thank you for helping the ISSC PubCom test the submission process.** You are a volunteer author, *not* a PubCom reviewer, and will submit an intentionally fictional manuscript as though it were a new publication. The Committee will review your PR. You do **not** need to conduct original research or generate real results.

## Before the PubCom meeting

1. Ask the organizer for the **separate volunteer-author packet** (summary, `manuscript_v1.md`, and `manuscript_v1.pdf`). **These files are not included in the repository update on `main`**: your contribution must create the new review PR.
2. Confirm you can sign into GitHub and open the [sandbox repository](https://github.com/lionandjelka/pubcom-sandbox-test). Ask the organizer for sandbox collaborator access if you cannot create a branch.
3. Open `Publications/summary_doc_template.md` to understand the expected information. The volunteer packet already contains a partially completed fictional `summary.md`; finish its marked author fields and make the GitHub handle yours. **Do not add real sensitive information.**
4. Create a new branch of `main` and commit the three publication files in one directory, for example:

   ```text
   Publications/mock-photoz-sbi-exercise-2026/
     summary.md
     manuscript_v1.md
     manuscript_v1.pdf
   ```

5. Open **one Draft Pull Request** with base `main`. Suggested title: `[MOCK SUBMISSION] Photo-z uncertainty calibration with SBI`. Complete the PR checklist and send the PR URL to the organizer **before the meeting**. Do not invite reviewers or mark it Ready; that is the Handler's responsibility.

### Browser-only route (no command line)

1. Choose the `main` branch on **Code**, open **Add file → Create new file** and name it `Publications/mock-photoz-sbi-exercise-2026/summary.md`. Paste the contents of the packet's `summary.md`, replacing the author-name/GitHub-handle placeholders.
2. At the bottom, click **Commit changes**, choose **Create a new branch for this commit** and name it `mock-photoz-sbi-exercise-2026`, then commit.
3. Switch the branch selector to `mock-photoz-sbi-exercise-2026`; enter the new `Publications/mock-photoz-sbi-exercise-2026` directory. Choose **Add file → Upload files**, upload `manuscript_v1.md` and `manuscript_v1.pdf`, then commit to **the current branch**.
4. Use **Compare & pull request** and choose **Create draft pull request**, not the default ordinary ready PR if GitHub offers both choices. If the branch banner disappears, use the **Pull requests → New pull request** page; select base `main` and compare `mock-photoz-sbi-exercise-2026`.
5. Check the PR's **Files changed** tab shows the summary, the readable Markdown manuscript and the PDF. Paste the PR URL into your confirmation to the Handler.

If the website does not allow branch creation or upload, ask the organizer to grant *sandbox* write access. An unaffiliated public visitor cannot necessarily commit directly to this repository; a fork is a possible alternative but changes reviewer-assignment permissions.

## During the review

- Reviewers will leave requests in the **Markdown manuscript's** review diff. Read the PDF as the submitted document.
- Reply **in each comment thread**, not only as a general PR comment.
- For v2, do not manufacture missing scientific measurements. Acknowledge genuinely unsupported statements, revise claims, describe required further analyses, and upload `manuscript_v2.md` to the **same publication directory on the same branch**. Update `summary.md`'s revision log. A new v2 PDF is optional for this compressed mock exercise; a real manuscript workflow should keep a stable versioned manuscript PDF/link.
- Ask reviewers to confirm which comments are resolved. Do not yourself treat silence as review completion.

**Time expectation:** prepare the Draft PR before the session; during the exercise, respond to comments and create a brief v2. The paper is fictional and must never be submitted to a journal or arXiv.
