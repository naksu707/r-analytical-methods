<div align="center">

# 📊 R Analytical Methods
### From raw data to models: cleaning, visualization and regression in R

<p>
<img src="https://img.shields.io/badge/R-276DC3?style=for-the-badge&logo=r&logoColor=white" /> <img src="https://img.shields.io/badge/tidyverse-1A162D?style=for-the-badge&logo=tidyverse&logoColor=white" /> <img src="https://img.shields.io/badge/ggplot2-E15759?style=for-the-badge" /> <img src="https://img.shields.io/badge/R%20Markdown-75AADB?style=for-the-badge&logo=rstudioide&logoColor=white" />
</p>

</div>

> [!NOTE]
> **Status: in progress 🚧** · The class exercises are being reorganized, corrected and documented as R Markdown reports.

---

## 💡 About

This repository collects my work from the **Analytical Methods** course, organized as a step-by-step path through a typical data analysis workflow in R:

**explore → visualize → tidy → model → apply to a real problem**

Each folder contains an R Markdown report rendered as a GitHub document, so the code, results and plots can be read directly on GitHub.

---

## 🗂️ Contents

| # | Topic | Data | What it covers |
|---|---|---|---|
| 01 | [**R basics and exploratory analysis**](01-r-basics-and-eda/) | Chili pepper (*Capsicum*) accessions · `Orange` trees | Data structures, missing-value codes (999 → `NA`), frequency tables, summary statistics, correlation |
| 02 | [**Data visualization with ggplot2**](02-data-visualization/) | `iris` · `ToothGrowth` · `ChickWeight` · Titanic | Grammar of graphics, scatter, bar, box and violin plots, facets, themes, interactive plots with plotly |
| 03 | [**Tidy data**](03-tidy-data/) | WHO tuberculosis report (`tidyr::who`) | Reshaping a messy real dataset with `pivot_longer()`, `separate()` and `mutate()` |
| 04 | [**Linear regression**](04-linear-regression/) | Soil temperature vs. ground cover | Correlation, simple linear model, residuals, prediction intervals |
| 05 | ⭐ [**Case study: cassava dry matter**](05-case-study-cassava-dm/) | 1,286 cassava field plots, 189 accessions | Comparing three methods to measure dry matter and predicting NIRS values |

---

## ⭐ Case study: can a NIRS scanner replace the oven?

**Dry matter content** is one of the most important traits in cassava breeding: it determines starch yield and the value of the roots. It can be measured in three ways:

| Method | How | Trade-off |
|---|---|---|
| **Oven drying** (`DM_raw`) | Weigh, dry and weigh again | Reference method, but slow |
| **Specific gravity** (`DM_gravity`) | Weigh the roots in air and in water | Fast and cheap, indirect |
| **NIRS** (`DM_nirs`) | Near-infrared spectroscopy scan | Very fast, needs calibration |

**First look at the data:**

| Comparison | Correlation (r) |
|---|---|
| NIRS vs. oven | **0.97** |
| Specific gravity vs. oven | 0.66 |

NIRS agrees closely with the reference method, while specific gravity is much less precise. The report fits regression models between the methods, checks their residuals, and predicts the NIRS value expected for a sample with **30% dry matter** in the oven.

---

## 🛠️ Tools

- **Language:** R
- **Packages:** tidyverse (dplyr, tidyr, readr, ggplot2), ggpubr, plotly, agricolae, modeest
- **Reports:** R Markdown → `github_document`
- **Environment:** RStudio / Posit Cloud

---

## ▶️ Run it

1. Clone the repository and open `r-analytical-methods.Rproj` in RStudio.
2. Install the packages:

```r
install.packages(c("tidyverse", "ggpubr", "plotly", "agricolae", "modeest", "rmarkdown"))
```

3. Open any `.Rmd` file and click **Knit**.

---

## 📁 Repository structure

```text
r-analytical-methods/
├── 01-r-basics-and-eda/
├── 02-data-visualization/
├── 03-tidy-data/
├── 04-linear-regression/
├── 05-case-study-cassava-dm/
│   ├── data/
│   ├── cassava-dry-matter.Rmd
│   └── cassava-dry-matter.md      # rendered report
└── r-analytical-methods.Rproj
```

---

## 🗺️ Roadmap

- [x] 01 · R basics and exploratory analysis
- [x] 02 · Data visualization with ggplot2
- [x] 03 · Tidy data
- [ ] 04 · Linear regression
- [ ] 05 · Case study: cassava dry matter

---

<div align="center">

Made by 💜 **[Maria Jose Ospina](https://github.com/naksu707)** 💜

</div>