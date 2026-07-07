# Calibrating Photometric Redshift Uncertainties for LSST withSBI

<!-- EXAMPLE cover page — accompanies DEMO_WALKTHROUGH.md. Fictional. -->

## Classification

- **Category:** [x] 1 · Mandatory  (came out of the ISSC Photo-z Interest Group hackathon → ISSC is an author)
- **Class:** [x] a · Paper
- **Timeline stream:** [x] ii · Standard — 2-week First Review, ≥1 week follow-up

## People

- **Author contact(s):** @rivera-astro (ISSC member), @okonkwo-ml
- **Full author list:** R. Rivera, N. Okonkwo, P. Sundaram
- **Host Interest Group:** Photometric Redshifts IG
- **Requested expert reviewers:** @lindqvist-photoz
- **Contributors:**
  - R. Rivera — ISSC — method design, writing
  - N. Okonkwo — ISSC — software, experiments
  - P. Sundaram — DESC — simulation inputs, review of results

## Publication

- **Where the publication can be found:** https://www.overleaf.com/read/EXAMPLE-photoz-sbi (PDF v1 attached in PR)
- **Intended publication venue:** ApJ
- **Slack channel:** #issc-photoz

## Review timeline

- **First Review deadline:** 2025-05-19 (2 weeks)
- **Follow-up Review deadline:** 2025-05-28

## Data rights

- **Does this work use proprietary/real Rubin data?** no (DC2 simulations only)
- **Who holds data rights:** n/a
- **SC Federation liaison / ICA note:** n/a — simulated data, standard ICA sufficient

## Abstract

We calibrate photometric-redshift posterior uncertainties for LSST using simulation-based
inference (SBI) trained on DC2, and show that SBI-derived credible intervals are better
calibrated than those from a baseline mixture-density network across the full magnitude range,
with the largest gains for faint, high-redshift galaxies.

## Resources used

DC2 simulations; the ISSC Photo-z IG hackathon (Feb 2025) where the method was prototyped;
`sbi` and `jax`. The hackathon origin places this in Category 1.

## Detailed description — section outline

1. Introduction & motivation
2. Data: DC2 photometry and spectroscopic truth
3. Method: SBI for redshift posteriors
4. Baseline: mixture-density network
5. Calibration metrics (PIT, coverage)
6. Results
7. Discussion & limitations
8. Conclusions
