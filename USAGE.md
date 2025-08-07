# 🛠️ Instructions for Using the RYFoR Dataset Template

This guide walks you through the steps required to use, adapt, and share your own dataset based on this template. The goal is to help you stay aligned with FAIR principles and good research data practices.

## 📚 Table of Contents

0. [🚀 Getting Started](#-getting-started)
1. [📁 Organize Your Dataset](#-1-organize-your-dataset)
2. [📝 Document Your Dataset](#-2-document-your-dataset)
3. [📊 Explore and Analyze](#-3-explore-and-analyze)
4. [🧬 Declare Metadata](#-4-declare-metadata)
5. [♻️ Reuse and Share](#-5-reuse-and-share)
6. [🤝 Collaborate](#-6-collaborate)

---

## 🚀 Getting Started

### Prerequisites

- Python 3.8+
- Jupyter Notebook
- Pandas, Matplotlib, Seaborn

### Installation

```bash
# Clone the repository
git clone https://github.com/ryfor/RYFOR-data-template.git
cd RYFOR-data-template

# Create environment
conda env create -f environment.yml
conda activate ryfor-data-template
```

---

## 📁 1. Organize Your Dataset

Place your raw data files into:

```
data/raw/
```

If needed, you can add `data/processed/` for cleaned or transformed versions.

---

## 📝 2. Document Your Dataset

Update the following files inside the `docs/` folder:

- `codebook.md`: Define variables and controlled vocabularies.
- `data_dictionary.md`: Describe each column and data type.
- `methodology.md`: Explain how the data was collected or generated.
- `quality_report.md`: Highlight data issues, cleaning steps, and completeness.

---

## 📊 3. Explore and Analyze

Use the notebooks in the `notebooks/` folder:

- `01-explore_raw_data.ipynb`: Automatically summarizes and visualizes your dataset.
- Add your own notebooks like `02-preprocessing.ipynb`, `03-analysis.ipynb`, etc.

You can run them using:

```bash
jupyter notebook
```

---

## 🧬 4. Declare Metadata

Update the metadata under the `catalog/` folder:

- `catalog.json`: Human and machine-readable metadata.
- `schema.yaml`: Structural and semantic definition of your dataset.

---

## ♻️ 5. Reuse and Share

- Update `CITATION.cff` to declare how your dataset should be cited.
- Include a license in the `LICENSE` file (CC BY recommended).
- Optional: fill the `FAIR/` folder with machine-readable FAIR profiles or linked vocabularies.

---

## 🤝 6. Collaborate

Encourage contributions with:

- `CONTRIBUTING.md`
- `CODE_OF_CONDUCT.md`
- Open issues or pull requests for improvement.

---

## 🗂️ Project Structure

```
RYFOR-data-template/
├── .github/                      # GitHub issue templates
├── catalog/                      # Metadata catalog and schema definitions
│   ├── catalog.json
│   └── schema.yaml
├── data/
│   └── raw/                      # Source data files
│       └── metadata.csv
├── docs/                         # Human-readable documentation
│   ├── codebook.md
│   ├── data_dictionary.md
│   ├── methodology.md
│   └── quality_report.md
├── notebooks/                    # Jupyter notebooks for data analysis
│   └── 01-explore_raw_data.ipynb
├── src/                          # Python source code modules
│   └── family_survey_data/
│       ├── __init__.py
│       ├── data_loader.py
│       ├── preprocessing.py
│       └── utils.py
├── FAIR/                         # FAIR principles declaration (TO BE COMPLETED)
├── CHANGELOG.md
├── CITATION.cff
├── CODE_OF_CONDUCT.md
├── CONTRIBUTING.md
├── LICENSE
├── README.md
├── environment.yml
└── pyproject.toml
```
