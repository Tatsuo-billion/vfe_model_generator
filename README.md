# VFE Model Generator

The **VFE Model Generator** project is designed to preprocess and analyze benchtop sensor data to determine the viability of predictive modeling. This workflow helps assess data quality and optimize models for force estimation.

---

## 📁 Project Structure
```
VFE-Model-Generator/
├── BenchtopDataFrameGeneration.ipynb # Step 1: Load & inspect raw data
├── BenchtopDataProcessing.ipynb # Step 2: Filter & model selection
├── datasets/ # Local storage for raw/processed data
├── .gitignore # Prevents datasets/ from being committed
└── README.md # You're here!
```

---

## 🚀 Workflow

### 1. **Data Inspection**
Use `BenchtopDataFrameGeneration.ipynb` to:
- Load raw CSV data from force sensor experiments.
- Combine and structure the data into a Pandas DataFrame.
- Visually and statistically inspect signal quality.
- Export the cleaned and processed data as a `.pkl` file.

🗂️ All raw CSVs and the exported DataFrame `.pkl` file should be saved in the `datasets/` directory.

---

### 2. **Data Processing & Modeling**
Use `BenchtopDataProcessing.ipynb` to:
- Load the exported DataFrame from the previous notebook.
- Apply filters (e.g., low-pass, smoothing).
- Explore feature engineering and preprocessing techniques.
- Train and evaluate different predictive models to estimate force or relevant outputs.
- Compare performance and select the most promising approach.

---

## 📂 datasets Directory

All data files (raw `.csv`, cleaned `.pkl`, or interim processed files) must be placed in the `datasets/` directory. This directory is excluded from version control by the `.gitignore` file to prevent large data files from being committed.

If `datasets/` does not exist, create it at the project root:

```bash
mkdir datasets

