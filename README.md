# ABC Company Employee Data Analysis

## Project Overview
This project analyzes **458 employees across 10 attributes** at ABC Company to evaluate team structure, positional distribution, demographics, and salary expenditure.

## Preprocessing Steps
- **Height Correction:** Replaced corrupted values in `Height` with random integers between **150 and 180** (`np.random.seed(42)`).
- **Data Integrity:** Imputed missing `College` entries as `"No College / International"` and filled missing `Salary` values using the median (`$2,836,186.00`).

## Key Insights (Data Story)
1. **Team Distribution:** Employees span **30 teams**, led by **New Orleans Pelicans** with **19 employees (4.15%)**.
2. **Positional Breakdown:** Segregated into **5 positions**, with **SG** forming the largest group (**117 employees, 25.55%**).
3. **Predominant Age Group:** The **23-26** bracket is the largest demographic (**170 employees**).
4. **Salary Expenditure:** **Cleveland Cavaliers** has the highest team payroll (**$109,824,875.00**), and **C** has the highest positional expenditure (**$466,377,332.00**).
5. **Age vs. Salary Correlation:** A weak positive correlation (**`r = 0.21`**) indicates that while older employees earn slightly more on average, salary is driven primarily by role and performance rather than age alone.
