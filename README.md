# GDP-Data-Analysis-Project
## Overview

This project focuses on cleaning, transforming, and analyzing GDP data for countries using the “List of Countries by GDP (Nominal)” dataset from Wikipedia. The dataset includes GDP estimates from IMF, World Bank, and the United Nations, providing multiple perspectives on country-level economic data.

The project demonstrates Power Query data cleaning, data transformation, and comparative analysis to generate meaningful insights.

## Dataset

- Source: Wikipedia – [List of countries by GDP (Nominal)](https://en.wikipedia.org/wiki/List_of_countries_by_GDP_(nominal)?utm_source=chatgpt.com)

- Key columns:

  * Country/Territory

  * IMF_GDP

  * WorldBank_GDP

  * UN_GDP

  * Additional metadata (rankings, year, etc.)

## Analysis & Insights

- Compared GDP estimates across IMF, World Bank, and UN.

- Highlighted countries with largest discrepancies between sources.

- Calculated average GDP to reduce source bias.

 
## Visuals / Screenshots 
### 1. Original vs Cleaned Country Names
 
| Original            | Cleaned       |
| ------------------- | ------------- |
| United States [n 1] | United States |
| China [n 2]         | China         |
| Finland             | Finland       |

### 2. GDP Comparison Chart
<img width="731" height="442" alt="image" src="https://github.com/user-attachments/assets/5e299b3b-737e-4592-81c7-29b222cbeef5" />

### 3. Share of Global GDP
<img width="736" height="445" alt="image" src="https://github.com/user-attachments/assets/873b283c-ee74-4ded-9e55-2ca388c8e448" />


### 4. Derived Columns Table
| Country | IMF_GDP | WorldBank_GDP | UN_GDP | GDP_Diff_IMF_WB | GDP_PercentDiff_IMF_WB | Average_GDP |
| ------- | ------- | ------------- | ------ | --------------- | ---------------------- | ----------- |
| USA     | $30,615,743.00 | $29,184,890.00  | $27,720,700.00  | 1430853          | 5%                    | $29,173,777.67    |
| China   | $19,398,577.00 | $18,743,803.00  | $17,794,782.00  | 654774       | 3%                   | $18,645,720.67    |


## Tools & Technologies

- **Microsoft Power Query** – Data cleaning, transformations, calculated columns

- **Power Query UI** – Footnote removal without code

- **Excel / Power BI Visuals** – Bar charts, tables, and KPI dashboards

## Challenge

The Country/Territory column contained footnotes like [n 1], [n 2], etc., which interfered with sorting, merging with other datasets, and calculations.

### Problem: 
Removing footnotes without deleting valid characters (like “n” in Finland) and without regex support in Power Query.

### Solution:

Used Power Query UI:

- Split column by '[' delimiter

- Kept only the first part (removing footnotes)

- Trimmed extra whitespace

## How to Use

1. Clone this repository:
```git clone https://github.com/yourusername/gdp-data-analysis.git```

2. Open the Power BI or Excel file.

3. Load the Wikipedia GDP table via Power Query.

4. Apply the transformation steps to clean the Country/Territory column.

5. Explore derived columns for analysis or modify the dashboard as needed.

## Lessons Learned

- Handling messy real-world data requires creative problem solving when some functions aren’t available.

- Splitting columns by delimiters can remove unwanted patterns while preserving valid data.

- Comparing multiple sources reveals data inconsistencies that can affect analysis.

## Discussion / Contribution

Open for discussion:

- Alternative methods for removing footnotes/reference tags

- Ideas for additional derived metrics

- Suggestions for improving visualizations or dashboards

**Feel free to fork this repository, submit issues, or contribute enhancements!**

