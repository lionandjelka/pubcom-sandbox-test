# How to review a submitted paper in GitHub — ISSC PubCom pilot

**For this mock exercise:** read `manuscript_v1.pdf` as the formatted scientific paper, and use **Pull Request → Files changed → `manuscript_v1.md`** for comments anchored to exact passages. `summary.md` is intake metadata; commenting on it does not substitute for scientific review.

> The sandbox is **public** and uses fictional data only. The PubCom review is **internal scientific consultation**, not journal peer review. The approved ISSC publication manual and data-rights rules supersede this training protocol.

## 1. Types of feedback

- **`Request:`** A material scientific, statistical, data-rights, or procedural issue that calls for a substantive answer. Include **location, issue, why it matters and the evidence or change needed**. Example: `Request: §3 treats held-out photometric rows as unseen galaxies, but realizations of the same galaxy may be in both partitions. Please use a galaxy-disjoint split or withdraw the generalization claim.`
- **`Suggestion:`** Helpful but **non-blocking** presentation or reporting improvement. Example: `Suggestion: §4 could show PIT results and baseline comparison with consistent axes and readable uncertainty indicators.`
- **`Question:`** Clarification needed before the reviewer can judge whether the issue is blocking. Example: `Question: Are faint-sample counts unique galaxies or simulated noise realizations?`

Do not assign scientific priority simply from GitHub 👍 reactions. Discuss material issues on their merits.

## 2. Preferred method — submit all line comments in one review

**Why:** During the 11 November 2026 mock review, the author received separate email notifications for independently published comments. GitHub allows the reviewer to collect comments as **pending** and submit them together.

1. Open the requested **Pull Request** and read the PDF and summary.
2. Select **Files changed** and find `manuscript_v1.md`.
3. Hover the first relevant changed line, click the blue **+** icon and type `Request:`, `Suggestion:` or `Question:` with a precise explanation.
4. Click **Start a review**, **not** **Add single comment**. The comment is saved as **pending**, initially visible only to the reviewing user.
5. Continue reading. For each new issue, click **+** and **Add review comment**; do not submit yet.
6. When finished, click **Review changes** or **Submit review** at the top/right of the diff (UI wording can vary).
7. Add a short overall summary and select **Comment** as the *GitHub review outcome* for this pilot.
8. Click **Submit review**. Now the author and Handler can view the complete set of comments.
9. Post a short `REVIEW 1 COMPLETE — manuscript v1 — [date]` note in the review summary if useful; a separate Handler handoff comment can carry deadlines.

**Notification caveat:** Submitting one batched review reduces multiple immediate emails, but recipients may still see notifications depending on GitHub configuration, subscriptions, mentions and later thread replies. Do not promise exactly one email.

**Important distinction:** `Request:` is **text in a scientific comment**. GitHub's **Request changes** button is a *platform review state*, which may have merge consequences depending on repository rules. Use GitHub **Comment** for the pilot unless the coordinator explicitly tests merge protection. Similarly, GitHub **Approve** is not the Chair's scientific decision.

## 3. Alternative method under evaluation — one consolidated PDF referee report

Some reviewers prefer a single document, especially for long LaTeX manuscripts. **This option is being tested and has not replaced the current PDF + Markdown pilot format.**

Suggested steps:

1. Read the formatted `manuscript_v1.pdf`.
2. Prepare a review document with numbered items (`R1.1`, `R1.2`), each identifying a section/page, concern and requested action.
3. Export as `Reviewer1_Report_v1.pdf`.
4. Open the PR **Conversation** tab and attach the PDF to a comment using GitHub's file-attachment facility, where enabled. Verify the uploaded link opens before submitting the comment.
5. Post a short summary such as `Reviewer 1 complete; detailed numbered requests R1.1–R1.n attached.`
6. The author posts a point-by-point response (`Response_to_Reviewer1_v1.pdf` or a numbered PR comment), identifying corresponding manuscript changes.
7. The Handler tracks every numbered issue until addressed, deferred with reasons, or outstanding.

A PDF attachment in PR Conversation does **not** produce per-line GitHub review threads or independently resolvable review items. For technical privacy, do not upload sensitive reports to this public sandbox. A future official workflow requires a properly permissioned repository.

## 4. Author responses and continuous discussion

After a review is submitted, authors and reviewers **may communicate directly in the original thread**. They do **not** need the Handler's permission for every exchange. The Handler monitors the deadline, sends reminders on inactivity, can seek clarification or additional review, and documents final dispositions.

- Author reply: `We changed §3 in v2 to ...` or `Not changed because ...; required evidence remains ...`.
- Author revision: commit `manuscript_v2.md` (and normally corresponding `manuscript_v2.pdf`) to the **same branch / PR** and update `summary.md` revision history.
- Reviewer follow-up: `Addressed`, `Partially addressed`, or `Outstanding; requires [specified test]`.
- Handler summary: `Request | author action | reviewer confirmation | outstanding condition`.

If comments cannot attach to a file absent from the current diff, use PR **Conversation** with **explicit version/section/page identifiers** and a link to the relevant manuscript version. Review is not complete merely because replies exist.

## 5. Thread resolution and recorded decisions

- Only mark a scientific discussion **resolved** when its substance has been addressed or the Handler has explicitly documented a reasoned disposition under the policy. The ability to click **Resolve conversation** depends on GitHub permissions, typically the PR author or users with write access.
- The Handler posts a **written recommendation** summarizing addressed, disputed, unanswered and outstanding requests.
- The Chair posts a **separate dated decision** for the mock workflow. A successful training cycle may finish with `return for further scientific work`.
- GitHub **merge** or **close** is a repository operation, not equivalent to publication clearance. Thread resolution may block merging only if enforced by branch protection or rulesets; check the actual repository configuration.

## 6. Authorship, confidentiality and permissions

- Review comments and PR reactions do **not automatically** confer co-authorship or builder status. Apply the currently approved collaboration and publisher policies.
- A public repository exposes the manuscript, comments and attachments. Use fictional content only. Do not submit real unpublished analyses or proprietary Rubin data here.
- Reviewers can generally comment with read access; requesting reviewers, labeling, committing, resolving, closing and merging have different authorization requirements. Consult the repository owner / admins rather than assuming the desired restrictions already operate.
- The committee is exploring hosting within an official LSST organization with appropriate access and closure/merge controls. Such deployment is **not yet approved**.

## 7. Reviewer quick checklist

- [ ] I read the PDF and understood the claims.
- [ ] I commented on the **scientific manuscript**, not only the metadata summary.
- [ ] I clearly separated `Request:`, `Suggestion:` and `Question:`.
- [ ] I collected inline comments using **Start a review**, then submitted them together.
- [ ] My submitted review has a short overall summary.
- [ ] I checked the author's updated version and replied in the original discussion.
- [ ] I informed the Handler which concerns remain scientifically outstanding.

**Further reading:** [Author handoff](AUTHOR_HANDOFF.md) · [Role cards](ROLE_INSTRUCTIONS.md) · [Conversion guide](CONVERT_TO_MARKDOWN.md) · [GitHub review quickstart](https://docs.github.com/en/pull-requests/get-started/reviewing-pull-requests-quickstart)
