# When Collaboration Becomes Currency: The Paradox of Authorship Inflation in the AI Age

**Author:** Shuja Shakir  
**Affiliation:** Dr Babasaheb Ambedkar Marathwada University, Chhatrapati Sambhajinagar, Maharashtra, India  
**Submitted to:** *Scientometrics*  
**ORCID:** 0000-0002-4145-9868

---

## Overview

This repository contains the data and code used in a bibliometric study examining authorship inflation across disciplines between 2018 and 2023. The analysis investigates why author lists continue to grow in an era when AI-assisted research tools should, in principle, reduce the functional need for large teams.

The study frames the problem through three overlapping analytical axes — institutional, technological, and epistemic — and draws on 8,908 publications from high-impact journals retrieved via the OpenAlex API.

---

## Repository Contents

```
authorship_inflation_clean.ipynb     →  Main replication notebook (run this)
authorship_inflation_final_dataset.csv  →  Cleaned publication metadata (n = 8,908)
README.md                            →  This file
```

---

## How to Reproduce the Results

Place the notebook and dataset in the same folder. Open `authorship_inflation_clean.ipynb` and run all cells from top to bottom.

The notebook is fully self-contained and reproduces, in order:

- Table 1: Pandemic-free contrast of mean authors per paper (2018–19 vs 2022–23)
- Table 2: Within-field deltas with bootstrap confidence intervals
- Table 3: Collaboration spectrum by journal (mega-team and hyper-team shares)
- Table 4: Within-journal authorship inflation across top venues
- Figure 1: Mean and 90th percentile author counts, 2018–2023
- Figure 4: Collaboration regimes by journal (stacked bar)
- All regression results (Sections 5.3 and robustness checks)
- Anticipated analyses (pre-trend test, negative binomial regression, quantile regression)

All outputs are saved automatically to the working directory on completion.

---

## Data

**Source:** OpenAlex (https://openalex.org), open-access bibliographic database  
**Retrieval:** API, 2024  
**Period:** 2018–2023 (2024–2025 excluded due to incomplete indexing)  
**Corpus:** Purposive sample of high-impact journals and leading venues across four fields:

| Field | Example Venues |
|-------|---------------|
| Medical | NEJM, The Lancet, JAMA |
| STEM and AI | Science, Nature, Nucleic Acids Research, CVPR, ICCV |
| Social Sciences | American Sociological Review, American Economic Review |
| Multidisciplinary | PNAS, Nature Communications |

**Primary variable:** Number of listed authors per publication  
**Excluded:** Editorials, letters, and non-standard document types  
**Pandemic years:** 2020–2021 excluded from core comparisons to avoid confounding

---

## Method Summary

**Analytical strategy:** Sequential pipeline from descriptive analysis to regression testing to robustness verification.

**Descriptive analysis:** Annual mean author counts and 90th percentile tracked for 2018–2023. Both measures are reported because the median remains stable while the upper tail rises sharply — the central distributional finding.

**Regression:** OLS models on the pandemic-free sample (2018–2019 and 2022–2023) with a binary post-2021 indicator and field interaction terms. Heteroskedasticity-robust standard errors (HC3) throughout. Social Sciences serves as the reference category.

**Key regression finding:** Raw count OLS yields non-significant coefficients (post-2021: +2.48, p = 0.912), indicating no uniform system-wide shift. Log-transformed specification yields a significant positive coefficient (+0.64, p = 0.010), corresponding to approximately 90% proportional growth. Top-coding at 50 authors attenuates the effect to non-significance, confirming that growth is concentrated in the extreme upper tail rather than distributed across all papers.

**Bootstrap CIs:** Within-field deltas use bootstrap resampling (B = 2,000) for 95% confidence intervals.

**Robustness checks:**
- Spec A: Raw author counts (baseline OLS)
- Spec B: Log-transformed counts (proportional change)
- Spec C: Top-coded at 50 authors (sensitivity to extreme values)

**Anticipated analyses (pre-built for reviewer requests):**
- Pre-trend test: t-test comparing 2018 vs 2019 baseline stability
- Negative binomial regression: count model accounting for overdispersion
- Quantile regression at the median: formal test of tail-driven interpretation

---

## Software and Environment

| Package | Purpose |
|---------|---------|
| pandas | Data handling |
| numpy | Numerical operations |
| statsmodels | OLS, quantile regression, negative binomial |
| scipy | Bootstrap CI, t-tests |
| matplotlib | Figures |
| seaborn | Plot styling |

**Python version:** 3.11  
**All packages are standard; no custom dependencies.**

---

## Key Findings

1. Mean authorship rose from 12.1 (2018–19) to 21.1 (2022–23), a 74% increase, despite widespread AI availability — the AI Authorship Paradox.
2. Growth is concentrated in the upper tail: median team size remained stable at 6–8 while the 90th percentile nearly tripled (26 to 65).
3. Three distinct collaboration regimes are identified: Industrial-Scale Medicine (NEJM), Balanced Big Science (Science/NAR), and Selective Collaboration (Nature Communications).
4. Social Sciences show no meaningful post-2021 shift (Δ = −0.35, 95% CI [−2.67, 2.46]), suggesting epistemic culture functions as a buffer against inflationary pressure.
5. Inflationary norms are spreading beyond elite venues to AI conference proceedings and broader open-access outlets, consistent with a prestige cascade.

---

## Interpretation Note

This study is explicitly descriptive and diagnostic. The post-2021 period serves as a temporal proxy for AI diffusion rather than a direct measure of AI usage. All regression results document associations rather than causal effects. Findings should be interpreted in terms of direction and structure rather than precise magnitude, given the smaller post-2021 sample.

---

## Citation

If you use this dataset or code, please cite:

> Shakir, S. (2025). When Collaboration Becomes Currency: The Paradox of Authorship Inflation in the AI Age. *Scientometrics*. https://github.com/shujashakir/authorship-inflation-ai

---

## License

Released under the MIT License. You are free to use, modify, and distribute with attribution.

---

## Contact

**Dr Shuja Shakir**  
Professor of Political Science  
Dr Babasaheb Ambedkar Marathwada University  
Chhatrapati Sambhajinagar, Maharashtra, India  
shujashakir@gmail.com
