# Conditional VAE for Molecular Generation Based on Solubility

This repository contains two Jupyter notebooks and the real/generated CSV files supplied for a molecular-generation and fingerprint-validation project using ESOL solubility data.

## Repository structure

```text
molecular-cvae/
├── README.md
├── requirements.txt
├── .gitignore
├── notebooks/
│   ├── Conditional VAE for molecules based on solubility.ipynb
│   └── Validation of generated molecular fingerprints.ipynb
└── datasets/
    ├── esol_dataset.csv
    ├── GDB11_top5_Tanimoto_per_generated_sample_ECFP4.csv
    └── matches_above_0.8.csv
```

## Datasets and provenance

- `datasets/esol_dataset.csv` is the **real/original dataset** supplied for this project.
- `datasets/GDB11_top5_Tanimoto_per_generated_sample_ECFP4.csv` is a **generated-sample results file**.
- `datasets/matches_above_0.8.csv` is a **generated-sample subset/results file**.
- `datasets/gen_ESOL_class1_cont.csv` contains generated ECFP fingerprint vectors and is the generated file used by the validation notebook. It was supplied separately and is included here so the validation notebook has its expected input.

The generated-sample CSVs are not the original real dataset. They are kept alongside it in `datasets/` as requested, and clearly distinguished here by their descriptions and filenames.

## Notebooks

- **Conditional VAE for molecules based on solubility.ipynb** — model/training and molecular-generation workflow.
- **Validation of generated molecular fingerprints.ipynb** — validation and comparison workflow for generated molecular fingerprints.

## Getting started

1. Create and activate a Python environment.
2. Install dependencies from `requirements.txt`.
3. Open the notebooks in Jupyter from the `notebooks/` folder.
4. The notebooks use paths relative to their own location, such as `../datasets/esol_dataset.csv`.
5. The CVAE notebook can write `gen_ESOL_class1_cont.csv` into `datasets/`; the supplied copy is included so the validation notebook can use it immediately. If you rerun the generation notebook, it may overwrite this file.

## Reproducibility and limitations

The notebooks have had their CSV paths adjusted for this folder structure, but they have not been fully executed end-to-end or scientifically validated as part of packaging. Check the notebook outputs and dependency versions before relying on results.

## Before publishing

Confirm that you have permission to redistribute the real dataset and generated CSV files. Consider Git LFS or an external data host if file size becomes an issue. No license is included because project ownership and reuse terms have not been specified.
