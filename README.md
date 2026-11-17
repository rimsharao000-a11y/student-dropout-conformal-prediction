# Class- and group-conditional conformal coverage for student outcomes

Reproducibility materials supporting the manuscript **Auditing Label- and Group-Conditional Coverage in Three-Class Student Outcome Prediction**.

**Authors:** Rimsha Bibi; Dr. M. Umair Shahzad (corresponding author). University of Okara, Pakistan.

## Contents
- `Paper3_analysis.ipynb`: research analysis notebook, with superseded/interrupted tuning cells removed.
- `results/`: partition-level outputs, aggregate summaries, group cell counts, and original-row-order split indices for seeds 1000–1099.
- `manuscript/main.tex`, `manuscript/supplement.tex`: manuscript and supporting analyses.
- `manuscript/Figure4*.png`: figure inputs used in the supplement.

## Data
Source: UCI Machine Learning Repository, *Predict Students' Dropout and Academic Success*, dataset 697 (4,424 observations, 36 features, three target classes). Download directly from UCI. The raw dataset is **not included** here.

## Experimental protocol
Primary experiments: 100 stratified 60/20/20 train/calibration/test partitions, seeds 1000–1099. Default random forest uses 500 trees. Separate 10-seed train-only tuning sensitivity uses seeds 42, 1, 7, 13, 21, 55, 77, 99, 123, 2024.

To reproduce, create a Python environment using the versions in `requirements.txt`, download the UCI dataset and place it where the notebook's data-loading code expects it, then execute the notebook in order. Check data path and input row order before running; `results/split_indices_1000_1099.csv` uses **zero-based original dataset row positions**.

## Release notes
The manuscript's Code Availability statement must be updated with the actual repository URL and Zenodo DOI after archiving. Research outputs have been checked against saved partition results; not all seed-42 figure source points have been independently regenerated. Please validate the notebook's dataset path and full run before claiming fully automated end-to-end reproduction.

## License
No license has been assigned to the research code in this draft. Authors should choose a code license explicitly if they wish to permit reuse. The original UCI dataset has its own license and attribution requirements.
