# Volunteer author handoff — ISSC PubCom mock submission

Thank you for volunteering to test the ISSC PubCom publication-submission workflow. This is a **fictional training manuscript** submitted to a **public GitHub sandbox**, not an official submission or scientific result. Please use only the supplied training files and do not upload confidential research, proprietary Rubin data or personal information.

**Repository:** https://github.com/lionandjelka/pubcom-sandbox-test

**You receive only:** `manuscript_v1.pdf` (mock submission) and `manuscript_v1.md` (same text for line-by-line GitHub review). **You must prepare `summary.md` yourself** using the public repository template at [Publications/summary_doc_template.md](Publications/summary_doc_template.md). No prefilled summary is supplied, because we want to test whether the submission instructions are understandable without a live walkthrough.

## Before the committee review — submit the paper

1. **Check your access.** Sign in to GitHub and open the sandbox. If you cannot create a branch or upload a file, notify the organizer. You can report difficulty without solving it yourself.
2. **Start from `main`.** Open `Publications/summary_doc_template.md` in GitHub. Select **Raw** (or copy the file contents) and paste it into a new file named `Publications/mock-photoz-sbi-exercise-2026/summary.md`. Complete the summary's fields using the fictional manuscript. Identify yourself with your actual GitHub username only where the workflow requires a contact; mark unknown items **Pending Handler confirmation** instead of guessing. Class/category/timeline are *provisional* until the Handler checks them.
3. **Make a new branch.** At the foot of GitHub's file creation editor, choose **Commit changes → Create a new branch for this commit**. Suggested name: `mock-photoz-sbi-exercise-2026-<yourhandle>` (substitute your GitHub handle, without `< >`). Do **not** commit the file directly to `main`.
4. **Upload both manuscript files.** Switch the repository branch selector to your new branch. Navigate to `Publications/mock-photoz-sbi-exercise-2026/`, click **Add file → Upload files**, and upload both `manuscript_v1.pdf` and `manuscript_v1.md`. Commit changes to **the current publication branch**, not `main`.
5. **Open one Draft Pull Request.** On **Pull requests → New pull request** (or the banner **Compare & pull request**), choose base `main` and compare your publication branch. Title: `[MOCK SUBMISSION] Photo-z uncertainty calibration with SBI`. Use **Create draft pull request** and complete the PR template as far as you can. If the PR opens as Ready by mistake, select **Convert to draft** if permitted or ask the organizer.
6. **Confirm the contents.** In the PR's **Files changed** tab, verify that exactly the mock `summary.md`, `manuscript_v1.pdf`, and `manuscript_v1.md` have been added. Send the PR URL to the organizer and mention any unclear or failed steps.

**Please leave the PR in Draft status.** Do not select the reviewers or begin the review yourself. The Paper Handler will check the submission, assign reviewers and open First Review.

## During review — respond and revise

- When the Handler tells you the review is open, read reviewers' line comments under **Files changed** and their general comments under **Conversation**.
- Reply in **each existing review thread**, explaining whether and how the manuscript can address the scientific point. Avoid inventing missing numerical results or unsupported evidence.
- Add a revised `manuscript_v2.md` in the **same publication folder and same branch**. Update `summary.md` to log what changed and which review comments remain unresolved. A PDF v2 is optional for this short exercise, but the actual policy for a real review may require a versioned PDF.
- Ask reviewers to confirm whether their concerns are addressed, and notify the Handler when your responses and revision are ready. The Handler and Chair, not the author, make the review recommendation and decision.

## How we will assess the instructions

Please follow this written guide independently as far as possible. If something is unclear, note **which step**, **what you expected** and **what GitHub showed**; it is useful evidence for improving the process. There is no need to solve technical ambiguities silently.

The fictional paper is intentionally incomplete for scientific-review training. Do not submit it to any journal or arXiv.
