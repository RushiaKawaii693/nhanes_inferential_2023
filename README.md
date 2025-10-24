# NHANES 2021-2023 Inferential Analytics

## Project Overview
This project performs inferential statistical analyses on NHANES (National Health and Nutrition Examination Survey) 2021-2023 data. The goal is to explore relationships between health metrics and demographic variables using Python in Google Colab.

#3 CoLab Link: https://colab.research.google.com/drive/1s_X7kUEhoql47Mb5tL_v0a3JFsBS1fbh?usp=sharing

## Dataset
**Source**: NHANES 2021-2023  
**Website**: https://wwwn.cdc.gov/nchs/nhanes/

The following datasets were merged for this analysis:
- Demographics (P_DEMO)
- Blood Pressure (P_BPXO)
- Physical Activity (P_PAQ)
- Weight/Height (P_WHQ)
- Vitamin D (P_VID)
- Hepatitis B (P_HEPB_S)
- Kidney Conditions (P_KIQ_U)

## Variables Used
- **DMDMARTZ**: Marital Status (recoded to Married/Not Married)
- **DMDEDUC2**: Education Level (recoded to Bachelor's or Higher/Less than Bachelor's)
- **RIDAGEYR**: Age in Years
- **BPXOSY3**: Systolic Blood Pressure
- **BPXODI3**: Diastolic Blood Pressure
- **PAD680**: Minutes of Sedentary Behavior (cleaned)
- **WHD020**: Self-Reported Weight (cleaned)
- **LBDVD2LC**: Vitamin D Lab Interpretation
- **LBXHBS**: Hepatitis B Antibodies
- **KIQ022**: Weak/Failing Kidneys

## Research Questions & Analyses

### Question 1: Association between Marital Status and Education Level
**Research Question**: Is there an association between marital status (married or not married) and education level (bachelor's degree or higher vs. less than a bachelor's degree)?

**Variables**:
- Independent: Marital Status (categorical)
- Dependent: Education Level (categorical)

**Statistical Test**: Chi-Square Test of Independence

**Rationale**: Both variables are categorical, so we use a chi-square test to determine if there is a statistically significant association between them.

**Result**: Significant association found (p < 0.05)

---

### Question 2: Sedentary Behavior by Marital Status
**Research Question**: Is there a difference in the mean sedentary behavior time between those who are married and those who are not married?

**Variables**:
- Independent: Marital Status (categorical: Married, Not Married)
- Dependent: Sedentary Behavior Time in minutes (continuous)

**Statistical Test**: Independent Samples t-test

**Rationale**: We are comparing means of a continuous variable (sedentary time) across two independent groups (married vs. not married).

**Result**: Significant difference found (p < 0.05) - Married individuals have less sedentary time

---

### Question 3: Age, Marital Status, and Systolic Blood Pressure
**Research Question**: How do age and marital status affect systolic blood pressure?

**Variables**:
- Dependent: Systolic Blood Pressure (continuous)
- Independent 1: Age in years (continuous)
- Independent 2: Marital Status (categorical)

**Statistical Tests**: 
- Pearson Correlation (Age × Blood Pressure)
- Independent t-test (Marital Status × Blood Pressure)

**Rationale**: We examine both the continuous relationship between age and BP (correlation) and whether marital status groups differ in BP (t-test).

**Results**: 
- Strong positive correlation between age and BP (p < 0.05)
- No significant difference in BP by marital status (p > 0.05)

---

### Question 4: Correlation between Weight and Sedentary Behavior
**Research Question**: Is there a correlation between self-reported weight and minutes of sedentary behavior?

**Variables**:
- Variable 1: Self-reported weight in pounds (continuous)
- Variable 2: Sedentary behavior time in minutes (continuous)

**Statistical Test**: Pearson Correlation

**Rationale**: Both variables are continuous, so we use correlation to assess the strength and direction of their linear relationship.

**Result**: Significant weak positive correlation (r = 0.156, p < 0.05)

---

### Question 5: Education Level and Diastolic Blood Pressure
**Research Question**: Does education level affect diastolic blood pressure?

**Variables**:
- Independent: Education Level (categorical: Bachelor's or Higher, Less than Bachelor's)
- Dependent: Diastolic Blood Pressure (continuous)

**Statistical Test**: Independent Samples t-test

**Rationale**: We are comparing means of a continuous variable (diastolic BP) across two independent groups (education levels).

**Result**: Significant difference found (p < 0.05) - Bachelor's degree holders have lower diastolic BP

---

## Key Findings

1. **Marital status and education are related** - Married individuals have higher rates of Bachelor's degrees or higher
2. **Married people are less sedentary** - About 18.67 minutes less per day on average
3. **Age strongly predicts blood pressure** - As age increases, systolic BP increases significantly
4. **Marital status does not affect blood pressure** - No significant difference between groups
5. **Weight and sedentary behavior are weakly related** - Small positive correlation exists
6. **Higher education associated with lower blood pressure** - Bachelor's holders have slightly lower diastolic BP

## Tools & Libraries Used
- **Python 3.x**
- **pandas**: Data manipulation and cleaning
- **numpy**: Numerical operations
- **scipy.stats**: Statistical tests (chi2_contingency, ttest_ind, pearsonr, f_oneway)
- **matplotlib**: Data visualization
- **seaborn**: Enhanced visualizations

## Files in Repository
- `nhanes_inferential_analysis.ipynb`: Complete Jupyter notebook with all analyses
- `README.md`: This file

## How to Run
1. Open the notebook in Google Colab
2. Upload NHANES 2021-2023 data files when prompted
3. Run all cells sequentially
4. View results and visualizations



## References
- National Health and Nutrition Examination Survey (NHANES). Centers for Disease Control and Prevention. https://www.cdc.gov/nchs/nhanes/
