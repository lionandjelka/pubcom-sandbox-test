# Calibrating Photometric Redshift Uncertainties for LSST with Simulation-Based Inference

## Identification and manuscript versions
- **Submission type:** MOCK / TRAINING — fictional results.
- **Title:** Calibrating Photometric Redshift Uncertainties for LSST with Simulation-Based Inference
- **Corresponding/primary author(s) and contact handle(s):** Bryce T. Bolin (mock Author), GitHub @brycebolin.
- **Paper Handler:** Pending assignment by the PubCom Chair.
- **Summary revision/date:** v2 / 2026-11-25
- **Manuscript PDF revision/date and link:** [v1 / 2026-10-20 (PDF)](manuscript_v1.pdf) · [v2 / 2026-11-25 (PDF)](manuscript_v2.pdf)
- **Line-commentable manuscript revision/date and link:** [v2 / 2026-11-25 (Markdown)](manuscript_v2.md)
- **Target journal or release venue and intended timeline:** ISSC PubCom sandbox, round 2. No external journal submission or release is planned.

## Provisional classification (Paper Handler to confirm)
- **Category (select one):** 
- **Category rationale and any ISSC resources or activity:** The simulated LSST-like photometry is used solely for the ISSC review pilot. The manuscript identifies no ISSC observational or computing resources.
- **Class (select one):** [x] a Paper (provisional)
- **Timeline (select one):** Pending Handler confirmation.
- **Current approved manual reference / check:** pending Handler confirmation

## Authors, collaborators and reviewers
- **Full author list and affiliations:** Bryce T. Bolin (Eureka Scientific), mock submitting Author. The supplied manuscript has no author byline.
- **Contributor statements** (name — collaboration — contribution): Bryce T. Bolin — ISSC PubCom pilot — prepared the summary and serves as mock Author.
- **Host ISSC Interest Group / other collaboration (if any):** ISSC PubCom review pilot. No scientific host group is identified in v1.
- **Suggested subject expertise/reviewers (optional; Handler invites):** Photometric redshifts and posterior calibration. Reviewer assignments pending.
- **Known reviewer conflicts/other disclosure (if any):** No reviewers proposed.

## Data, resources and rights
- **Data and software resources used:** Entirely synthetic LSST-like photometry for 40,000 fictional galaxies with five noise realizations each. The manuscript describes an SBI estimator and a mixture density network baseline. It supplies no software or catalog.
- **Real Rubin observational data?** No.
- **Proprietary or restricted data?** No.
- **Data-rights and release basis:** Organizer-supplied fictional manuscript for the public training sandbox. No observational data are being released.
- **Cross-collaboration liaison / ICA needs, if applicable:** None identified for this exercise.
- **Attribution or acknowledgment issue to check:** No additional attribution is specified in v1.

## Abstract

We compare simulation-based inference (SBI) with a mixture density network (MDN) for estimating photometric-redshift uncertainties. We split the synthetic photometry by noise realization, allowing measurements of the same simulated galaxy to enter both training and testing. The comparison therefore describes performance on held-out realizations. The illustrative probability-integral-transform (PIT) histogram motivates a direct test of interval coverage. Empirical coverage at 68% and 95%, performance on unseen galaxies, and any advantage at the faint end remain unmeasured.

## Detailed section outline (must match the submitted manuscript)

1. Introduction
2. Data
3. SBI and baseline
4. Calibration assessment
5. Results
6. Discussion
7. Conclusions

## Review dates (Paper Handler completes)
- **First Review opened:** Pending.
- **First Review deadline:** Pending.
- **Follow-up opened/deadline, if any:** Pending.
- **Reviewers formally requested:** Pending.

## Revision history

| Version / date | Files or stable manuscript URL | Main changes and linked comments |
|---|---|---|
| v1 / 2026-11-24 | [PDF](manuscript_v1.pdf) · [Markdown](manuscript_v1.md) | Round 2 submission of the 2026-10-20 exercise manuscript. |
| v2 / 2026-11-25 | [Revised PDF](manuscript_v2.pdf) · [Revised Markdown](manuscript_v2.md) | Clarified the [row-level split and its effect on generalization](https://github.com/lionandjelka/pubcom-sandbox-test/pull/16#discussion_r4692082351). Added a [proposed 68% and 95% coverage test](https://github.com/lionandjelka/pubcom-sandbox-test/pull/16#discussion_r4692087175) and withdrew the unsupported calibration and faint-end performance claims. |

## Final disposition (Handler + Chair complete, not the author at submission)
- **Handler recommendation/date and PR comment link:**Exercise-only procedural completion / 2026-11-25 / [Handler recommendation](https://github.com/lionandjelka/pubcom-sandbox-test/pull/16#issuecomment-7164529941)
- **Chair decision/date and PR comment link:** Exercise-only procedural completion / 2026-11-25 / [Chair decision](https://github.com/lionandjelka/pubcom-sandbox-test/pull/16#issuecomment-7164566139)
- **Outstanding scientific/procedural conditions:** No empirical 68%/95% coverage or galaxy-disjoint validation; combined Handler/Reviewer role and compressed timeline.
- **Confirmed attribution and data-rights disposition:** Entirely fictional training data; no real publication clearance or attribution decision.
- **Final version/link, if cleared:** manuscript_v2.pdf and manuscript_v2.md — final mock versions only; not cleared for real publication.
- **Training or real-publication status:** MOCK / TRAINING — NO PUBLICATION CLEARANCE.
