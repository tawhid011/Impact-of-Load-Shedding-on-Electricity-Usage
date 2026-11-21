# Impact of Load Shedding on Electricity Usage

A statistical analysis of how load shedding (scheduled power cuts) changes household electricity consumption **before, during and after** outages, using a dataset of 7,500 records.

## Question

Does load shedding change how much electricity households use, and does the effect depend on area type or income level?

## Dataset

`load_shedding_7500_rows.json` has one row per household and period, with these columns:

| Column | Meaning |
|---|---|
| `Household_ID` | household identifier |
| `Area_Type` | e.g. Semi-Urban |
| `Family_Size`, `Appliance_Count` | household characteristics |
| `Income_Level` | income group |
| `Backup_Type` | backup power (e.g. IPS) |
| `Load_Shedding_Status` | `Before`, `During` or `After` |
| `Outage_Hours`, `Temperature_C`, `Day_Index` | conditions on that day |
| `Electricity_Usage_kWh` | outcome variable |

## Methods

The notebook `Impact_of_Load_Shedding_on_Electricity_Usage.ipynb` walks through:

1. Data overview and summary statistics by period
2. One-way ANOVA (does usage differ across periods?)
3. Two-way ANOVA (area type × period interaction)
4. Tukey HSD pairwise comparisons and Cohen's d effect sizes
5. Regression with household and weather controls
6. Subgroup analysis by area type and income level
7. Visualisations: bar plot, histogram, box plot, reduction by income, correlation heatmap, time-series scatter

## Run it

```bash
pip install pandas numpy scipy statsmodels seaborn matplotlib tabulate jupyter
jupyter notebook Impact_of_Load_Shedding_on_Electricity_Usage.ipynb
```

Keep the JSON file in the same folder as the notebook.

## Tools

Python, pandas, SciPy, statsmodels, seaborn, matplotlib

## Author

Tawhid Hossain, [@tawhid011](https://github.com/tawhid011)
