# Proactive Traffic Safety Assessment for Highway Alignment Planning Without Crash Data

<div align="left">
  <a href="INSERT_YOUR_COLAB_LINK_HERE">
    <img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab">
  </a>
  <a href="https://doi.org/10.5281/zenodo.INSERT_DOI_HERE">
    <img src="https://zenodo.org/badge/DOI/10.5281/zenodo.INSERT_DOI_HERE.svg" alt="DOI">
  </a>
  <a href="https://github.com/YOUR_USERNAME/YOUR_REPO">
    <img src="https://img.shields.io/badge/Status-In--Preparation-blue" alt="Manuscript Status">
  </a>
</div>

## 📝 Abstract
Traditional highway alignment selection relies heavily on historical crash records, which are often unavailable or unreliable during the planning phase or in data-poor regions. This research proposes a **proactive traffic safety assessment framework** that bypasses the need for reactive accident data. By integrating the **Analytic Network Process (ANP)** with a custom Python-based **Row Sensitivity Analysis (RSA)**, the model ranks highway alignments based on geometric design consistency and Surrogate Measures of Safety (SMoS). This repository serves as the official computational supplement to the manuscript.

## 🛠️ Computational Framework
The methodology utilizes a hybrid decision-support workflow designed for high-fidelity safety modeling:

1. **Network Modeling (SuperDecisions):** Used to construct complex interdependency networks among safety criteria and calculate initial weighted supermatrices.
2. **Advanced Synthesis (Python/Colab):** Utilizes the `pyanp` library for limit matrix convergence and automated high-resolution sensitivity testing.

### Technical Specifications
| Parameter | Setting | Rationale |
| :--- | :--- | :--- |
| **Synthesis Method** | Calculus Limit Matrix | Ensures stochastic convergence of the ANP network |
| **Precision Threshold ($\epsilon$)** | $1 \times 10^{-12}$ | High-fidelity resolution for critical infrastructure decisions |
| **Maximum Iterations** | 25,000 | Guarantees numerical stability in complex feedback loops |
| **Sensitivity Limit ($p$)** | 0.995 | Evaluates decision robustness under extreme strategic perspectives |

## 📊 Evaluation Criteria: Surrogate Measures of Safety (SMoS)
The framework prioritizes proactive risk indicators, categorized by their safety impact:

* **PACF (Predicted Average Crash Frequency):** An exposure-based risk metric utilizing Safety Performance Functions (SPFs) consistent with the *Highway Safety Manual (HSM)* to estimate expected frequency based on traffic volume and alignment geometry.
* **CCR & CRR (Curvature Change Rate & Curve Radius Ratio):** Quantitative indicators of geometric consistency. CCR measures angular changes per unit length, while **CRR** evaluates the ratio of individual radii to the segment average to detect unexpected deviations in horizontal alignment.
* **$\Delta V_{85}$ (85th Percentile Speed Differential):** A critical consistency metric calculating the difference in operating speeds between successive geometric elements to identify high-risk speed violations.
* **AVC & TLR (Average Vertical Curvature & Travel Length Risk):** **AVC** assesses vertical profile impact on Stopping Sight Distance (SSD), while **TLR** quantifies cumulative exposure risk related to total alignment length.

## 🚀 How to Reproduce
1. Click the **"Open In Colab"** badge at the top of this page.
2. Ensure your weighted supermatrix (exported from SuperDecisions) is loaded into the script.
3. Execute the cells to generate the **Influence Heatmaps** and **RSA Stability Plots**.

## 📄 Manuscript Status
This code is the official implementation for a research paper currently **in preparation/pre-submission**.

* **Title:** *Proactive Traffic Safety Assessment for Highway Alignment Planning Without Crash Data*
* **Corresponding Author:** [Name] ([Email])

## 📖 License & Citation
This project is licensed under the MIT License. Once published, please cite as follows:
> [Name], (2026). "Proactive Traffic Safety Assessment for Highway Alignment Planning Without Crash Data." Python Implementation Source Code. Zenodo DOI: [Insert DOI].
---
*Last Updated: April 2026*
