# ISSC PubCom documentation upgrade — installation and change summary

**Package date:** 16 November 2026  
**Target repository:** <https://github.com/lionandjelka/pubcom-sandbox-test>  
**Basis:** current `main` documentation and the 11 November PubCom meeting discussion.  
**Status:** complete replacement documents prepared; **not yet uploaded to live GitHub**.

## Complete files supplied

- `README.md` — fully updated repository entrypoint with notification and format decision guidance.
- `AUTHOR_HANDOFF.md` — complete author instructions; no longer implies the Handler must release each separate author reply; links to conversion guide.
- `REVIEW_PROTOCOL.md` — full batched-review instructions and an explicitly *experimental* PDF-report alternative.
- `ROLE_INSTRUCTIONS.md` — updated Author, Handler, Reviewer 1, Reviewer 2, Chair and Observer cards with permissions and responsibilities.
- `CONVERT_TO_MARKDOWN.md` — new end-to-end LaTeX/PDF conversion guide with Pandoc, PyMuPDF4LLM, quality-control checks and safe uploading.

All five are **complete Markdown files**, not fragments to append to existing documents. Paths and cross-links are intended for the repository root. **Do not replace the old files blindly on `main`.**

## Installation without modifying existing submissions

1. Open the repository and create a new branch, e.g. `docs/pubcom-review-guidance-2026-11` **from `main`**.
2. Switch to that documentation branch and choose **Add file → Upload files**; upload the five new/replacement files **at repository root** (not under `Publications/`).
3. For files that already exist (`README.md`, `AUTHOR_HANDOFF.md`, `REVIEW_PROTOCOL.md`, `ROLE_INSTRUCTIONS.md`), GitHub's file-upload interface may not always overwrite in place. If it does not allow replacement, click the existing file → **Edit this file** (pencil) → replace its entire contents with the corresponding complete Markdown text → **Commit changes to the docs branch**.
4. Add the **new** `CONVERT_TO_MARKDOWN.md` to the root.
5. Open a **documentation-only Pull Request** from `docs/pubcom-review-guidance-2026-11` to `main`.
6. Verify the diff: only those five Markdown documents should be changed. Confirm links, formatting and all role guidance render as expected.
7. Invite PubCom to review the documentation PR, merge only after agreeing on the text. **Do not close, merge, edit, or rebase any active manuscript-review PR.**

## Specifically addressed from the meeting

**Item 2 — Notifications and comments:** `Start a review` saves pending comments; `Add review comment` collects more; a final `Submit review` releases the batch. State that batching may *reduce*, but not promise to eliminate, separate email notifications.

**Item 3 — Scientific manuscript formats:** provide clear source `.tex` → Pandoc `.md` and PDF → extracted `.md` methods, including limits for equations/figures/citations and a comparison checklist. PDF-only plus numbered consolidated referee report remains an **option under testing**, not an approved general submission policy.

**Related clarification — Author/Handler interaction:** authors can respond directly after a review is submitted; Handler monitors and records the outcome, rather than approving each chat exchange.

**Related clarification — Permission safeguards:** documentation describes the limitations; configuring and enforcing the actual rights to close/merge PRs, set branch protection, and store confidential files needs administrator decisions and appropriate hosting.

## Out of scope / untouched

- Existing mock paper PRs and branches, labels, GitHub Actions, branch protection and collaborator permissions.
- The approved ISSC Publication Policy, classifications, or formal review time windows.
- The older `DEMO_WALKTHROUGH.md` (a historical worked example; it is not the normative review policy).
- The `ASYNC_EXERCISE_GUIDE.md` timetable and `.github/pull_request_template.md` checklist, which remain compatible with this training-mode documentation.

## Suggested documentation PR description

```markdown
# ISSC PubCom — clearer reviewer notifications and manuscript conversion

Documentation-only update following the 11 November 2026 mock-review feedback.

- Clarify **Start a review → Add review comment → Submit review**.
- Clarify continuous author–reviewer discussion and Handler monitoring.
- Add LaTeX/PDF → Markdown guidance for the present pilot.
- Keep PDF-only consolidated reports **under evaluation**, not mandatory.
- Describe permissions and official deployment as open technical/governance questions.

No manuscript reviews, security settings, or approved publication policies changed.
```
