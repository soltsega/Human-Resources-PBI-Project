# HR Dataset Analysis Summary

## 📊 Dataset Overview
- **Total Records:** 1,470 employees.
- **Attrition Status:** 237 employees have left (approx. 16.1% attrition rate).
- **Key Columns:** Age, Attrition, BusinessTravel, Department, MonthlyIncome, OverTime, JobSatisfaction, YearsAtCompany, etc.

## 🔍 Key Findings for Dashboard
- **Attrition & Overtime:** Out of the 416 employees who work overtime, 127 have left (30.5% attrition rate). This is significantly higher than the overall average.
- **Departmental Trends:**
    - **Sales:** High headcount with a noticeable number of "Yes" for attrition.
    - **Research & Development:** Largest department with a relatively stable workforce.
- **Income Correlation:** Most attrition cases are concentrated in the lower `MonthlyIncome` brackets (under $5,000).
- **Age Groups:** Attrition is more prevalent in the "Junior" demographic (ages 25-35).

## 💡 Implementation Tips
- **Calculated Column:** In Phase 5 of your `todo.md`, confirm you create the `Age Group` bucket, as many attrition trends are age-specific.
- **Visual Priority:** Use a **Donut Chart** for `Attrition by OverTime`—the data shows this is a major factor.
- **KPI Card:** Your `Average Monthly Income` is approximately **$6,503**. You can use this as a benchmark in your dashboard.
