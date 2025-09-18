# AI Literacy: High School Statistics Research Project

## Overview

Students will utilize statistical research methods with the support of AI to analyze the relationship between income inequality and educational achievement.

**Subject:** Mathematics - Statistics and Social Impact  
**Suggested Tools:** Python with ChatGPT assistance, R for advanced analysis  
**Duration:** 6-week capstone project  
**Learning Objective:** Using AI to enhance statistical analysis while maintaining mathematical rigor

## Research Project: "Income Inequality and Educational Achievement: A Statistical Analysis"

### Research Development:

**Week 1-2: Literature Review with AI Enhancement**
*Research Question:* "What is the relationship between income inequality in US counties and standardized test performance, and how has this relationship changed over the past decade?"

*AI-Assisted Literature Strategy:*
*Student approach:* Used AI to help develop search strategies and evaluate academic sources
*Sample prompt:* "I'm researching the relationship between income inequality and educational outcomes. Can you suggest specific academic databases I should search and help me brainstorm keywords that would find the most relevant peer-reviewed studies?"

*Literature Review Process:*
- Identified 15 peer-reviewed studies using AI-suggested search terms
- Used ChatGPT to help understand complex statistical methods in papers
- Created annotated bibliography with AI assistance for summarizing methodology (not conclusions)

**Week 3-4: Data Collection and Cleaning**
*Data Sources:*
- Census Bureau income data (Gini coefficient by county)
- Department of Education test score data
- County demographic information

*AI-Assisted Data Processing:*
```python
# Student wrote initial data cleaning code
import pandas as pd
import numpy as np

# Initial attempt at handling missing data
df = pd.read_csv('county_data.csv')
df_clean = df.dropna()  # Student's first approach
```

*AI Consultation for Improvement:*
*Student prompt:* "I'm cleaning a dataset with county-level education and income data. I have missing values and I just used dropna(), but I'm wondering if this is the best approach. Can you explain different methods for handling missing data and help me think about which might be most appropriate for my research question?"

*Refined Approach After AI Guidance:*
```python
# More sophisticated missing data handling
# Student learned about imputation methods through AI discussion
from sklearn.impute import SimpleImputer

# Analyze missing data patterns first
missing_analysis = df.isnull().sum()
print("Missing data by column:")
print(missing_analysis)

# Use median imputation for income data (AI suggested this was 
# more robust to outliers than mean)
imputer = SimpleImputer(strategy='median')
df['median_income_imputed'] = imputer.fit_transform(df[['median_income']])
```

**Week 4-5: Statistical Analysis**
*Student's Analysis Plan:*
1. Correlation analysis between Gini coefficient and test scores
2. Multiple regression controlling for demographic factors
3. Time series analysis of trends

*AI-Enhanced Statistical Reasoning:*
*Student prompt:* "I found a correlation of -0.67 between income inequality (Gini coefficient) and math test scores. Before I conclude that inequality causes lower test scores, what other factors should I consider? Can you help me think about potential confounding variables and limitations of correlation analysis?"

*Student's Refined Analysis:*
- Added controls for population density, racial composition, per-pupil spending
- Conducted residual analysis with AI help interpreting diagnostic plots
- Used AI to understand concepts like multicollinearity and heteroscedasticity

*Advanced Statistical Work:*
```python
# Multiple regression with controls
from sklearn.linear_model import LinearRegression
from sklearn.metrics import r2_score
import statsmodels.api as sm

# Student built model incrementally with AI guidance on interpretation
X = df[['gini_coefficient', 'pop_density', 'per_pupil_spending', 
        'percent_college_educated']]
y = df['avg_math_score']

# Added statistical significance testing
X_with_const = sm.add_constant(X)
model = sm.OLS(y, X_with_const).fit()
print(model.summary())
```

**Week 6: Findings and Implications**
*Key Research Findings:*
- Strong negative correlation between income inequality and test scores persists even when controlling for other factors
- Relationship has strengthened over the past decade
- Effect size varies significantly by region

*AI-Assisted Interpretation:*
*Student prompt:* "My regression shows that income inequality significantly predicts test scores even with controls (p < 0.001, β = -12.3). Help me think about how to interpret this effect size in practical terms and what limitations I should acknowledge in my conclusions."

### Final Research Paper Highlights:

**Abstract:**
"This study examines the relationship between income inequality and educational achievement using county-level data from 2010-2020. Multiple regression analysis reveals that a one-point increase in the Gini coefficient is associated with a 12.3-point decrease in average math scores, even when controlling for population density, per-pupil spending, and adult education levels (p < 0.001, R² = 0.74)."

**Methodology Transparency:**
"Throughout this research, I used AI tools to enhance my statistical analysis while maintaining methodological rigor. Specifically, I used ChatGPT to understand advanced statistical concepts like heteroscedasticity and to help interpret diagnostic plots, but all analytical decisions and interpretations were my own. I documented all AI interactions to ensure transparency in my research process."

**Discussion of Limitations:**
"While these findings suggest a strong relationship between inequality and educational outcomes, several limitations must be acknowledged: (1) correlation does not establish causation, (2) county-level data may mask important within-county variations, and (3) unmeasured variables like school quality or family structure may confound these relationships."