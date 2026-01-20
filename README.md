This repository contains a fully reproducible implementation of the Gravity-Modulated Viability Model (GMVM) used in the manuscript.

Purpose

Reproduce all Results and Supplementary Figures directly from the Methods.

Demonstrate that conclusions follow deterministically from the model formulation, without post-hoc tuning.

Files

gmvm_review_pipeline.py
Single, self-contained script that:

Loads benchmark data (CSV or embedded fallback)

Computes derived quantities (xi, b, log10(b))

Generates all figures used in the manuscript

Exports processed data and a run manifest

benchmark_data.csv (optional)
External benchmark dataset.
If absent, an embedded dataset is used to ensure executability.

gmvm_outputs/ (generated)

Figure_1_Envelopes.png

Figure_2_b_Jitter.png

Figure_3_CrossoverWidth_logQ.png

Figure_S1_Sensitivity.png

processed_benchmark_with_derived.csv

run_manifest.txt (explicit parameter settings)

How to Run
python gmvm_review_pipeline.py

Requirements

Python ≥ 3.9

numpy, pandas, matplotlib

Notes for Reviewers

All model equations correspond exactly to Methods Sections 2.3–2.7.

Parameter values are explicitly fixed and recorded in run_manifest.txt.

No figure depends on manual adjustment or post-processing.

Supplementary material consists of figures only; no hidden analyses.
