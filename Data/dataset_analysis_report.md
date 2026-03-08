# Phase 2: Dataset Analysis Report

## Dataset Overview
The analysis was performed on the `IBM-HR-Analytics-Employee-Attrition-and-Performance-Revised.csv` file to understand the workforce demographics and attrition patterns.

## Key HR Metrics
| Metric | Value |
| :--- | :--- |
| **Total Employees** | 1,470 |
| **Attrition Rate** | 16.12% |
| **Average Monthly Income** | $6,502.93 |
| **Average Years at Company** | 7.01 years |

## Column Verification
All requested columns are present and properly formatted:
- **Demographics**: `Age`, `Education`
- **Organizational**: `Department`, `JobRole`, `YearsAtCompany`
- **Behavioral/Sentiment**: `Attrition`, `JobSatisfaction`, `WorkLifeBalance`, `OverTime`, `PerformanceRating`
- **Economic**: `MonthlyIncome`

## Detailed Distributions

### Department Distribution
- **Research & Development**: 961 employees (65.37%)
- **Sales**: 446 employees (30.34%)
- **Human Resources**: 63 employees (4.29%)

### OverTime Distribution
- **No**: 1,054 employees (71.70%)
- **Yes**: 416 employees (28.30%)

### Top 5 Job Roles
1. **Sales Executive**: 326
2. **Research Scientist**: 292
3. **Laboratory Technician**: 259
4. **Manufacturing Director**: 145
5. **Healthcare Representative**: 131

### Education Levels
- **Level 3**: 572
- **Level 4**: 398
- **Level 2**: 282
- **Level 1**: 170
- **Level 5**: 48

## Insights for Power BI Development
- The dataset is clean with no missing critical headers.
- **Attrition** is a binary "Yes"/"No" categorical field, which will need to be converted to a numeric measure (0/1) in Power BI for easier calculation of the Attrition Rate.
- **MonthlyIncome** and **YearsAtCompany** are continuous variables suitable for trend analysis and correlation with attrition.
- **JobSatisfaction** and **WorkLifeBalance** are ordinal scales (likely 1-4) that can be used to identify areas for management intervention.
