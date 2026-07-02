# AI Drug Discovery Small Molecule ML and Generative AI Workflow

A reproducible project demonstrating an **AI for Drug Discovery** workflow for **small-molecule design**, integrating machine learning, generative AI, explainability, uncertainty estimation, applicability-domain analysis, multi-objective prioritisation, and agentic medicinal-chemistry triage.

This project is designed to showcase how predictive modelling and generative molecule design can be connected into a transparent decision-support workflow for small-molecule drug discovery, with emphasis on oncology-relevant targets and future extension to **BindingDB**, **ChEMBL**, and **PDBbind**.

---

## Project Overview

Modern small-molecule drug discovery requires more than a single virtual-screening score. A useful AI for Drug Discovery workflow should connect:

- molecular descriptors
- protein-ligand interaction features
- binding-affinity-style prediction
- ADME-like developability scoring
- molecular generation
- chemical validation
- explainable AI
- uncertainty estimation
- applicability-domain detection
- novelty and diversity analysis
- active-learning selection
- medicinal-chemistry decision logic

This repository provides a simulated but scientifically grounded workflow demonstrating how these components can be assembled into a reproducible AI drug discovery pipeline.

---

## Repository Contents

Recommended structure:

```text
AI-drug-discovery-small-molecule-ML-and-generative-AI-workflow/
│
├── AI for Drug Discovery_Agentic_Explainable_ML_Small_Molecule_Drug_Design.ipynb
├── AI for Drug Discovery_Generative_AI_Candidate_Molecule_Design.ipynb
│
├── figures_ai4dd/
│   ├── 01_distribution_panel.png
│   ├── 02_target_potency_boxplot.png
│   ├── 03_docking_vs_potency.png
│   └── ...
│
├── generative_ai4dd_outputs/
│   ├── figures/
│   ├── tables/
│   └── molecule_images/
│
├── manuscript/
│   └── Petalcorin_ AI for Drug Discovery_Generative_Agentic_Explainable_ML_Manuscript.docx
│
├── README.md
└── .gitignore
```

---

## Main Notebooks

### 1. Agentic and Explainable ML for Small-Molecule Drug Design

**Notebook:** ` AI for Drug Discovery_Agentic_Explainable_ML_Small_Molecule_Drug_Design.ipynb`

This notebook builds the predictive and explainable AI for Drug Discovery module. It includes:

- simulated small-molecule dataset generation
- oncology-relevant targets, LDHA, ATR, RAD52, POLQ, KRAS_G12D, and PI3K_alpha
- molecular descriptors
- protein-ligand interaction features
- docking-like scores
- graph-inspired latent variables
- pIC50 and pKd-like potency labels
- ADME-like properties
- active versus inactive classification
- continuous pIC50 regression
- model comparison
- ROC and precision-recall analysis
- confusion matrix
- global explainability
- local explanation agent
- uncertainty estimation
- applicability-domain analysis
- calibration analysis
- multi-objective lead prioritisation
- agentic medicinal-chemistry triage
- active-learning candidate selection

### 2. Generative AI Candidate Molecule Design

**Notebook:** ` AI for Drug Discovery_Generative_AI_Candidate_Molecule_Design.ipynb`

This notebook extends the first workflow from prediction to design. It includes:

- BindingDB-, ChEMBL-, and PDBbind-ready data structure
- public-dataset-inspired seed molecules
- optional RDKit molecular validation
- molecular descriptor calculation
- n-gram SMILES generation
- fragment recombination
- scaffold mutation
- optional PyTorch GRU molecule generator
- generated molecule filtering
- novelty analysis
- surrogate pIC50 prediction
- predicted active probability
- docking-like scoring
- ADME-like scoring
- hERG-like risk scoring
- synthetic accessibility-like risk
- uncertainty and applicability-domain scoring
- molecule-grid visualisation
- PCA chemical-space visualisation
- agentic triage of generated molecules
- active-learning selection for the next design round

---

## Scientific Rationale

The workflow is based on a molecular-level and systems-level view of drug discovery.

At the **molecular level**, small-molecule activity depends on:

- ligand size
- lipophilicity
- polarity
- hydrogen-bond donors and acceptors
- topological polar surface area
- aromaticity
- fraction sp3
- conformational flexibility
- hydrophobic contacts
- hydrogen bonding
- shape complementarity
- protein-ligand docking-like quality

At the **systems level**, a useful discovery workflow must also evaluate:

- predicted potency
- predicted activity probability
- ADME-like developability
- toxicity-like liabilities
- synthetic accessibility
- novelty
- diversity
- model confidence
- applicability-domain support
- experimental learning value
- medicinal-chemistry actionability

---

## Target Panel

| Target | Biological Theme |
|---|---|
| LDHA | Cancer metabolism and lactate production |
| ATR | Replication stress and DNA damage response |
| RAD52 | DNA repair pathway rewiring |
| POLQ | Alternative end joining and synthetic lethality |
| KRAS_G12D | Mutant oncogenic signalling |
| PI3K_alpha | Growth signalling and cancer pathway addiction |

---

## Example Outputs

The notebooks generate manuscript-ready outputs, including:

- molecular descriptor distributions
- target-specific potency landscapes
- docking-like score versus pIC50 plots
- potency versus ADME landscapes
- PCA molecular feature maps
- classification model comparisons
- ROC curves
- precision-recall curves
- confusion matrices
- regression performance plots
- predicted versus observed pIC50 plots
- global feature-importance plots
- partial dependence plots
- uncertainty and applicability-domain maps
- calibration curves
- multi-objective lead-prioritisation landscapes
- agentic triage decision plots
- active-learning acquisition maps
- generated molecule grids
- generated molecule chemical-space plots
- novelty versus priority plots

---

## Agentic AI Components

### Data Audit Agent

Checks dataset quality, missing values, duplicate compound identifiers, active-rate balance, and molecular-property distributions.

### Local Explanation Agent

Explains why a candidate molecule was prioritised by comparing its important features against seed or training-set medians.

### Medicinal Chemistry Triage Agent

Assigns candidate-level decisions:

- advance
- advance with caution
- optimise
- active-learning candidate
- deprioritise

### Active-Learning Agent

Selects molecules that are promising, uncertain, diverse, novel, and useful for model improvement.

---

## Installation

### Recommended Environment

```bash
conda create -n ai4dd python=3.11 -y
conda activate ai4dd
```

### Core Dependencies

```bash
pip install numpy pandas matplotlib scikit-learn notebook jupyter
```

### Optional Cheminformatics and Deep Learning Dependencies

For RDKit molecular validation and visualisation:

```bash
conda install -c conda-forge rdkit -y
```

For the optional GRU generative model:

```bash
pip install torch
```

For optional SHAP extensions:

```bash
pip install shap
```

---

## How to Run

Open Jupyter:

```bash
jupyter lab
```

Run the notebooks in this order:

```text
1. AI for Drug Discovery_Agentic_Explainable_ML_Small_Molecule_Drug_Design.ipynb
2. AI for Drug Discovery_Generative_AI_Candidate_Molecule_Design.ipynb
```

---

## Data Statement

All data generated in this project are synthetic or public-dataset-inspired.

No proprietary, patient-level, confidential assay, or restricted chemical data are included.

The workflow is designed to be adapted to public datasets such as:

- BindingDB
- ChEMBL
- PDBbind

Real-data use requires appropriate curation, licensing review, assay harmonisation, target annotation, and validation.

---

## Real-Data Extension Plan

To adapt this workflow to real datasets:

1. Download and curate target-specific BindingDB and ChEMBL records.
2. Harmonise IC50, Ki, Kd, and EC50 values into pActivity values.
3. Remove ambiguous assay qualifiers or handle them separately.
4. Standardise SMILES, remove salts, canonicalise molecules, and handle stereochemistry.
5. Add RDKit descriptors and ECFP fingerprints.
6. Add protein sequence or protein-structure descriptors.
7. Add PDBbind-derived protein-ligand contact features where available.
8. Train baseline ML models.
9. Add graph neural networks or message-passing neural networks.
10. Use scaffold-split and time-split validation.
11. Add uncertainty and applicability-domain analysis.
12. Add generative molecular design.
13. Prioritise molecules with active-learning and medicinal-chemistry triage.
14. Validate predictions experimentally.

---

## Key Methods Demonstrated

- molecular descriptor simulation
- RDKit descriptor calculation
- protein-ligand feature simulation
- docking-like score modelling
- pIC50 regression
- active-class classification
- random forest models
- gradient boosting models
- ridge regression
- multilayer perceptrons
- permutation importance
- partial dependence
- calibration analysis
- uncertainty estimation
- isolation forest applicability-domain detection
- PCA chemical-space visualisation
- n-gram SMILES generation
- fragment recombination
- scaffold mutation
- optional GRU sequence generation
- molecule-grid visualisation
- novelty and diversity scoring
- multi-objective ranking
- active-learning acquisition
- agentic decision support

---

## Manuscript

The accompanying manuscript describes the workflow as a scientific article:

**Agentic, Explainable, and Generative Machine Learning for Structure-Aware Small-Molecule Drug Design: A Simulated, Literature-Benchmarked AI for Drug Discovery Workflow**

The manuscript explains the workflow at both:

- the molecular level, including descriptors, protein-ligand interactions, potency, and developability
- the systems level, including uncertainty, applicability domain, active learning, and agentic decision-making

---

## Limitations

This project is a simulated and methodological demonstration.

Important limitations include:

- simulated affinity labels
- simulated docking-like scores
- simulated ADME-like properties
- simulated hERG-like risk
- simulated synthetic accessibility-like risk
- graph-inspired variables rather than true learned molecular embeddings
- no real docking poses
- no molecular dynamics
- no experimental validation
- no prospective assay confirmation

The generated molecules should be interpreted as computational hypotheses, not experimentally validated inhibitors.

---

## Future Work

Future versions can add:

- real BindingDB and ChEMBL curation
- PDBbind structure-derived features
- RDKit ECFP fingerprints
- graph neural networks
- protein language model embeddings
- structure-conditioned generative models
- molecular docking
- molecular dynamics
- free-energy perturbation
- retrosynthesis scoring
- DMPK and toxicity prediction
- scaffold-split validation
- active-learning experimental feedback
- Streamlit or FastAPI deployment

---

## References

Ballester, P. J., & Mitchell, J. B. O. (2010). A machine learning approach to predicting protein-ligand binding affinity with applications to molecular docking. *Bioinformatics, 26*(9), 1169-1175. https://doi.org/10.1093/bioinformatics/btq112

Gaulton, A., Bellis, L. J., Bento, A. P., Chambers, J., Davies, M., Hersey, A., Light, Y., McGlinchey, S., Michalovich, D., Al-Lazikani, B., & Overington, J. P. (2012). ChEMBL: A large-scale bioactivity database for drug discovery. *Nucleic Acids Research, 40*(Database issue), D1100-D1107. https://doi.org/10.1093/nar/gkr777

Heid, E., Greenman, K. P., Chung, Y., Li, S. C., Graff, D. E., Vermeire, F. H., Wu, H., Green, W. H., & McGill, C. J. (2024). Chemprop: A machine learning package for chemical property prediction. *Journal of Chemical Information and Modeling, 64*(1), 9-17. https://doi.org/10.1021/acs.jcim.3c01250

Kearnes, S., McCloskey, K., Berndl, M., Pande, V., & Riley, P. (2016). Molecular graph convolutions: Moving beyond fingerprints. *Journal of Computer-Aided Molecular Design, 30*(8), 595-608. https://doi.org/10.1007/s10822-016-9938-8

Lipinski, C. A., Lombardo, F., Dominy, B. W., & Feeney, P. J. (2001). Experimental and computational approaches to estimate solubility and permeability in drug discovery and development settings. *Advanced Drug Delivery Reviews, 46*(1-3), 3-26. https://doi.org/10.1016/S0169-409X(00)00129-0

Liu, T., Lin, Y., Wen, X., Jorissen, R. N., & Gilson, M. K. (2007). BindingDB: A web-accessible database of experimentally determined protein-ligand binding affinities. *Nucleic Acids Research, 35*(Database issue), D198-D201. https://doi.org/10.1093/nar/gkl999

Rogers, D., & Hahn, M. (2010). Extended-connectivity fingerprints. *Journal of Chemical Information and Modeling, 50*(5), 742-754. https://doi.org/10.1021/ci100050t

Torng, W., & Altman, R. B. (2019). Graph convolutional neural networks for predicting drug-target interactions. *Journal of Chemical Information and Modeling, 59*(10), 4131-4149. https://doi.org/10.1021/acs.jcim.9b00628

Veber, D. F., Johnson, S. R., Cheng, H. Y., Smith, B. R., Ward, K. W., & Kopple, K. D. (2002). Molecular properties that influence the oral bioavailability of drug candidates. *Journal of Medicinal Chemistry, 45*(12), 2615-2623. https://doi.org/10.1021/jm020017n

Wang, R., Fang, X., Lu, Y., & Wang, S. (2005). The PDBbind database: Methodologies and updates. *Journal of Medicinal Chemistry, 48*(12), 4111-4119. https://doi.org/10.1021/jm048957q

Wu, Z., Ramsundar, B., Feinberg, E. N., Gomes, J., Geniesse, C., Pappu, A. S., Leswing, K., & Pande, V. (2018). MoleculeNet: A benchmark for molecular machine learning. *Chemical Science, 9*(2), 513-530. https://doi.org/10.1039/C7SC02664A

---
## Citation

**Petalcorin, M.I.R** (2026). Agentic, Explainable, and Generative Artificial Intelligence for Structure-Aware Small-Molecule Drug Design. ChemRxiv. https://doi.org/10.26434/chemrxiv.15005130/v1

## Author

**Mark I.R. Petalcorin**  
Molecular biologist, biochemist, machine learning and AI scientist  
London, United Kingdom

---

## Disclaimer

This repository is for educational, portfolio, and methodological demonstration purposes only. It does not provide medical advice, does not identify experimentally validated inhibitors, and should not be used to make clinical or therapeutic decisions.

All molecules and model outputs generated by the notebooks should be treated as computational hypotheses requiring experimental validation.

