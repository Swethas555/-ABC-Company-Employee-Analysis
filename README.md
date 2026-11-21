# Define pos_pct so Cell 8 runs independently without errors
pos_pct = (pos_counts / len(df) * 100).round(2)

readme_text = f"""# ABC Company Employee Data Analysis

## Project Overview
This project analyzes **{len(df)} employees across {df.shape[1]} attributes** at ABC Company to evaluate team structure, positional distribution, demographics, and salary expenditure.

## Preprocessing Steps
- **Height Correction:** Replaced corrupted values in `Height` with random integers between **150 and 180** (`np.random.seed(42)`).
- **Data Integrity:** Imputed missing `College` entries as `"No College / International"` and filled missing `Salary` values using the median (`${df['Salary'].median():,.2f}`).

## Key Insights (Data Story)
1. **Team Distribution:** Employees span **{df['Team'].nunique()} teams**, led by **{team_counts.index[0]}** with **{team_counts.iloc[0]} employees ({team_pct.iloc[0]}%)**.
2. **Positional Breakdown:** Segregated into **{df['Position'].nunique()} positions**, with **{pos_counts.index[0]}** forming the largest group (**{pos_counts.iloc[0]} employees, {pos_pct.iloc[0]}%**).
3. **Predominant Age Group:** The **{predominant_age}** bracket is the largest demographic (**{age_counts.max()} employees**).
4. **Salary Expenditure:** **{team_salary.index[0]}** has the highest team payroll (**${team_salary.iloc[0]:,.2f}**), and **{pos_salary.index[0]}** has the highest positional expenditure (**${pos_salary.iloc[0]:,.2f}**).
5. **Age vs. Salary Correlation:** A weak positive correlation (**`r = {corr:.2f}`**) indicates that while older employees earn slightly more on average, salary is driven primarily by role and performance rather than age alone.
"""

print(readme_text)
