# Power Query Transformation TODO List

Perform these steps in the **Power Query Editor** before clicking "Load" to ensure your data model is professional and optimized.

## 1. Remove Redundant Columns
*   [ ] Remove `EmployeeCount` (constant value: 1)
*   [ ] Remove `Over18` (constant value: "Y")
*   [ ] Remove `StandardHours` (constant value: 80)
*   [ ] Remove `EmployeeNumber` (unless needed for specific row tracking; usually redundant for aggregate KPIs)

## 2. Numeric Conversions (For DAX Efficiency)
*   [ ] **Attrition**: Use *Replace Values* ("Yes" -> "1", "No" -> "0") and change type to **Whole Number**.
*   [ ] **OverTime**: Use *Replace Values* ("Yes" -> "1", "No" -> "0") and change type to **Whole Number**.

## 3. Data Type Validation
*   [ ] **MonthlyIncome**: Change to **Currency** or **Fixed Decimal Number**.
*   [ ] **Age**: Ensure type is **Whole Number**.
*   [ ] **YearsAtCompany**: Ensure type is **Whole Number**.
*   [ ] **JobSatisfaction / WorkLifeBalance**: Ensure type is **Whole Number** (for average calculations).

## 4. Derived Columns / Bucketing
*   [ ] **Age Group**: Create a *Conditional Column*:
    - If `Age` <= 24 then "18-24"
    - If `Age` <= 34 then "25-34"
    - If `Age` <= 44 then "35-44"
    - If `Age` <= 54 then "45-54"
    - Else "55+"
*   [ ] **Salary Range**: Create a *Conditional Column*:
    - If `MonthlyIncome` < 5000 then "Low (<5k)"
    - If `MonthlyIncome` < 10000 then "Medium (5k-10k)"
    - Else "High (>10k)"

## 5. Final Polish
*   [ ] **Rename Columns**: Ensure all columns use "Title Case" and have spaces (e.g., `JobSatisfaction` -> `Job Satisfaction`).
*   [ ] **Sort By Column**: (Optional) Prepare to sort your Age Group and Salary Range columns by a numeric index later in Power BI Desktop to avoid alphabetical sorting (e.g., "18-24" should come before "25-34").
