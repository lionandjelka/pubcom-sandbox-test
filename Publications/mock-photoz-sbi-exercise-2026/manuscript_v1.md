# MOCK MANUSCRIPT — FICTIONAL, NOT FOR SUBMISSION
## Calibrating Photometric Redshift Uncertainties for LSST with Simulation-Based Inference

**Exercise manuscript v1 — 20 October 2026**. Entirely invented training case; methods, figures and claims are not real DC2 measurements.

### Abstract
We explore simulation-based inference (SBI) for photometric-redshift uncertainty calibration using synthetic LSST-like galaxy photometry, comparing it with a mixture density network baseline. A visually nearly uniform probability-integral-transform (PIT) histogram motivates the claim that SBI gives calibrated 68% and 95% credible intervals, including faint galaxies. We conclude that the approach generalizes reliably to previously unseen sources.

### 1. Introduction
Photometric redshift posterior distributions must support well-calibrated statistical inference. Simulated photometry provides a testbed to study calibration, selection effects and posterior predictive performance.

### 2. Data
A **fictional** training table contains 40,000 simulated galaxies, each with five independent noisy photometric realizations: 200,000 photometry rows. We split the **rows at random** into 80% training and 20% testing without grouping by original galaxy ID. The faint subsample has simulated i-band magnitude >24; its unique-galaxy count and selection function are not reported. These data are synthetic, not proprietary Rubin observations.

### 3. SBI and baseline
We fit a conditional SBI posterior estimator to the noisy flux vector and compare it with an MDN trained on the same row split. Distinct realizations of **the same galaxy can appear both in training and testing**. Nevertheless, we describe test rows as "previously unseen galaxies".

### 4. Calibration assessment
Figure 1 is a placeholder PIT histogram. Its bars appear fairly flat for SBI compared with the MDN; no PIT uncertainty, quantitative coverage statistic or sample-size information is reported. We have not computed empirical coverage at 68% or 95% on a galaxy-disjoint test set.

### 5. Results
We claim that SBI's 68% and 95% credible intervals are "well calibrated" and that performance gains are largest at the faint end. No observed coverage fractions, confidence intervals, residuals, or magnitude-bin counts are reported. The effect of row-level train/test leakage has not been evaluated.

### 6. Discussion
PIT uniformity alone is not a sufficient numerical demonstration of coverage. Robust statements would need unique-galaxy-disjoint test partitions, empirical interval coverage, meaningful uncertainty estimates, and selection-function reporting.

### 7. Conclusions
These simulated experiments motivate follow-up testing, but any claim about reliable generalization to unseen galaxies requires new analysis.
