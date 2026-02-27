# Determinants of political radicalization

# Project Overview

The increasing ideological polarization of political debates and the rising frequency of terrorism-related events pose serious risks to the security and stability of societies.

This project aims to examine the determinants of terrorist radicalization as theorized by social and psychological literature, and to identify which factors have an actual explanatory power regarding the approval of terrorism as a tool for political, ideological, or religious struggle.

To achieve this, a large, high-quality dataset—long recognized in social research—was used, and supervised learning techniques were applied to analyze the data.

# Data and Methodology

A high-quality public dataset was used: the World Values Survey.

A sample of Armenian participants was selected, a country historically affected by terrorism-related phenomena.

Analyses were conducted to test the relationship between social-psychological determinants and support for terrorism.

# Libraries Used

Data preprocessing and analysis were conducted using JupyterLab (version 4.0.11) within the Anaconda environment (version 24.11.1), based on Python 3.12.4. The following libraries were also used:

Pandas (v2.2.2) for data manipulation and cleaning

Seaborn (v0.13.2) for data visualization

Statsmodels (v0.14.2) for statistical modeling and outlier detection

Scikit-learn (v1.4.2) for data transformation and penalized regression analyses

SciPy (v1.11.4) for numerical computations

# Predictor Selection

Items were selected based on conceptual alignment with the determinants summarized in Table 1 (see notebook).

Items with similar wording or overlapping content across different measurement scales were filtered:

Less comprehensive items were discarded to favor generalization.

Items with a high number of response levels were removed to reduce dimensionality when coding dummy variables.

This selection procedure was repeated three times by the author to ensure internal consistency.

A total of 93 predictors were selected.

# Data Preparation and Cleaning

The original dataset contained 97,220 observations and 613 columns.

After column selection and filtering for the Armenian sample, the dataset included 1,223 observations and 93 columns.

Rows with missing values (-1, -2, -3, -4, -5) were removed, resulting in a final dataset of 332 observations.

Median imputation was initially considered but discarded due to the high number of replacements, which would have substantially altered predictor distributions.

Selected columns were renamed for clarity.

# Variable treatment:

Following common practice in social psychology (e.g., Robitzsch 2021), ordinal variables with 5 or more response levels were treated as continuous.

Remaining categorical variables were converted to dummy variables, bringing the total number of predictors to 147.

Skewness of continuous variables was calculated, and variables with skewness < -1 or > +1 were transformed.


# Objectives

Estimate the fit of an explanatory model for the determinants of terrorism approval as a political, ideological, or religious tool in an Armenian sample.

Reduce model dimensionality to improve accuracy, robustness, and interpretability.

The full list of predictors, including original measurement levels before categorical transformations, is available in the notebook.

Response Variable:

Justifiable – Terrorism as a political, ideological, or religious means (1 = Never justifiable, 10 = Always justifiable)


# Key Findings

The data do not meet the assumptions required for ordinary least squares (OLS) estimation.

The tested model is underspecified.

Studying theories of terrorist radicalization from a social-psychological perspective requires a high-dimensional variable space and methods suitable for handling complex relationships.

Recommendations for Future Research

Future studies using datasets similar to the one employed here should:

Use statistical models capable of handling high-dimensional data.

Maintain flexibility in methodological approaches (e.g., classification vs. regression).

Adopt theoretical models that allow for precise operationalization of variables.
