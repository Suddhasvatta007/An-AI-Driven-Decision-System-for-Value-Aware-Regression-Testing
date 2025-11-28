# An-AI-Driven-Decision-System-for-Value-Aware-Regression-Testing

This repository contains the code and datasets for a research project comparing five different algorithms for the constrained test case selection problem: a baseline Binary Constrained Particle Swarm Optimization (BCPSO), a Non-Dominated Genetic Algorithm - II (NSGA-II), and a purely Random Selector (RAND).

The project is structured to allow for the generation of synthetic datasets and the subsequent analysis of these datasets by each algorithm.

---

## Current Repository Structure

```
.
├── CodeFiles/
│   ├── Baseline/
│   │   ├── 124-40/
│   │   ├── 248-80/
│   │   └── BCPSO Code.ipynb
│   ├── NSGA-II/
│   │   ├── NSGA-II 40-124 implementation.ipynb
│   │   ├── NSGA-II 80-248 implementation.ipynb
│   │   ├── NSGA-II Results Comparison.ipynb
│   │   ├── 124-40/
│   │   │   └── NSGA-II Results.csv
│   │   └── 248-80/
│   │       └── NSGA-II Results.csv
│   └── Random/
│       ├── Random Selecton Code.ipynb
│       ├── 124-40/
│       └── 248-80/
├── Combined Visualization & Stat Reports/
│   ├── Combined Results Comparison.ipynb
│   ├── Statistical Results Code.ipynb
│   ├── 40-124/
│   ├── 80-248/
│   └── Raw_Data/
└── Datasets/
```

### Directory Descriptions

- **`CodeFiles/`**: Contains algorithm implementations and experiment notebooks.
  - **`Baseline/`**: Contains the BCPSO baseline notebook `BCPSO Code.ipynb` and sub-folders for the two dataset sizes (`124-40`, `248-80`) which may contain result files.
  - **`NSGA-II/`**: Includes NSGA-II implementation notebooks and a results comparison notebook. Pre-generated CSV result files are stored under the `124-40` and `248-80` subfolders.
  - **`Random/`**: Contains `Random Selecton Code.ipynb` (filename contains a small typo "Selecton") and result subfolders for `124-40` and `248-80`.

- **`Combined Visualization & Stat Reports/`**: High-level notebooks for plotting and statistical comparison across algorithms.
  - **`Combined Results Comparison.ipynb`**: Notebook to generate combined plots from multiple algorithm result files.
  - **`Statistical Results Code.ipynb`**: Notebook that performs ANOVA and post-hoc tests and compiles multi-sheet Excel reports.
  - Subfolders `40-124/`, `80-248/`, and `Raw_Data/` hold intermediate and final outputs used by these notebooks.

- **`Datasets/`**: Contains the input files required to run the experiment notebooks (e.g., mapped datasets used by the algorithms).

---

## Quick Workflow

Follow these steps to reproduce experiments and run analysis. Replace dataset filenames and paths as needed.

1. Run the BCPSO Baseline
  - Open `CodeFiles/Baseline/BCPSO Code.ipynb` and execute all cells.
  - When prompted, upload the appropriate dataset file from `Datasets/`.
  - The notebook produces an Excel report which can be moved into `CodeFiles/Baseline/124-40/` or `CodeFiles/Baseline/248-80/`.

2. Run the NSGA-II Experiments
  - Open the NSGA-II notebooks in `CodeFiles/NSGA-II/` and run the implementation cells.
  - The notebooks save results (CSV) into the `124-40` and `248-80` subfolders.

3. Run the Random Selection Baseline
  - Open `CodeFiles/Random/Random Selecton Code.ipynb` and execute the cells.
  - Provide the same dataset as used above. The notebook generates a report that can be added to the `Random` subfolders.

4. Combined Analysis and Plotting
  - Open the notebooks in `Combined Visualization & Stat Reports/` to generate combined plots and statistical reports.
  - Use the pre-generated result files in each algorithm folder (if present) to speed up analysis.

---

## Pre-generated Results

Some result files are already present in the repository under the algorithm-specific subfolders. These can be used directly with the combined analysis notebooks.

- `CodeFiles/Baseline/124-40/` and `CodeFiles/Baseline/248-80/` may contain BCPSO result files.
- `CodeFiles/NSGA-II/124-40/NSGA-II Results.csv` and `CodeFiles/NSGA-II/248-80/NSGA-II Results.csv` are available.
- `CodeFiles/Random/124-40/` and `CodeFiles/Random/248-80/` may contain Random selection reports.

---

## Notes and Suggestions

- Filenames: There is a minor typo in `CodeFiles/Random/Random Selecton Code.ipynb` ("Selecton" -> "Selection"). Renaming is optional but recommended for clarity.
- NSGA-II: One NSGA-II notebook filename includes double extension `NSGA-II 80-248 implementation.ipynb.ipynb`; consider renaming to a single `.ipynb` extension.
- If you want me to: I can run quick checks to list files in each folder, fix the filename typos, or open any notebook and extract the main entry points or README snippets.

---

## Next Steps (optional)

- Run the notebooks to regenerate reports and confirm reproducibility.
- Standardize filenames and folder naming for clarity.
- Add a `requirements.txt` or `environment.yml` describing Python and Jupyter dependencies for reproducible runs.

If you'd like, I can proceed to perform any of the optional steps above (list files, rename notebooks, add dependencies file).
