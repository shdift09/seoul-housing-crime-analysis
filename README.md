# Apartment Prices and Crime Rates in Seoul (2014–2022)

**Statistical Data Analysis | R | Data Visualization | Regression Modeling**

## Project Overview

This project investigates the relationship between apartment transaction prices and recorded crime rates across Seoul's 25 districts from 2014 to 2022.

By integrating apartment transaction, crime occurrence, and population datasets, the analysis examines geographic and temporal patterns in crime rates and their associations with apartment prices.

**Research Question:** Is there an association between apartment transaction prices and recorded crime rates across Seoul districts?

## Project Background

This analysis originated as a group project for CDS 101 (Statistical Data Analysis) at George Mason University.

For my individual portfolio, I independently revisited the original datasets, restructured the analytical workflow, refined the statistical interpretations, and expanded the methodology with additional statistical models and robustness checks.

## Tools and Techniques

**Programming:** R, R Markdown

**Key Libraries:** tidyverse, broom, knitr, sandwich, lmtest

**Analytical Methods:**
- Data cleaning, transformation, and integration
- Exploratory data analysis and visualization
- Simple linear regression and hypothesis testing
- Benjamini–Hochberg multiple-testing correction
- District and year fixed effects regression
- District-clustered robust standard errors
- District-cluster bootstrap confidence intervals
- Cohen's d effect size analysis
- Leave-one-district-out sensitivity analysis

## Data and Methodology

The analysis combines three datasets covering 25 Seoul districts from 2014 through 2022:

1. **Apartment Transactions:** District-level average apartment transaction prices per square meter.
2. **Crime Records:** Recorded occurrences of murder, robbery, rape, larceny, and violence.
3. **Population Statistics:** Annual district populations used to calculate crime rates per 100,000 residents.

The integrated dataset contains 225 district-year observations and 1,125 district-year-crime-category records.

For descriptive comparisons, housing price groups were defined using each year's median district-level apartment price.

## Key Findings

**1. Exploratory Regression**

The unadjusted simple regression found a weak negative association between apartment prices and total recorded crime rates, but the relationship was not statistically significant under conventional OLS assumptions (p = 0.1870, R² = 0.0078).

**2. Housing Price Group Comparison**

Districts in the High-Price group had higher average recorded total crime rates than those in the Low-Price group in all nine years.

The equal-weighted annual mean difference (Low-Price minus High-Price) was approximately −382.70 incidents per 100,000 residents.

**3. Bootstrap and Sensitivity Analysis**

The district-cluster bootstrap yielded a 95% percentile confidence interval of [−806.98, −51.40] for the descriptive group difference.

Leave-one-district-out sensitivity analysis indicated that the direction of the group difference remained negative, although the magnitude varied depending on which district was excluded.

**4. Fixed Effects Regression**

After controlling for district and year fixed effects and using district-clustered robust standard errors, the association between apartment prices and total crime rates was not statistically significant (p = 0.26036).

## Interpretation and Limitations

Descriptive group comparisons and fixed effects regression address different questions and should not be interpreted as interchangeable evidence.

The results describe statistical associations rather than causal effects. Potential confounding variables, differences in crime reporting and population exposure, and the limited number of district clusters should be considered when interpreting the findings.

## Project Takeaways

This project strengthened my experience in integrating multiple datasets, implementing statistical analyses in R, evaluating model assumptions, and communicating uncertainty.

Independently extending the original study reinforced the importance of distinguishing descriptive patterns from regression-based inference and evaluating conclusions through robustness checks.
