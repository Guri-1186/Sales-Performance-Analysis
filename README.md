# My First Data Analysis Project: Retail Sales Analysis

## About This Project

This is my first complete data analysis project! As a junior data analyst, I wanted to practice working with real-world retail data to learn data cleaning, analysis, and finding business insights.

**What I analyzed:** Online retail sales data to understand customer behavior and product performance.

## Skills I Learned & Used

- **Data Cleaning**: Handling missing values, duplicates, and invalid data
- **Python/Pandas**: Data manipulation and analysis
- **Problem Solving**: Identifying and fixing data quality issues
- **Business Analysis**: Finding actionable insights from data

## The Dataset

I worked with an Online Retail Dataset from the UCI Machine Learning Repository:

- **Size**: 25,000 transactions
- **Time Period**: Historical retail sales data
- **Columns**: 8 main fields including customer info, products, prices, and dates

### What the data looked like:

| Column      | What it means        | Example               |
| ----------- | -------------------- | --------------------- |
| InvoiceNo   | Receipt number       | 536365                |
| StockCode   | Product ID           | 85123A                |
| Description | Product name         | "White Hanging Heart" |
| Quantity    | Items bought         | 6                     |
| InvoiceDate | When purchased       | 2010-12-01 08:26:00   |
| UnitPrice   | Price per item       | £2.55                 |
| CustomerID  | Customer number      | 17850                 |
| Country     | Where customer lives | United Kingdom        |

## Problems I Found (Data Quality Issues)

When I first looked at the data, I found several problems that needed fixing:

| Problem                     | How Many         | Why It's Bad                  |
| --------------------------- | ---------------- | ----------------------------- |
| Missing Customer IDs        | 8,944 rows (36%) | Can't track customer behavior |
| Returns/Negative quantities | 464 rows         | Messes up sales totals        |
| Missing product names       | 111 rows         | Don't know what was sold      |
| Duplicate records           | 352 rows         | Counts sales twice            |
| Zero prices                 | Some rows        | Products can't be free        |

## How I Cleaned the Data

This was the hardest part! Here's what I did step by step:

1. **Removed returns**: Deleted 464 rows with negative quantities
2. **Fixed missing product names**: Changed blanks to "Unknown Product"
3. **Handled missing customers**: Used "GUEST_CUSTOMER" for missing IDs
4. **Removed duplicates**: Found and deleted 343 duplicate rows
5. **Fixed pricing issues**: Removed rows where price was £0 or negative
6. **Saved clean data**: Created a new file called `sales_clean.csv`

**Final result**: 24,078 clean transactions ready for analysis!

## What I Discovered

### Best Selling Products

**Top Revenue Winner**: REGENCY CAKESTAND 3 TIER (£17,062!)

- This was surprising - it's expensive but people really want it
- Taught me that high price doesn't always mean low sales

**Most Consistent Seller**: WHITE HANGING HEART T-LIGHT HOLDER

- Appeared in both "most sold" and "highest revenue" lists
- Shows this is a reliable product customers love

**Pattern I noticed**: Home decoration items sell really well, especially gift-type products

### Customer Insights

I learned that customers fall into different groups:

- **Regular Customers (72%)**: Buy occasionally, normal amounts
- **Gold Customers (11%)**: Buy often AND spend a lot (the best customers!)
- **High Spenders (9%)**: Spend lots but don't buy often
- **Frequent Buyers (8%)**: Buy often but spend little each time

**Key insight**: Just 20% of customers (Gold + High Spenders) make most of the money for the business!

### Pricing Patterns

- Most products (70%+) cost less than £5
- Average price: £5.01
- But half of all products cost £2.55 or less
- Very few expensive items (over £100)

This tells me the store focuses on affordable items that many people can buy.

## Challenges I Overcame

- **Missing data everywhere**: Learned that real data is messy!
- **Deciding what to do with problems**: Keep or delete? Fill in or leave blank?
- **Understanding business context**: What do negative quantities mean? (Returns!)
- **Making sense of patterns**: Why do some products sell better than others?

## Tools I Used

- **Python**: For all the data work
- **Pandas**: To clean and analyze the data
- **Basic statistics**: To find averages, counts, and patterns
