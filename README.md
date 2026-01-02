# IMMUNOSCOPE-Training

This repository is a **training and methods demonstration project** focused on immune biomarker discovery and explainable machine-learning analysis for assessing cellular immunity following vaccination.

The project uses a **biologically realistic, simulated whole-blood cytokine dataset** inspired by orthopoxvirus (e.g., Mpox) vaccination studies. It is designed to illustrate how multiplex cytokine and chemokine measurements can be analyzed to identify parsimonious immune signatures that outperform single-marker readouts such as IFN-γ alone.

## Scientific Motivation
Antibody titers often decline within a few years after vaccination and provide limited insight into durable protection. In contrast, long-lived T-cell memory is characterized by coordinated cytokine responses (e.g., IFN-γ, IL-2, TNF-α) and downstream chemokine amplification (e.g., CXCL10/IP-10). Translating these complex immune signals into scalable, interpretable diagnostics remains a major challenge.

This repository demonstrates a computational framework for exploring such immune signatures in a controlled, reproducible setting.

## Dataset
- **Type:** Synthetic / simulated data (no real human subjects)
- **Samples:** Vaccinated individuals and unexposed controls
- **Matrix:** Whole-blood stimulation (stimulated minus nil)
- **Analytes:** IFN-γ, IL-2, TNF-α, CXCL10 (IP-10), and related cytokines
- **Location:** `data/simulated_cytokine_data.csv`

The dataset was generated to reflect realistic biological variability, partial overlap between groups, and plausible effect sizes observed in immunological studies.

## What This Repository Demonstrates
- Structuring an immunology-focused analysis repository for research applications
- Exploratory analysis of multiplex cytokine data
- Feature selection to identify minimal immune signatures
- Use of interpretable machine-learning models in a biological context
- Critical discussion of assumptions and limitations when working with simulated data

## Results and Figures
Key analysis figures (ROC curve, cytokine group comparisons, and model coefficients) are available in `results/figures/`.

## Limitations
All data in this repository are **simulated for training purposes** and do not represent real clinical or experimental results. Conclusions drawn from this dataset are illustrative only and should not be interpreted as biological or diagnostic claims.

## Intended Audience
This repository is intended for:
- PhD applications and research training demonstration
- Immunology and vaccinology researchers interested in computational analysis
- Data scientists working at the interface of biology and machine learning
