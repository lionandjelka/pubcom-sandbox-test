# How to review the submitted paper in GitHub

**Review both manuscript formats:** read `manuscript_v1.pdf` for the paper-like submission, and use **Files changed → `manuscript_v1.md`** for comments anchored to exact manuscript text. `summary.md` is for intake metadata, not a replacement for peer review.

## Suggested format for an actionable comment

- **`Request:`** A scientific, data-rights, or procedural deficiency that needs resolution. Include *location, concern, reason and a feasible remedy*. Example: `Request: §3 describes held-out rows as unseen galaxies, but five realizations can belong to the same source. Please use an ID-disjoint split or remove the generalization claim, and state which verification remains outstanding.`
- **`Suggestion:`** Optional presentation or reporting improvement. Example: `Suggestion: §4 should explain how the PIT comparison with the MDN will be shown, ideally with a figure caption and uncertainty information.`
- **`Question:`** Clarification needed before judging whether there is a serious problem. Example: `Question: Is the faint sample counted in unique galaxies or noisy realizations?`

**Submit the review:** hover line → click **+** → **Start a review** → add comments → top-right **Review changes** → **Comment** → **Submit review**. If a section is not in the GitHub diff (for example later revisions), comment under **Conversation** with explicit manuscript version and section. If you also use `Approve` or `Request changes`, explain why in the review text; this exercise does not depend on them.

## Revision comparison

The volunteer should preserve `manuscript_v1.md` and add `manuscript_v2.md` to the **same PR**, recording in the summary what changed. Each reviewer should return to the **original thread**, assess v2 and say whether the concern was met. A completed response may be `not resolved — requires new quantitative experiment`; GitHub workflow closure does not require a scientifically accepted paper.

## Attributing reviewer work

Relevant comments, co-authorship requests, author-list changes, collaboration names and required acknowledgements must follow **current ISSC policy and ordinary authorship standards**. A review comment or reaction does not automatically earn co-authorship. Do not treat 👍 voting as scientific adjudication.

## Security and authority

This is a **public sandbox**. Comments are publicly visible. Do not use real proprietary data or circulate unpublished results via public PRs. The approved ISSC manual and data-rights rules supersede any exercise convention.
