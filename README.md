# Exploratory Data Analysis – Course Project (BCSE331L)

**Name:** Vyom Khurana
**Reg. No.:** 23BDS0081
**Course:** BCSE331L / BCSE331P – Exploratory Data Analysis, VIT Vellore
**Faculty:** Prof. Balaji G N

**Demo video:** [Watch the project demonstration](https://drive.google.com/drive/folders/1-E9nqPz4qoCq0UACKuIwQ9jodzxtQR_N)
**Full report (code + outputs + plots):** [`Exploratory_Data_Analysis_Submission_23BDS0081.pdf`](Exploratory_Data_Analysis_Submission_23BDS0081.pdf)

---

## About the project

This project covers the full Exploratory Data Analysis process in **R**: creating and joining data, handling missing values and outliers, transforming data, visualising single and multiple variables, time series analysis, descriptive statistics and correlation, clustering, and Principal Component Analysis.

## Datasets

| Dataset | Used in | Details |
|---|---|---|
| [SuicideChina.csv](https://github.com/salemprakash/EDA/blob/main/Data/SuicideChina.csv) | Assessments 2, 3, 5, 7, 8, 9 | 2571 records, 12 columns (Age, Sex, Education, Occupation, Urban, Hospitalised, Died, Year, Month, method, IDs) |
| AirPassengers (built into R) | Assessment 6 | Monthly airline passengers, Jan 1949 – Dec 1960 |
| Small product data frames (created in code) | Assessment 1 | Product ID, name, price, company location |
| Numeric vector (created in code) | Assessment 4 | 10 values for normalisation |

The SuicideChina data is read straight from GitHub inside the R code, so no download is needed.

## Repository contents

```
EDA/
├── README.md
└── Exploratory_Data_Analysis_Submission_23BDS0081.pdf
```

The PDF contains the R code, console output and plots for every assessment.

## What each part does

| # | Topic | Main R functions | Key result |
|---|---|---|---|
| 1 | Data frame operations | `rbind`, `cbind`, `merge` | Append, concatenate, inner / left / right / full outer joins |
| 2 | Missing values | `is.na`, `colSums`, `na.omit`, `zoo::na.locf` | Mean, median, mode, forward / backward fill and constant imputation |
| 3 | Data cleaning and visualisation | `dplyr`, `ggplot2`, `quantile` | Removed a >70% empty column, IQR outlier check, histogram, violin, bar, pie, lollipop and faceted plots |
| 4 | Data transformation | arithmetic in base R | Min-max scaling to [-3, 3], [-1, 1], [0, 1]; z-score; decimal scaling |
| 5 | Multivariate visualisation | `ggplot2` (`colour`, `shape`, `size`) | Scatter plots with 3 and 4 variables, bubble plot |
| 6 | Time series analysis | `start`, `end`, `frequency`, `decompose` | Upward trend; seasonal peak in July–August, lowest in November |
| 7 | 1D, 2D and N-D analysis | `e1071::skewness`, `kurtosis`, `table`, `cor` | Age: mean 52.63, median 53, SD 19.78, skewness 0.014, kurtosis −1.005; Pearson r (Age, Month) = −0.028 |
| 8 | Clustering | `scale`, `kmeans`, `dist`, `hclust` (Ward), `cutree` | K-means (k = 3): 923 / 899 / 749; hierarchical (k = 3): 807 / 893 / 871 |
| 9 | Principal Component Analysis | `scale`, `prcomp` | Scree plot, biplot and PC scores |

## How to run the code

1. Install R and RStudio.
2. Install the packages once:

   ```r
   install.packages(c("ggplot2", "dplyr", "tidyr", "stringr", "forcats", "zoo", "e1071"))
   ```

3. Copy the code of any assessment from the PDF into RStudio and run it. An internet connection is needed to load the dataset.

## Tools

R, RStudio, ggplot2, dplyr, tidyr, stringr, forcats, zoo, e1071