# 📊 Power BI Sales Dashboard

An interactive, insight-driven dashboard created in Power BI to explore and analyse sales performance across different product categories, regions, customer segments, and periods.

---

## 💼 Business Case Summary

This project simulates a retail company's business scenario, aiming to understand its sales trends and regional performance better. The objective was to build a reporting solution that allows business users to answer questions such as:

- Which product categories are generating the most revenue?
- How does sales performance vary across customer segments and regions?
- What seasonal trends can be observed across years?
- Are discounts impacting profit margins?

---

## 🔗 Dataset Source

> [Superstore Dataset on Kaggle](https://www.kaggle.com/datasets/vivek468/superstore-dataset-final)

The dataset contains detailed transactional data, including product information, sales, profit, shipping dates, discounts, and customer segmentation across regions and states.

---

## 🧼 Data Cleaning & Preparation (Power Query)

Before creating visuals, the raw data was thoroughly cleaned and pre-processed in Power Query:

- **Text Standardisation**: Applied `Trim` and `Clean` functions to remove unwanted whitespace and invisible characters in fields like region and category names.
- **Duplicate Removal**: Identified and eliminated duplicate rows to ensure accurate aggregations.
- **Column Renaming**: Renamed fields for better readability (e.g., `orderdate` → `Order Date`).
- **Data Type Corrections**: Ensured columns were set to the correct types (e.g., date, currency, whole number).
- **Currency Localisation**: Converted all financial fields from USD to AUD, formatting for regional consistency.
- **Filtering**: Removed placeholder or irrelevant rows for clarity and performance.

---

## 📅 Handling Date Format Issues

One key challenge involved the **Order Date column**, which was in US format (`MM/DD/YYYY`). This created inconsistencies in time-based analysis.

To address this:

- A **new calculated column** was created using DAX to correctly parse the date into the **Australian format (`DD/MM/YYYY`)**.
- This ensured that slicers, time-series charts, and year-based filtering functioned correctly across all visuals.

---

## 🧠 DAX Calculations

The report uses DAX to build dynamic, context-aware metrics and aggregations:

- `Total Sales` and `Total Profit` as headline KPIs
- Time-based filtering using calculated year fields from `Order Date`
- Logic for removing filters across visuals to support cross-category comparisons using `REMOVEFILTERS()` and `CALCULATE()`
- Quick Measures for % of total sales and average discount

---

## 🎨 Dashboard Design

Designed for clarity and usability, the report follows best practices in business dashboarding:

- Visual hierarchy: KPIs at the top, followed by breakdowns by segment, region, and time
- Custom category colours applied to key visuals
- Slicers for **Year**, **Category**, and **Region** to enable user-driven exploration
- Consistent use of layout spacing and clean labelling for professional readability

### Visuals Included:
- Pie Chart: Sales by Category  
- Bar Charts: Sales by Segment, Region, and State  
- Column Chart: Monthly Sales Trends  
- Matrix + Bars: Discount by Subcategory

---

## 🛠 Tools Used

- Power BI Desktop  
- Power Query  
- DAX  

---

## 📁 Project Files

| File                      | Description                             |
|---------------------------|-----------------------------------------|
| `SalesDashboard.pbix`     | Fully interactive Power BI report       |
| `SalesDashboard.pdf`      | Exported static version                 |
| `dashboard-screenshot.png`| Image preview of final dashboard        |
| `README.md`               | Project documentation                   |

---

## 👩‍💼 About Me

Hi, I’m Nicolle — a Master of Business Information Systems graduate based in Australia, with a background in marketing and a growing expertise in data analytics and visual communication. I build data projects that prioritise both functionality and clarity, helping businesses understand their numbers and take action.

---

> _“A strong dashboard doesn’t just show data — it reveals insight.”_
