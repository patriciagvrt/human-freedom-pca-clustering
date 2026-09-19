# Human Freedom PCA & Clustering

Exploratory analysis of global freedom profiles using Principal Component Analysis (PCA) and Hierarchical Clustering on Principal Components (HCPC) in R.

This project was developed as part of the MSc in Computational Social Science at Linköping University.

## Research Question

Do personal and economic freedoms form a single shared structure across countries, or do they combine into different geopolitical country profiles?

## Data

The analysis uses the Human Freedom Index dataset.

The original dataset contains observations from 2008 to 2016 and 123 variables. For this project, I focus on the 2016 cross-sectional data and select 11 domain-level indicators representing personal and economic freedom.

After removing observations with missing values, the final analytical dataset contains 161 countries and 11 numerical variables.

## Variables

### Personal freedom

- Rule of law
- Security and safety
- Freedom of movement
- Freedom of religion
- Freedom of expression
- Identity and relationships

### Economic freedom

- Size of government
- Legal system and property rights
- Sound money
- Freedom to trade internationally
- Regulation

## Methods

The analysis combines two multivariate techniques.

### Principal Component Analysis

PCA is used to reduce the 11 freedom indicators into a smaller number of latent dimensions.

All variables are standardized before PCA so that differences in measurement scale do not determine the components.

### Hierarchical Clustering on Principal Components

After PCA, HCPC is used to identify groups of countries with similar combinations of personal and economic freedom.

This allows the analysis to move from individual indicators to broader country profiles.

## Results

The first three principal components explain approximately 74.6% of the total variation in the selected indicators.

- PC1 explains 49.2%
- PC2 explains 14.7%
- PC3 explains 10.7%

PC1 combines both personal and economic freedom indicators, including rule of law, legal institutions, trade freedom, security, freedom of expression, regulation, and sound money.

This suggests that a large part of cross-country variation can be interpreted as a broad legal-institutional freedom dimension rather than a purely personal or purely economic dimension.

The clustering analysis identifies groups of countries with distinct combinations of personal and economic freedom.

## Workflow

```text
Human Freedom Index
        ↓
Select 2016 observations
        ↓
Select 11 freedom indicators
        ↓
Remove missing observations
        ↓
Standardize variables
        ↓
Principal Component Analysis
        ↓
Interpret latent dimensions
        ↓
Hierarchical clustering
        ↓
Compare country profiles

Only the 2016 observations are included, so the results describe differences between countries at one point in time rather than changes in freedom over time.

PCA and clustering are descriptive techniques and should not be interpreted as evidence of causal relationships between the different dimensions of freedom.
