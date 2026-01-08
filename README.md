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

This project is designed to explore that distinction in a clean, quantitative way using information theory.

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
