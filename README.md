# Amazon Product Data Analysis (Microsoft Excel)

This project is a comprehensive analysis of Amazon product data using **Microsoft Excel**. The goal is to uncover insights related to pricing, discounts, ratings, and customer engagement by leveraging **data cleaning**, **pivot tables**, **charts**, and **formulas**.



---

## Objectives

1. Clean and transform the dataset for analysis.
2. Derive insights using pivot tables, calculated columns, and charts.
3. Visualize relationships between key variables like rating and discount.
4. Answer 14 key business questions based on the dataset.

---

## Data Cleaning Steps

Performed in Excel before analysis:

- Removed symbols like `₹` and `%` from numeric fields.
- Converted `actual_price`, `discounted_price`, `rating`, and `rating_count` to numeric types.
- Extracted **main_category** from multi-level category fields.
- Created **price_bucket** column based on `actual_price`:
  - `<200`, `200–500`, and `>500`
- Created **potential_revenue** = `actual_price × rating_count`
- Ensured data is inside an Excel Table (`Ctrl + T`) for dynamic PivotTables.

---

## Key Analytical Tasks & How They Were Done

| Question | Method |
|---------|--------|
| 1. Average discount % by category | PivotTable (Average of `discount_percentage` by `main_category`) |
| 2. Number of products per category | PivotTable (Count of `product_id` by `main_category`) |
| 3. Total reviews per category | PivotTable (Sum of `rating_count` by `main_category`) |
| 4. Top products by average rating | PivotTable (Average `rating` by `product_name`, sorted) |
| 5. Avg actual vs discounted price | PivotTable (Avg `actual_price` & `discounted_price` by category) |
| 6. Top products by number of reviews | PivotTable (Sum of `rating_count` by `product_name`, sorted) |
| 7. Products with 50%+ discount | Helper column + PivotTable (Count of `discount ≥ 50%`) |
| 8. Rating distribution | New column `Rounded_Rating` + PivotTable (Count by rounded values) |
| 9. Potential revenue by category | PivotTable (Sum of `potential_revenue` by `main_category`) |
| 10. Product count by price range | PivotTable (Count by `price_bucket`) |
| 11. Rating vs Discount | Scatter Plot (Rating vs `discount_percentage`) |
| 12. Products with <1000 reviews | COUNTIF or filter on `rating_count` |
| 13. Highest discounts by category | PivotTable (Avg `discount_percentage` sorted descending) |
| 14. Top 5 products by combined rating & reviews | New score = `rating × log10(review_count + 1)` |

---

## Tools & Features Used

- Microsoft Excel 2016+
- Excel Tables (`Ctrl + T`)
- PivotTables
- Formulas (`IF`, `LEFT`, `FIND`, `LOG10`, `ROUND`, `COUNTIF`)
- Charts: Scatter plot, column chart, bar chart
- Conditional formatting & data filtering

---

## Key Learnings

- Data cleaning is critical for accurate insights.
- PivotTables are powerful for summarizing complex datasets.
- Visualizing relationships (e.g., rating vs discount) helps identify patterns.
- Excel formulas can be combined for custom metrics like potential revenue or hybrid ranking.

---

## Author

**Student:** *[Samuel Adebiyi Ibukun]*  
**Institution:** *[Digital Skill Africa(DSA)]*  
**Course:** Data Analysis

---

## License

This project is for educational purposes and personal learning.  
Feel free to fork or adapt for your own coursework.

