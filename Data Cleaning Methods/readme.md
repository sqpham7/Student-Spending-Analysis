# Data Cleaning Methods

## Missing Values
- Used **Python** to check for missing values in the dataset.  
- No missing values were found.  
- Note: The dataset was large enough that some data could have been removed without compromising reliability.  

## Duplicate Values
- Used **Python** to check for duplicate entries.  
- None were found.  

## Removed Irrelevant Variables
- Removed:  
  - A blank variable column.  
  - The "preferred payment method" column (most payments were card; cash payments had no significant impact).  

## Created Flag Variables for Better Explanations
- **Major (Economics flag):**  
  - `=IF(E2="Economics", "Yes","No")`  

- **Expense Ratio:**  
  - Formula: `Total income / Total expenses`  
  - Categories:  
    - Ratio ≥ 1 → "Stable"  
    - Ratio < 1 → "Unstable"  

- **Expense Level (based on average total expense = $1795.08):**  
  - `< 1600 → "Low expense"`  
  - `1600–1900 → "Average expense"`  
  - `> 1900 → "High expense"`  

- **Debt Ratio:**  
  - Formula: `Total income / Total expenses`  
  - Categories:  
    - > 1 → "Financially stable"  
    - = 1 → "Break even"  
    - < 1 → "In debt"  

- **Financial Aid Dependency:**  
  - If financial aid > 25% of tuition → "High aid"  
  - Otherwise → "Low aid"  

- **Upperclassman Status:**  
  - `=IF(OR(D2="Junior",D2="Senior"), "Yes", "No")`  

- **Entertainment Spending (as % of monthly income):**  
  - > 10% → "High spender"  
  - ≤ 10% → "Low spender"  
