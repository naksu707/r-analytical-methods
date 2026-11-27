<div align="center">

# R Analytical Methods
### From raw data to models: cleaning, visualization and regression in R

<p>
<img src="https://img.shields.io/badge/R-276DC3?style=for-the-badge&logo=r&logoColor=white" /> <img src="https://img.shields.io/badge/tidyverse-1A162D?style=for-the-badge&logo=tidyverse&logoColor=white" /> <img src="https://img.shields.io/badge/ggplot2-E15759?style=for-the-badge" /> <img src="https://img.shields.io/badge/R%20Markdown-75AADB?style=for-the-badge&logo=rstudioide&logoColor=white" />
</p>

</div>

---

## 💡 About

This repository collects my work from the **Analytical Methods** course, reorganized as a step-by-step path through a typical data analysis workflow in R:

**explore → visualize → tidy → model → apply to a real problem**

Each folder contains an R Markdown report rendered as a GitHub document: open any folder to read the code, results and plots directly on GitHub.

---

## 🗂️ Contents

| # | Topic | Data | What it covers |
|---|---|---|---|
| 01 | [**R basics and exploratory analysis**](01-r-basics-and-eda/) | Chili pepper (*Capsicum*) accessions · `Orange` trees | Data structures, missing-value codes (999 → `NA`), frequency tables, summary statistics, correlation heatmap, growth curves |
| 02 | [**Data visualization with ggplot2**](02-data-visualization/) | `iris` · `ToothGrowth` · `ChickWeight` · `frijol` · Titanic | Grammar of graphics, bar, box and violin plots, themes, trends over time, and a visual story of who survived the Titanic |
| 03 | [**Tidy data**](03-tidy-data/) | WHO tuberculosis report (`tidyr::who`) | Reshaping a messy real dataset step by step with `pivot_longer()` and `separate_wider_*()`, then exploring it |
| 04 | [**Linear regression**](04-linear-regression/) | Soil temperature vs. ground cover | Correlation, simple linear model, residual diagnostics, confidence and prediction intervals |
| 05 | ⭐ [**Case study: cassava dry matter**](05-case-study-cassava-dm/) | 1,286 cassava field plots, 189 accessions | Regression, Bland-Altman agreement and variety selection to compare three measurement methods |

---

## ⭐ Case study: can a NIRS scanner replace the oven?

**Dry matter content** is one of the most important traits in cassava breeding: it determines starch yield and the value of the roots. It can be measured in three ways:

| Method | How | Trade-off |
|---|---|---|
| **Oven drying** | Weigh, dry and weigh again | Reference method, but slow |
| **Specific gravity** | Weigh the roots in air and in water | Fast and cheap, indirect |
| **NIRS** | Near-infrared spectroscopy scan | Very fast, needs calibration |

**Results** (compared against the oven):

| | NIRS | Specific gravity |
|---|---|---|
| Variation explained (R²) | **93%** | 43% |
| Average bias | **+0.1 points** | −2.6 points |
| 95% limits of agreement | **−2.5 to +2.7 points** | −10.2 to +5.1 points |
| Same top 10% accessions as the oven | **14 of 19** | 9 of 19 |

**Conclusion:** NIRS can replace the oven for routine screening, keeping oven drying on a subset of samples to recalibrate it. Specific gravity is useful only to discard clearly poor roots.

---

## 🛠️ Tools

- **Language:** R
- **Packages:** tidyverse (dplyr, tidyr, readr, ggplot2, stringr), ggpubr, agricolae, modeest, knitr
- **Reports:** R Markdown → `github_document`
- **Environment:** RStudio

---

## ▶️ Run it

1. Clone the repository and open `r-analytical-methods.Rproj` in RStudio.
2. Install the packages:

```r
install.packages(c("tidyverse", "ggpubr", "agricolae", "modeest", "rmarkdown"))
```

3. Open the `README.Rmd` file inside any folder and click **Knit**.

---

## 📁 Repository structure

```text
r-analytical-methods/
├── 01-r-basics-and-eda/
├── 02-data-visualization/
├── 03-tidy-data/
├── 04-linear-regression/
├── 05-case-study-cassava-dm/
│   ├── data/            # input data
│   ├── figures/         # plots generated when knitting
│   ├── README.Rmd       # source code and text
│   └── README.md        # rendered report shown on GitHub
├── r-analytical-methods.Rproj
└── README.md
```

---

## 🗺️ Roadmap

- [x] 01 · R basics and exploratory analysis
- [x] 02 · Data visualization with ggplot2
- [x] 03 · Tidy data
- [x] 04 · Linear regression
- [x] 05 · Case study: cassava dry matter

---

> [!NOTE]
> **Project status: Completed ✅**
> This repository is finished and is no longer being updated. All projects were last verified to work correctly as of **November 24, 2026**. Later changes to browsers, libraries or dependencies may affect how some projects run.

---

<div align="center">

Made by 💜 **[Maria Jose Ospina](https://github.com/naksu707)** 💜

</div>
