# Data-Driven Insights for Product Sales, Stock Trends, and Customer Behavior

Midterm project focused on analyzing a product inventory dataset to uncover sales, revenue, stock movement patterns, and customer-rating signals that can support better pricing and inventory decisions.

**Author:** Mithilesh Menakuru  


---

## Project Goals

This project answers practical business questions using exploratory data analysis (EDA) and visualizations:

1. **Which product categories generate the highest revenue?**
2. **Which products have the highest stock but lowest sales?**
3. **Which products show the fastest stock depletion trends over time?**
4. **How do price and customer ratings relate (if at all)?**

---

## Dataset

This project uses the below dataset:

- **Global Product Inventory Dataset 2025**  
  (Download and place the CSV as `products.csv` in the project root)

The analysis primarily works with fields like:
- Product Name, Product Category
- Price
- Stock Quantity (renamed to **Product Quantity** in the cleaned dataset)
- Manufacturing Date
- Warranty Period
- Product Ratings

---

## What’s Inside the Analysis

### 1) Data Loading & Review
- Reads `products.csv`
- Reviews dataset shape, column types, summary stats

### 2) Data Preparation (Cleaning)
- Drops non-essential columns for the analysis (e.g., Product ID, Product Description, Product Tags)
- Renames `Stock Quantity` → `Product Quantity`
- Checks missing values and duplicates
- Standardizes product category values (example: Laptop/Smartphone/Headphones/Monitor mapped into broader groups like Computing Devices, Mobile Devices, Audio Devices, Display Devices)

### 3) EDA (Exploratory Data Analysis)
Visual tools used to understand distributions, quality issues, and relationships:
- Boxplots (outlier detection): Price, Product Quantity, Warranty Period, Product Ratings
- Histograms (distributions)
- Correlation heatmap
- Pairplot for numeric relationships
- Violin plots for distribution shape and spread

### 4) Business Question Analysis
**Q1: Revenue by Category**
- Computes `Revenue = Price * Product Quantity`
- Aggregates revenue by Product Category
- Bar chart + summary table

**Q2: High Stock, Low Sales**
- Computes `Total Sales = Price * Product Quantity`
- Sorts products to highlight high quantity + low sales
- Bar chart + table output

**Q3: Stock Depletion Trends**
- Converts Manufacturing Date to datetime
- Creates `Days Since Manufacturing`
- Builds a pivot table and plots a heatmap to visualize stock movement patterns over time

---

## Key Insights (From the Notebook)

- **Stock depletion trends:** some products show consistent depletion (high demand), while others show irregular patterns (possible restocking or inconsistent supply behavior).
- **Price vs ratings:** higher-priced products can receive lower ratings, suggesting higher customer expectations.
- **Revenue concentration:** a few categories contribute the majority of revenue, which can guide prioritization.
- **High stock + low sales:** flags candidates for clearance, bundling, repositioning, or marketing pushes.

---

## Tech Stack

- Python 3.x
- pandas, numpy
- matplotlib, seaborn
- Jupyter Notebook


