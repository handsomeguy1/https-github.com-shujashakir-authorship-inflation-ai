### Replication files for the paper:
“When Collaboration Becomes Currency: The Paradox of Authorship Inflation in the AI Age”
- (Submitted to Scientometrics, 2025)

### Overview
- This repository contains the data and code used for the study analyzing multi-authorship patterns across disciplines between 2018 and 2023. The analysis examines how collaboration structures have evolved in the period contemporaneous with the widespread availability of AI-assisted research tools.

- 📁 data/            →  Cleaned and anonymized dataset (CSV)
- 📁 code/            →  Python scripts for data processing and regression analysis
- 📁 results/         →  Summary statistics and regression outputs
- 📄 README.md        →  This file

### Method Summary
- The analysis estimates Ordinary Least Squares (OLS) regression models with year fixed effects and field interactions to assess changes in author counts over time.
- Robustness checks include log-transformed author counts and top-coding extreme values (cap = 50) to evaluate sensitivity to upper-tail concentration.

### Key finding:
- The standard linear (OLS) regression models do not yield statistically significant coefficients for the post-2021 period or its interactions with field categories (all p > 0.8). This null result, considered alongside the observed descriptive increases in mean and upper-tail authorship, indicates that authorship inflation is not well captured by a uniform, system-wide linear shift. Robustness checks—including log-transformed specifications and top-coding extreme values—are consistent with the interpretation that observed growth is concentrated in the extreme upper tail of the distribution, particularly among large collaborative (“mega-team”) publications.

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
