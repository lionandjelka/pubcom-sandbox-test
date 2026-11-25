# MOCK MANUSCRIPT — FICTIONAL, NOT FOR SUBMISSION
## Calibrating Photometric Redshift Uncertainties for LSST with Simulation-Based Inference

**Exercise manuscript v2 — 25 November 2026.** This fictional study uses entirely synthetic LSST-like photometry.

### Abstract
We compare simulation-based inference (SBI) with a mixture density network (MDN) for estimating photometric-redshift uncertainties. We split the synthetic photometry by noise realization, allowing measurements of the same simulated galaxy to enter both training and testing. The comparison therefore describes performance on held-out realizations. The illustrative probability-integral-transform (PIT) histogram motivates a direct test of interval coverage. Empirical coverage at 68% and 95%, performance on unseen galaxies, and any advantage at the faint end remain unmeasured.

### 1. Introduction
Photometric redshift posterior distributions must support well-calibrated statistical inference. Simulated photometry provides a testbed to study calibration, selection effects and posterior predictive performance.

### 2. Data
The fictional sample comprises 40,000 simulated galaxies with five independent noise realizations per galaxy, for a total of 200,000 photometry rows. We randomly assigned 80% of the rows to training and 20% to testing. Because the split was made by row, different realizations of the same galaxy can occur in both sets. Those realizations share the underlying source photometry and true redshift even though their noise differs. The faint subsample is defined by simulated $i$-band magnitude $i>24$. Its unique-galaxy count and selection function are unspecified.

### 3. SBI and baseline
We compare an SBI posterior estimator conditioned on the noisy fluxes with an MDN fitted to the same training rows. For either model, a held-out realization may come from a galaxy represented during training. This overlap could make test performance appear better than it would be on entirely new galaxies. Its effect on the relative performance of the two estimators is unknown.

### 4. Calibration assessment
The illustrative PIT histogram in Figure 1 appears approximately flat for SBI. To test interval coverage directly, we would first split the sample by galaxy ID, keeping all five realizations of a galaxy together, then refit both estimators. For each model and each nominal level (68% and 95%), we would construct a central posterior interval from the predicted redshift distribution and measure how often it contains the simulated true redshift.

For each held-out galaxy, we would average the coverage indicators across its five realizations, then average those fractions over galaxies. We would compare each empirical fraction with its nominal level and report the difference in percentage points. Resampling whole galaxies would provide an uncertainty estimate that accounts for repeated realizations. We would repeat the comparison for the $i>24$ selection, using the qualifying realizations of each galaxy and reporting the number of distinct galaxies represented.

### 5. Results
The placeholder histogram provides a qualitative comparison of the two estimators. The exercise supplies no measured coverage fractions or uncertainties for either model. It therefore leaves open whether the 68% and 95% intervals attain their nominal coverage in the full or faint sample.

### 6. Discussion
A pooled PIT histogram can conceal a dependence on magnitude. Comparing the two estimators on the same held-out galaxies, both overall and at the faint end, would distinguish a difference in interval coverage from an impression based on the pooled histogram. Interpreting the faint-end comparison would also require the selection function and the number of galaxies contributing to it.

### 7. Conclusions
The row-level split tests predictions for additional noise realizations and leaves generalization to new galaxies undetermined. A galaxy-disjoint evaluation with empirical coverage and uncertainties at both nominal levels is needed to establish how well either estimator calibrates photometric-redshift uncertainties.
