# ISSC Publication Portal

Repository for **ISSC publications in internal review**. This portal implements the
[LSST–ISSC Publication Review Manual, v1.0](https://github.com/LSSTISSC/PubCom-sandbox) (April 2, 2025).

> **The review is run inside a Pull Request (PR).** GitHub Issues are used only as an optional public
> record of the registration step. If the README and the Manual ever disagree, the Manual wins.

See the [open review PRs](https://github.com/LSSTISSC/PubCom-sandbox/pulls) for publications currently under review.

---

## The process at a glance

```mermaid
flowchart TD
    A["Register with PubCom<br/>(email or Slack):<br/>title, authors, abstract,<br/>preliminary category + class"] --> B["PubCom Chair assigns<br/>a Paper Handler"]
    B --> C["Paper Handler confirms remit,<br/>sets Category / Class / Timeline"]
    C --> D["Author: new branch +<br/>completed cover page +<br/>DRAFT Pull Request"]
    D --> E["Paper Handler:<br/>Draft to Ready, add reviewers,<br/>email the ISSC, apply labels"]
    E --> F["First Review<br/>(reviewers comment:<br/>suggestion / Request: + upvotes)"]
    F --> G["Authors respond to all comments,<br/>offer co-authorship, upload revision"]
    G --> H{"Any Request:<br/>still unresolved?"}
    H -->|Yes| I["Follow-up Review<br/>(repeat, up to once more<br/>for new Requests)"]
    I --> H
    H -->|No| J["Paper Handler releases +<br/>recommends to PubCom Chair"]
    J --> K["Chair records final decision"]
    K --> L["Add ISSC to author list<br/>(Mandatory / Encouraged) or<br/>acknowledgement (Optional);<br/>post final version; merge"]
```

A fully worked example is in **[DEMO_WALKTHROUGH.md](DEMO_WALKTHROUGH.md)**.

---

## Who does what (in one line each)

- **Author** — makes **one branch per publication** and adds the cover page to it, **once**. Then responds to comments.
- **Reviewer** (any ISSC member) — **never** makes a branch or commits anything; comments entirely in the browser.
- **Paper Handler** (PubCom) — opens/closes the review, applies labels, runs follow-ups, releases to the Chair.

## For authors

### 1 · Register (email or Slack)
Message PubCom with **title, author(s), abstract**, and your **preliminary category and class**.
If you want specific expert reviewers invited, name them now. The Chair assigns a **Paper Handler**,
who confirms the publication is in ISSC remit and sets the final **category, class and timeline**.
_(Optional: open a [registration issue](../../issues/new?template=register-publication.md) for a public record — it is not the review itself.)_

### 2 · Open the review Pull Request
A pull request always needs one committed file — that file is your cover page. Two ways to add it:

**✅ Recommended — in the browser, no command line:**
1. **Add file → Create new file** on the repo.
2. Name it `Publications/<your-title>.md`, paste your completed cover page (copy [`Publications/summary_doc_template.md`](Publications/summary_doc_template.md) and fill in every field, including the **enumerated section outline**).
3. At the bottom pick **Commit to a new branch**, then **Propose new file → Create pull request**. Branch, commit, and PR are created in one step.

**Alternative — command line:** branch off `main`, add `Publications/<your-title>.md`, commit, push, open the PR.

Either way: open it as a **Draft**, set **Assignees** = all authors (add the Paper Handler once known), assign **no reviewers** (the Paper Handler does that), and paste the cover-page text into the description too. The template's checklist loads automatically.

### 3 · Respond to feedback
Reply to each comment in its thread, tagging the reviewer. Address **every** comment (a `Request:` may be answered with a justification instead of a change). **Offer co-authorship** to any reviewer whose feedback significantly improved the publication. When done, upload the revised version at the stated link and tell the Paper Handler.

---

## For reviewers (any ISSC member) — everything in the browser

You do **not** clone the repo, make a branch, or commit. Just:

1. Open the review PR and read the cover page under **Files changed**.
2. Comment either as a **line comment** — hover a line, click the blue **+**, then **Start a review** — or under **Conversation** for general notes.
3. **Mark required feedback** by prefixing the comment with **`Request:`** (validity-critical). Everything else is a **suggestion**.
4. **Upvote with 👍** — more-upvoted comments are higher priority.
5. If you raised a `Request:`, engage with the authors' reply and **resolve your own comment** once satisfied.

> *You are reviewing readiness for publication as an ISSC product — teams produce better work than individuals. But the premise of the publication has already been developed by the authors and does not itself merit criticism.*

---

## For the Paper Handler (PubCom)

Work the checklist that ships in the PR template. In short:

- **Open:** check procedural compliance, confirm/adjust category-class-timeline, apply labels, convert Draft → Ready, add requested reviewers, and email the ISSC (PR link + abstract + publication link).
- **Close First Review:** remind reviewers to re-review; the original commenter resolves their own comment; you adjudicate anything unresolved. An un-adopted `Request:` is either re-classified to a suggestion (with the authors' justification) or the change is required.
- **Follow-up:** repeat as needed — once more at most, for newly raised Requests you agree are needed — keeping the original timeline stream.
- **Conclude:** **release** and recommend to the **Chair**, who records the **final decision**. Confirm the final version carries the ISSC author-line (Mandatory/Encouraged) or acknowledgement (Optional), post it, set `status: concluded`, and merge.

Labels live in [`.github/labels.yml`](.github/labels.yml) (category · class · timeline · status) and can be auto-synced to the repo.

---

## Timeline streams

| Stream | First Review | Follow-up | Typical use |
|--------|--------------|-----------|-------------|
| **i · Accelerated** | 1 week | ≥ 3 days per stage | Conference proceedings, short notes |
| **ii · Standard** | 2 weeks | ≥ 1 week | Most peer-reviewed papers |
| **iii · Extended** | 3 weeks | ≥ 1 week | Dissertations, long works |

## Repository layout

| Path | Purpose |
|------|---------|
| `Publications/summary_doc_template.md` | The cover page authors copy and complete |
| `.github/pull_request_template.md` | Auto-loading review checklist + who-does-what (used for every PR) |
| `.github/ISSUE_TEMPLATE/register-publication.md` | Optional pre-PR registration record |
| `.github/labels.yml` | Category / class / timeline / status labels |
| `DEMO_WALKTHROUGH.md` | End-to-end worked example of one publication |
