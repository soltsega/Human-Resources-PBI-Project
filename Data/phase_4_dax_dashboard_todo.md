# Phase 4: DAX & Dashboard Development Checklist

## 1. Setup the Measures Table
*   [ ] **Create a blank table**: Go to "Enter Data", name it `_Measures`, and load it.
*   [ ] **Move Measures**: As you create DAX formulas, move them here to keep your "Fields" pane clean.

## 2. Core DAX Measures (The "Big Four")
*   [ ] **Total Employees**:
    ```dax
    Total Employees = COUNTROWS('HR_Data')
    ```
*   [ ] **Total Attrition**:
    ```dax
    Total Attrition = SUM('HR_Data'[Attrition]) 
    // This works because we converted Attrition to 1/0 in Phase 3
    ```
*   [ ] **Attrition Rate**:
    ```dax
    Attrition Rate = DIVIDE([Total Attrition], [Total Employees], 0)
    ```
*   [ ] **Active Employees**:
    ```dax
    Active Employees = [Total Employees] - [Total Attrition]
    ```

## 3. UI & Visual Development
*   [ ] **KPI Layer**: Add 4 Card Visuals at the top for the measures above.
*   [ ] **Attrition Drivers (Charts)**:
    - **Bar Chart**: Attrition by Department.
    - **Column Chart**: Attrition by Age Group (using your new bucket).
    - **Tree Map**: Attrition by Job Role.
    - **Line Chart**: Relation between Monthly Income and Attrition.
*   [ ] **Filter Layer (Slicers)**:
    - Add slicers for `Department`, `Job Role`, `Education`, and your new `Salary Range`.

## 4. Final Formatting
*   [ ] **Theme**: Apply a consistent color palette (e.g., the professional blue/gray theme we planned).
*   [ ] **Glassmorphism**: Add subtle shadows and rounded corners to visual containers.
*   [ ] **Tooltips**: Customize tooltips to show more detail when hovering over charts.
