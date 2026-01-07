# Information-Theoretic Analysis of Photon-Limited Optical Interferometric Measurements

**Author:** Hitesh Kumar Singh   
**Domain:** Photonics • Astrophysics • Statistical Inference  

---

## Overview

This repository contains a complete, self-contained computational research project that studies the **fundamental statistical limits of optical interferometric measurements in photon-limited regimes**.

The project develops an **information-theoretic inference framework** for an idealized optical interferometer observing a binary star system. It combines physical modeling, statistical estimation theory, numerical simulation, and careful interpretation to answer a simple but deep question:

> *How accurately can astrophysical parameters be estimated from interferometric measurements when photon noise dominates?*

The emphasis of this work is on **reasoning, methodology, and understanding limits**, rather than on proposing new instruments or reporting observational data.

---

## Motivation: Where did this idea come from?

During my astrophysics internship, I was exposed to a broad range of topics including observational astronomy, detection techniques, interferometry, data analysis, and research methodology.

In most discussions of optical interferometry, performance is described primarily in terms of **angular resolution**, which improves with increasing baseline length. However, these discussions often do not explicitly address the role of **photon statistics** in limiting measurement precision.

This led to a natural question:

> *Even if an interferometer has very high angular resolution, how precisely can we actually estimate parameters when the number of detected photons is limited?*

In other words:
- Resolution describes what can be distinguished geometrically
- Precision describes what can be inferred statistically

This project was designed to explore that distinction in a clean, quantitative way using information theory.

---

## Scientific Problem Statement

The central problem studied in this project is:

> **What are the fundamental statistical limits on parameter estimation in photon-limited optical interferometry?**

To make the problem concrete and tractable, the following simplified scenario is considered:

- A **two-aperture optical interferometer**
- Observing an **unresolved binary star**
- Characterized by:
  - Angular separation
  - Flux (brightness) ratio
- Detection via **photon-counting detectors**
- Noise dominated by **Poisson photon statistics**

The goal is **parameter estimation**, not detection:
to quantify how accurately the parameters of the binary system can be inferred from noisy photon counts.

---

## Modeling Approach

### 1. Physical Forward Model

The project begins by constructing a **first-principles forward model** that connects astrophysical parameters to measurable quantities.

Key elements:
- Interferometric phase depends on baseline, wavelength, and angular separation
- The expected photon count at the interferometer output depends on:
  - Interferometric phase
  - Flux ratio
  - Total photon normalization

This step ensures that all subsequent statistical analysis is grounded in physically meaningful quantities.

---

### 2. Noise and Statistical Model

Photon detection is inherently random, especially at low light levels.

In this project:
- Photon counts are modeled using **Poisson statistics**
- A likelihood function is derived for observing a given number of photons
- This likelihood forms the basis for parameter estimation

---

### 3. Information-Theoretic Framework

To quantify fundamental limits on precision, the project uses:

- **Fisher Information Matrix**
- **Cramér–Rao Lower Bound (CRB)**

The Fisher Information measures how sensitive the likelihood is to changes in parameters.  
The CRB provides a lower bound on the variance of any unbiased estimator.

This framework answers the question:
> *What is the best possible precision achievable by any estimator, in principle?*

---

### 4. Parameterization and Identifiability

Rather than working directly with angular separation, the analysis uses the **interferometric phase**, which is the actual observable of the instrument.

This dimensionless parameterization:
- Improves numerical stability
- Clarifies which parameters are identifiable
- Reveals regimes where information vanishes

At certain operating points (fringe extrema), the interferometer becomes insensitive to phase changes, leading to a true loss of identifiability.

---

### 5. Numerical Validation via Monte Carlo Simulation

Theoretical bounds are validated using **Monte Carlo simulations**:

- Synthetic photon counts are generated from the forward model
- Parameters are estimated using a maximum-likelihood approach
- The empirical variance of the estimator is compared to the CRB

This step verifies that:
- Theoretical limits are achievable under appropriate conditions
- Deviations occur when assumptions (such as unbiasedness) break down

---

### 6. Global Likelihood Structure and Estimator Bias

Fisher Information describes only the **local** behavior of the likelihood.

To understand the full inference problem, the project also examines:
- The likelihood over the entire parameter domain
- Periodicity and multimodality of interferometric phase
- Estimator bias as a function of true parameter value

This analysis demonstrates important limitations of Fisher-based bounds and highlights the role of global ambiguity in interferometric measurements.

---

## Key Observations and Results

The main insights obtained from this project are:

- High angular resolution does not automatically imply high statistical precision
- Fisher Information can vanish at certain operating points
- Cramér–Rao bounds are meaningful only in locally identifiable, unbiased regimes
- Information content depends non-trivially on interferometer baseline
- Flux ratio strongly affects inferential precision
- Global likelihood structure introduces phase ambiguity and estimator bias

These results clarify when information-theoretic limits are useful and when they must be interpreted with caution.

---
