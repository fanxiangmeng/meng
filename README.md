# Machine-learning-guided biomimetic design of dual-atom nanozymes for quorum-sensing signal hydrolysis

This repository contains the code and data processing workflows associated with the manuscript:

**Machine-learning-guided biomimetic design of dual-atom nanozymes for programmable hydrolysis of quorum-sensing signals**

submitted to *Nature Chemistry*.

The code supports the extraction of enzyme-derived structural priors, machine-learning–assisted catalyst screening, and kinetic data analysis related to the hydrolysis of N-acyl homoserine lactones (AHLs).

---

## 1. Overview

Natural AHL lactonases achieve high catalytic efficiency through cooperative metal centers, precise coordination geometry, and substrate-selective binding pockets.  
This project aims to translate these protein-level structural features into **inorganic dual-atom nanozyme active sites** using a **machine learning–guided biomimetic design framework**.

The repository includes:
- Feature construction from enzyme structural and kinetic descriptors
- Machine learning models for catalyst performance prediction
- Kinetic analysis scripts for AHL hydrolysis
- Data processing workflows supporting mechanistic interpretation

---

2. Repository Structure

.
├── data/
│ ├── enzyme_priors/ # Extracted structural and kinetic descriptors from natural AHL lactonases
│ ├── catalyst_features/ # Feature matrices for dual-atom nanozyme candidates
│ └── kinetics/ # Experimental kinetic data (e.g., 1H NMR–derived hydrolysis rates)
│
├── models/
│ ├── training/ # Machine learning training scripts
│ └── evaluation/ # Model evaluation and cross-validation
│
├── analysis/
│ ├── feature_importance.py # Interpretation of ML model decision factors
│ ├── kinetics_fit.py # Steady-state kinetic fitting (Km, kcat)
│ └── statistics.py # Statistical analysis and visualization
│
├── figures/
│ └── final/ # Figures used in the manuscript
│
├── notebooks/
│ └── exploratory/ # Jupyter notebooks for data exploration (not required for reproduction)
│
├── requirements.txt
├── README.md
└── LICENSE

yaml

---

## 3. Requirements

The code was developed and tested using Python ≥ 3.9.

Install the required dependencies using:

```bash
pip install -r requirements.txt
Main dependencies include:

numpy

pandas

scikit-learn

scipy

matplotlib

seaborn

4. Machine Learning Workflow
Enzyme-derived prior extraction
Structural and functional descriptors (metal–metal distance, coordination geometry, substrate preference) are derived from reported AHL lactonase structures.

Feature mapping to inorganic systems
Protein-level descriptors are translated into atomistic features suitable for dual-atom nanozyme modeling.

Model training and validation
Supervised learning models are trained to predict catalytic efficiency metrics for candidate nanozymes.

Interpretability analysis
Feature importance and structure–activity relationships are analyzed to reveal physicochemical origins of catalytic enhancement.

5. Kinetic Analysis
Steady-state kinetic parameters (Km, kcat) are obtained by fitting experimental hydrolysis data using Michaelis–Menten models.

Example usage:
python analysis/kinetics_fit.py --input data/kinetics/example.csv
6. Reproducibility Notes
All random seeds used in model training are explicitly fixed.

Intermediate machine learning checkpoints are not included to ensure repository clarity.

Final figures correspond exactly to those reported in the manuscript.

7. Code Availability Statement
The code supporting the findings of this study is available in this repository.
Additional data that support the plots within this paper are available from the corresponding author upon reasonable request.

8. License
This project is released under the MIT License.

9. Contact
For questions regarding the code or data processing workflows, please contact:

Fanxiang Meng
Corresponding author
