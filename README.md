# Fashion Trend Intelligence Dashboard

## Understanding What Consumers Want Using Power BI

---

## Project Overview

This project analyzes a synthetic fashion sales dataset to understand product performance, consumer purchasing patterns, seasonal trends, and revenue drivers.

An interactive Power BI dashboard was created to explore revenue and sales performance across categories, products, brands, genders, seasons, colors, regions, ratings, and discounts.

> **Note:** The dataset used in this project is synthetic and was created for educational and portfolio purposes.

---

## Business Objective

The objective of this project is to:

- Identify the highest-performing fashion categories and products
- Analyze revenue across different seasons and genders
- Understand brand and color performance
- Examine the relationship between product ratings and revenue
- Analyze revenue trends over time
- Explore revenue across different discount levels
- Build an interactive dashboard for exploring sales performance

---

## Dataset

The dataset contains 96 sales records and 12 columns.

### Columns

| Column | Description |
|---|---|
| Date | Date of the sales record |
| Product | Fashion product name |
| Category | Product category |
| Gender | Target gender |
| Brand | Product brand |
| Color | Product color |
| Season | Fashion season |
| Price | Product price |
| Units Sold | Number of units sold |
| Discount % | Discount percentage |
| Rating | Product rating |
| Region | Sales region |

Revenue was not directly included in the dataset. It was calculated in Power BI using:

**Revenue = Price × Units Sold**

---

## Tools & Technologies

- Microsoft Excel
- Power Query
- Microsoft Power BI
- DAX
- Data Visualization
- Dashboard Design

---

## Data Preparation

The dataset was imported into Power BI from Excel.

Power Query was used to:

- Review the dataset structure
- Check and correct data types
- Prepare the data for analysis
- Load the prepared data into Power BI

---

## DAX Measures

Several DAX measures were created to support the analysis.

### Total Revenue

```DAX
Total Revenue =
SUMX(
    'Fashion Sales',
    'Fashion Sales'[Price] * 'Fashion Sales'[Units Sold]
)

### Total Units Sold

Total Units Sold =
SUM('Fashion Sales'[Units Sold])

### Average Rating 

Average Rating =
AVERAGE('Fashion Sales'[Rating])

### Average Selling Price

Average Selling Price =
AVERAGE('Fashion Sales'[Price])

### Product Count

Product Count =
DISTINCTCOUNT('Fashion Sales'[Product])

### Total Discount Amount

Total Discount Amount =
SUMX(
    'Fashion Sales',
    'Fashion Sales'[Price] *
    'Fashion Sales'[Units Sold] *
    'Fashion Sales'[Discount %] / 100
)

Dashboard Features

The dashboard includes:

-Total Revenue KPI
-Total Units Sold KPI
-Average Rating KPI
-Average Selling Price KPI
-Revenue by Category
-Revenue by Season
-Revenue by Gender
-Revenue by Brand
-Top Products by Revenue
-Revenue Trend Over Time
-Revenue by Color
-Rating vs Revenue
-Revenue by Discount
-Interactive slicers for Gender, Season, Category, and Region
-Key Insights

Based on the synthetic dataset:

-Footwear generated the highest revenue among the categories.
-Floral Summer Dress was the top product by revenue.
-Spring was the highest-revenue season.
-Black generated the highest revenue among the colors.
-Women generated the highest revenue among the gender segments.

These findings represent patterns in the synthetic dataset and should not be interpreted as real-world fashion market trends.

Skills Demonstrated

* Data cleaning and preparation using Power Query
* Data analysis using Power BI
* DAX measure creation
* KPI development
* Data visualization
* Interactive dashboard design
* Business-oriented data analysis
* Extracting insights from sales data

Project Files

*Fashion_Trend_Analytics.xlsx – Source dataset
*Fashion_Trend_Analytics.pbix – Power BI dashboard
*README.md – Project documentation

Note:

This project uses a synthetic dataset created for educational and portfolio purposes. The analysis demonstrates Power BI, Power Query, DAX, and data visualization skills rather than representing actual fashion industry data.