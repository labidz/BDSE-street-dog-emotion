# BDSE-street-dog-emotion
BDSE: First emotion-annotated dataset for Bangladeshi street dogs, with PEACE method and cross-dataset evaluation


# BDSE: Bangladeshi Street Dog Emotion Dataset & PEACE Method

[![License: CC BY 4.0](https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by/4.0/)

**Paper:** "Deep-Learning Based Emotion Recognition in Bangladeshi Street Dogs: An Ethogram-Anchored Prototype Method and A Population-Specific Dataset"

**Authors:** Rohul Amin*, Md. Mehedi Rana, Aroshi Ali  
**Affiliation:** Department of CSE, Bangladesh Army University of Science and Technology (BAUST), Khulna, Bangladesh  
**Submitted to:** Arabian Journal for Science and Engineering (AJSE)

---

## Overview

This repository contains:

1. **BDSE Dataset** — 500 emotion-annotated images of free-ranging Bangladeshi street dogs (Angry/Neutral/Happy), annotated by 3 faculty annotators (Fleiss' κ = 0.782), with instance-aware 5-fold splits and veterinary validation.

2. **PEACE Method** — Prototype Ethogram-Anchored Classification Engine: a frozen-backbone interpretable classifier with 18 prototypes initialized at SigLIP text embeddings of ethogram criteria.

3. **Full experimental results** — 12-method in-domain benchmark, 10-seed cross-dataset evaluation across 16,745 images, ablation study, interpretability evidence, and OOD probe.

## Dataset Statistics

| Class | Images | Percentage |
|-------|--------|-----------|
| Angry | 200 | 40.0% |
| Neutral | 202 | 40.4% |
| Happy | 98 | 19.6% |
| **Total** | **500** | **100%** |

- Unique individual dogs: 441
- Inter-annotator agreement: Fleiss' κ = 0.782
- Unanimous agreement: 82.8%

## Key Results

- **In-domain BDSE:** PEACE macro-F1 = 0.910 ± 0.040 (matches strongest baseline)
- **Cross-dataset transfer:** PEACE > ProtoPNet (Δ = +0.128, p < 10⁻⁵), PEACE > SigLIP-LP (Δ = +0.028, p = 1.6×10⁻⁴)
- **Interpretability:** 18/18 prototypes correctly aligned with anchored class (mean margin = +0.077)

## Reproduction

All experiments run on Kaggle free-tier T4 GPUs. Notebooks in `notebooks/` are self-contained:

1. `NB2_indomain_benchmark.ipynb` — 12-method benchmark on BDSE
2. `NB5_cross_dataset_10seed.ipynb` — 10-seed cross-dataset evaluation
3. `NB6_interpretability.ipynb` — Prototype activation analysis
4. `NB6.3_final_ablation.ipynb` — Component ablation study



## License

- **Dataset (images + annotations):** [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/)
- **Code (notebooks + PEACE implementation):** [MIT License](LICENSE)

## Contact

Rohul Amin — rohul.amin@baust.edu.bd
