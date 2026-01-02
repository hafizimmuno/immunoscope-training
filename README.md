IMMUNO-SCOPE

Data-Driven Profiling of a Whole-Blood Immune Mediator Signature for Viral T-Cell Surveillance

📌 Project Overview

IMMUNO-SCOPE is a research and training project aimed at developing a field-compatible, whole-blood immune profiling framework to assess durable virus-specific T-cell immunity. While antibody titers decline within a few years after vaccination, T-cell memory can persist for decades and plays a critical role in limiting viral dissemination and disease severity. However, scalable tools to monitor cellular immunity remain limited.

Using orthopoxvirus vaccination (MVA-BN) as a well-defined model system, this project develops and evaluates a biologically amplified, multi-marker immune signature that improves sensitivity beyond conventional interferon-gamma release assays (IGRAs). The framework is designed to be broadly applicable to viral T-cell immune surveillance, not limited to orthopoxviruses.

🧠 Scientific Rationale

Conventional cellular assays rely primarily on IFN-γ as a single readout, which often fails to detect low-frequency memory T cells and does not capture immune polyfunctionality. IMMUNO-SCOPE adopts a signal amplification paradigm, leveraging the biological cascade in which antigen-specific T-cell–derived IFN-γ activates innate immune cells (monocytes and neutrophils) to secrete downstream mediators such as CXCL10 (IP-10).

This downstream amplification transforms weak T-cell signals into robust, quantifiable biomarkers measurable in whole blood, enabling simplified workflows and improved scalability.

🎯 Objectives

Identify immune mediator combinations that outperform IFN-γ alone for detecting long-term virus-specific T-cell memory

Apply interpretable statistical learning to derive a minimal, non-redundant biomarker signature

Demonstrate analytical robustness and generalizability using biologically constrained feature engineering and external validation

Provide a reproducible analysis pipeline suitable for translational and surveillance-oriented research

🧪 Data Description

This repository uses synthetic (simulated) datasets generated to mimic cytokine and chemokine responses measured after whole-blood stimulation with viral peptide pools.

Simulated features include:

IFN-γ

TNF-α

IL-2

IP-10 (CXCL10)

IL-6

IL-10

Data are structured to reflect:

Stimulated vs. unstimulated (Nil) conditions

Inter-individual variability

Correlated immune responses consistent with polyfunctional T-cell immunity

⚠️ Note: No real patient data are included. The dataset is intended for methodological development and training.

🧮 Analytical Approach

The analysis pipeline emphasizes interpretability, biological plausibility, and statistical robustness.

Feature Engineering

Background-subtracted values (stimulated − Nil)

Fold-induction metrics

Selected cytokine ratios reflecting immune balance and polyfunctionality

Feature construction is hypothesis-driven to limit dimensionality and overfitting.

Statistical Learning & AI

Penalized regression models (LASSO / Elastic Net) as stable baseline methods

Tree-based models applied after dimensionality reduction

Explainable feature selection using variable importance and SHAP-style attribution

Nested cross-validation to rigorously assess model performance

External validation logic consistent with translational study design

The final output is a diagnostic score based on a minimal immune mediator signature.

📂 Repository Structure
immunoscope-training/
│
├── data/               # Simulated immune mediator datasets
├── notebooks/          # Analysis and modeling notebooks
├── results/            # Figures and model outputs
├── src/                # Reusable scripts (feature engineering, modeling)
├── README.md           # Project documentation
└── LICENSE             # MIT License

🚀 Getting Started
1️⃣ Clone the repository
git clone https://github.com/hafizimmuno/immunoscope-training.git
cd immunoscope-training

2️⃣ Install dependencies

Create a virtual environment and install required packages:

pip install -r requirements.txt


(If requirements.txt is not yet present, dependencies include pandas, numpy, scikit-learn, matplotlib, seaborn, shap.)

3️⃣ Run the analysis

Open the notebooks in sequence:

jupyter notebook

🧬 Training & Research Context

This project builds on pilot work conducted during the Erasmus Mundus LIVE Master in Vaccinology, with initial experimental training at the Institute of Tropical Medicine (ITM), Antwerp. It is conceptually aligned with doctoral-level research integrating immunology, statistical learning, and translational diagnostics.

The proposed PhD hosting environment includes:

Centre d’Immunologie de Marseille-Luminy (CIML) — expertise in innate and T-cell immunology and cytokine signaling

SESSTIM & Aix-Marseille School of AI — biostatistics and interpretable AI methodologies

🌍 Broader Impact

By reducing assay complexity and emphasizing interpretability, IMMUNO-SCOPE supports:

Scalable immune surveillance in low-resource settings

Rational booster vaccination strategies

Transferable analytical frameworks for other viral diseases

The project reflects SCHADOC’s triple “I” philosophy:
Interdisciplinarity, Innovation, and International training, with relevance both inside and outside academia.

📜 License

This project is licensed under the MIT License — see the LICENSE file for details.

🤝 Contact

H. Hassan Ahmad
Vaccinology | Immunology | Statistical Learning
GitHub: https://github.com/hafizimmuno
