### Replication files for the paper:
“When Collaboration Becomes Currency: The Paradox of Authorship Inflation in the AI Age”
- (Submitted to Scientometrics, 2025)

### Overview
- This repository contains the data and code used for the study analyzing multi-authorship trends across disciplines in the post-AI era (2018–2023).
- The paper investigates whether the rise of automation, particularly artificial intelligence (AI), has reduced or expanded collaboration in scientific publishing.

- 📁 data/            →  Cleaned and anonymized dataset (CSV)
- 📁 code/            →  Python scripts for data processing and regression analysis
- 📁 results/         →  Summary statistics and regression outputs
- 📄 README.md        →  This file

### Method Summary
- We estimated Ordinary Least Squares (OLS) regressions with year fixed effects and field interactions, controlling for variation across disciplines and publication years.
Robustness checks included log-transformation and top-coded author counts (cap = 50).

### Key finding:
- None of the regression coefficients reach conventional significance levels (all p > 0.8), suggesting that authorship inflation is a long-term, system-wide drift rather than an abrupt structural shift.

### Reproducibility
- All scripts are written in Python (v3.11) using standard packages: pandas, numpy, statsmodels, matplotlib, seaborn

### To reproduce results:
- python 01_preprocess.py
- python 02_regression_models.py

### Citation
- If you use this dataset or code, please cite as:
Shakir, S. (2025). When Collaboration Becomes Currency: The Paradox of Authorship Inflation in the AI Age. https://github.com/shujashakir/authorship-inflation-ai

### License
- Released under the MIT License.
- You are free to use, modify, and distribute with attribution.

### Contact
Dr. Shuja Shakir
Professor of Political Science, Ch. Sambhajinagar, Maharashtra, India
📧 shujashakir@gmail.com
