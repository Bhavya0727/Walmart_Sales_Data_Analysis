# Walmart_Sales_Data_Analysis
## About
This project involves analyzing Walmart's sales data to identify high-performing branches and products, understand sales patterns, and gain insights into customer behavior. The primary goal is to optimize sales strategies based on data-driven findings.

The dataset utilized in this project is sourced from the Kaggle Walmart Sales Forecasting Competition.

---

## **Purposes of the Project**
The main objective is to explore and analyze various factors influencing sales across different Walmart branches, products, and customer segments.

---

## **About the Data**
The dataset was obtained from the Kaggle Walmart Sales Forecasting Competition. It includes sales transactions from three Walmart branches located in Mandalay, Yangon, and Naypyitaw. The dataset comprises 17 columns and 1000 rows.

### **Column Descriptions**
| Column             | Description                                  | Data Type         |
|--------------------|----------------------------------------------|-------------------|
| `invoice_id`       | Invoice of the sales made                   | `VARCHAR(30)`     |
| `branch`           | Branch at which sales were made             | `VARCHAR(5)`      |
| `city`             | The location of the branch                  | `VARCHAR(30)`     |
| `customer_type`    | The type of the customer                    | `VARCHAR(30)`     |
| `gender`           | Gender of the customer                      | `VARCHAR(10)`     |
| `product_line`     | Product line of the product sold            | `VARCHAR(100)`    |
| `unit_price`       | Price of each product                       | `DECIMAL(10, 2)`  |
| `quantity`         | Amount of the product sold                  | `INT`             |
| `VAT`              | Tax amount on the purchase                  | `FLOAT(6, 4)`     |
| `total`            | Total cost of the purchase                  | `DECIMAL(12, 4)`  |
| `date`             | Date of the purchase                        | `DATETIME`        |
| `time`             | Time of the purchase                        | `TIME`            |
| `payment`          | Total amount paid                           | `DECIMAL(10, 2)`  |
| `cogs`             | Cost Of Goods Sold                          | `DECIMAL(10, 2)`  |
| `gross_margin_pct` | Gross margin percentage                     | `FLOAT(11, 9)`    |
| `gross_income`     | Gross Income                                | `DECIMAL(12, 4)`  |
| `rating`           | Rating                                      | `FLOAT(2, 1)`     |

---

## **Analysis List**
The project is divided into three major analysis areas:

1. **Product Analysis**:
   - Evaluate product performance across various product lines.
   - Identify top-performing and underperforming product categories.
   - Determine revenue and VAT contributions by product line.

2. **Sales Analysis**:
   - Understand sales trends across time, branches, and customer types.
   - Analyze the efficiency of applied sales strategies.

3. **Customer Analysis**:
   - Segment customers based on purchasing trends.
   - Analyze profitability and customer preferences by segment.

---

## **Approach Used**
# Data Wrangling, Feature Engineering, and Exploratory Data Analysis (EDA)

## 1. Data Wrangling

During this initial phase, the data is examined to detect any NULL or missing values. Strategies for data replacement are implemented to address and substitute these values effectively.

### Steps:
1. **Build a Database**:
   - Create a table and insert the data into it.
   - Use `NOT NULL` constraints for each field to filter out any null values effectively.

2. **Detect NULL Values**:
   - Select columns with null values in them (if any) and handle them appropriately.
   - Since `NOT NULL` constraints are applied, the dataset is free from null values.

---

## 2. Feature Engineering

Feature engineering is used to generate new columns from the existing data to extract more meaningful insights.

### Steps:
1. **Add a `time_of_day` Column**:
   - Categorize sales as occurring in the Morning, Afternoon, or Evening.
   - Insight: Identify which part of the day records the highest sales.

2. **Add a `day_name` Column**:
   - Extract the day of the week (e.g., Mon, Tue, Wed) from the transaction date.
   - Insight: Determine the busiest days for each branch.

3. **Add a `month_name` Column**:
   - Extract the month (e.g., Jan, Feb, Mar) from the transaction date.
   - Insight: Identify which months record the highest sales and profit.

---

## 3. Exploratory Data Analysis (EDA)

Exploratory Data Analysis is essential for addressing the project's objectives and answering key business questions.

---

### **Business Questions to Answer**

#### **Generic Questions**
- How many distinct cities are present in the dataset?
- In which city is each branch located?

---

### **Product Analysis**
1. How many distinct product lines are there in the dataset?
2. What is the most common payment method?
3. What is the most selling product line?
4. What is the total revenue by month?
5. Which month recorded the highest Cost of Goods Sold (COGS)?
6. Which product line generated the highest revenue?
7. Which city has the highest revenue?
8. Which product line incurred the highest VAT?
9. Retrieve each product line and add a column `product_category`, indicating "Good" or "Bad" based on whether its sales are above the average.
10. Which branch sold more products than the average number of products sold?
11. What is the most common product line by gender?
12. What is the average rating of each product line?

---

### **Sales Analysis**
1. Number of sales made in each time of the day per weekday.
2. Identify the customer type that generates the highest revenue.
3. Which city has the largest tax percentage/VAT (Value Added Tax)?
4. Which customer type pays the most VAT?

---

### **Customer Analysis**
1. How many unique customer types are in the data?
2. How many unique payment methods are in the data?
3. Which is the most common customer type?
4. Which customer type buys the most?
5. What is the gender distribution of customers?
6. What is the gender distribution per branch?
7. Which time of the day do customers give the most ratings?
8. Which time of the day do customers give the most ratings per branch?
9. Which day of the week has the best average ratings?
10. Which day of the week has the best average ratings per branch?

---

This structured approach ensures thorough analysis, enabling data-driven insights to optimize Walmart's sales strategies and understand customer behavior effectively.
