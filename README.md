# Smartphone Market Survey & Statistical Analysis in R

A statistics course project analyzing consumer smartphone preferences — from raw survey data to hypothesis testing, correlation, and probability modeling.

**Course:** Probability and Statistics (BMAT202P) · VIT Chennai
**Team:** Kaushal TS, Anant Kumar Singh, Arsh Saxena, Ann Maria Joby, Dipyaman Chakraborty

---

## Problem Statement

Understanding consumer preferences in the smartphone market is hard — there's a lot of noise in what people say they want versus what actually drives purchase decisions. This project collects real survey data and applies statistical methods to find which specs (RAM, storage, camera, price) actually matter to buyers, and whether popular brand assumptions hold up under a formal test.

## Dataset

- **100 survey responses**, self-collected
- Variables: preferred brand, price range, minimum storage (ROM), minimum RAM, camera megapixels, screen size, primary use case, daily usage hours, replacement cycle

## Methods

- **Data cleaning & visualization** — bar charts, pie charts, line plots, boxplots, and scatter plots in base R
- **Descriptive statistics** — mean, median, mode, standard deviation, and moments for each spec category
- **Correlation & regression** — Pearson correlation and linear regression between storage and RAM; partial and multiple correlation across storage, RAM, and daily usage
- **Hypothesis testing** — two-sample z-tests comparing brands (e.g., OnePlus vs. Xiaomi usage span, Apple vs. Samsung storage preference) at 5% significance
- **Probability modeling** — binomial and Poisson distributions applied to purchase likelihood by price bracket and RAM tier

## Key Visualizations

**Storage (ROM) distribution across respondents**
![ROM distribution](images/pie_chart_rom.png)

**RAM preference distribution**
![RAM distribution](images/pie_chart_ram.png)

**Brand popularity across the sample**
![Brand popularity](images/bar_chart_brand.png)

**Demand by price range**
![Price range distribution](images/line_chart_price_range.png)

**RAM distribution across storage tiers**
![Boxplot of RAM by ROM](images/boxplot_ram_by_rom.png)

**Storage vs. RAM — regression fit**
![Storage vs RAM regression](images/scatter_regression_rom_ram.png)

## Key Findings

- **Storage and RAM are positively correlated** (r ≈ 0.57, p < 0.001) — buyers who want more storage tend to also want more RAM, as confirmed by both a Pearson correlation test and a significant linear regression fit.
- **No statistically significant brand-level differences** were found in usage span (OnePlus vs. Xiaomi) or storage preference (Apple vs. Samsung) at the 5% significance level — in both cases the z-statistic fell below the critical value, so we failed to reject the null hypothesis of no difference.
- **8GB RAM and 128GB storage** are the clear majority preference in the sample, with Samsung as the most represented brand.

## Tools

R, RStudio · base R plotting (`barplot`, `pie`, `boxplot`, `plot`) · `moments` package for statistical moments

## Files

- `report.pdf` — full project report with all analysis, code, and output
