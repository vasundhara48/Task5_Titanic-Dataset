# Task 5: Exploratory Data Analysis (EDA) — Titanic Dataset

**Internship:** Data Analyst Internship, Elevate Labs
**Objective:** Extract insights using visual and statistical exploration.
**Tools:** Python (Pandas, Matplotlib, Seaborn)
**Dataset:** [Titanic Dataset](https://raw.githubusercontent.com/datasciencedojo/datasets/master/titanic.csv)

## 📁 Repository Contents

| File | Description |
|---|---|
| `Task5_Titanic_EDA.ipynb` | Full Jupyter Notebook with code, charts, and observations |
| `Task5_Titanic_EDA.html` | HTML export of the notebook (viewable without Jupyter) |
| `Task5_EDA_Findings_Report.pdf` | PDF report summarizing key findings with charts |
| `titanic.csv` | Dataset used |
| `*.png` | Individual chart images used in the notebook and report |

## 🔍 What Was Done

1. **Data understanding** — used `.info()`, `.describe()`, `.value_counts()` to check structure, data types, and missing values.
2. **Light cleaning** — median-imputed `Age`/`Fare`, mode-imputed `Embarked`; engineered `FamilySize`, `IsAlone`, `AgeGroup`.
3. **Univariate analysis** — histograms and boxplots for `Age`, `Fare`, survival counts, and class distribution.
4. **Bivariate analysis** — survival rate by `Pclass`, `Sex`, `Age`, `FamilySize`; scatterplot of `Age` vs `Fare` colored by survival.
5. **Multivariate analysis** — `sns.pairplot()` across key numeric features and a `sns.heatmap()` correlation matrix, plus a class-vs-embarkation crosstab heatmap.
6. **Summary of findings** — written up at the end of the notebook and in the PDF report.

## 📊 Key Insights

- **Sex** is the strongest predictor of survival: ~74% for females vs. ~19% for males.
- **Passenger class** strongly affects survival: ~63% (1st class) down to ~24% (3rd class).
- **Fare** positively correlates with survival (proxy for class/cabin location).
- **Family size** of 2–4 had the best survival odds; solo travelers and large families (6+) fared worse.
- **Fare** is right-skewed with high-value outliers; **Cabin** has ~77% missing values.

Full details and all charts are in the notebook and the PDF report.

## 💬 Interview Questions & Answers

**1. What is EDA and why is it important?**
Exploratory Data Analysis (EDA) is the process of visually and statistically examining a dataset to understand its structure, spot patterns, detect anomalies, and check assumptions before formal modeling. It's important because it guides feature engineering, reveals data quality issues, and prevents building models on flawed assumptions.

**2. Which plots do you use to check correlation?**
Scatterplots (two continuous variables), pairplots (multiple variables at once), and correlation heatmaps (quick overview of all pairwise correlations).

**3. How do you handle skewed data?**
Apply log, square-root, or Box-Cox transformations to reduce skew, use robust scalers, or bin the variable into categories. Skew matters more for linear/distance-based models than tree-based models.

**4. How to detect multicollinearity?**
Use a correlation heatmap to spot highly correlated numeric features, or compute the Variance Inflation Factor (VIF) — a VIF above ~5–10 typically signals problematic multicollinearity.

**5. What are univariate, bivariate, and multivariate analyses?**
- *Univariate*: one variable at a time (histograms, boxplots, value counts).
- *Bivariate*: relationship between two variables (scatterplots, grouped bar charts).
- *Multivariate*: relationships among three or more variables at once (pairplots with hue, heatmaps).

**6. Difference between heatmap and pairplot?**
A heatmap shows a color-coded correlation matrix — a quick numeric summary of pairwise linear relationships. A pairplot shows actual scatterplots (plus distributions on the diagonal) for every pair of variables, revealing the shape of relationships that a single correlation number can't capture.

**7. How do you summarize your insights?**
By tying each observation back to the question at hand, ranking findings by impact on the target variable, and writing a concise narrative summary that a non-technical stakeholder could act on.

## ✅ Outcome

Gained hands-on skill in finding patterns, trends, and anomalies using univariate, bivariate, and multivariate visual exploration.
