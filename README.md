# Video Game Sales Dashboard (Power BI)

##  Objective
Build an interactive dashboard using Power BI to analyze global video game sales and uncover business insights for stakeholders.

## Dataset
- File: `vgsales.csv`
- Source: [Kaggle](https://www.kaggle.com/datasets/gregorut/videogame-sales-with-ratings)

## Tools
- Power BI Desktop

## Steps to Build the Dashboard

### 1. Load and Clean the Data
1. Open Power BI Desktop.
2. Go to **Home → Get Data → Text/CSV** and load `vgsales.csv`.
3. Click **Transform Data** to open Power Query Editor.
4. **Remove Unnecessary Columns**:
   - Keep only the following:
     - `Name` (Game title)
     - `Platform`
     - `Year`
     - `Genre`
     - `Publisher`
     - `Global_Sales`
   - Remove:
     - `NA_Sales`, `EU_Sales`, `JP_Sales`, `Other_Sales`

### 2. Create New Measures / KPIs
Under the **Modeling** tab, create the following DAX measures:

- **Total Global Sales**:
  ```DAX
  Total Sales = SUM(vgsales[Global_Sales])
