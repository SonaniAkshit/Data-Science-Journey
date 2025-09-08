# **Step 3: Data Preprocessing & Visualization**

📺 **Resources:**

* [NumPy Tutorial (YouTube)](https://www.youtube.com/watch?v=Utgwk0r9Zq4&t=365s)
* [Pandas Tutorial (YouTube)](https://www.youtube.com/watch?v=QUaSmqBeR9w)
* [Data Visualization Full Course (YouTube)](https://www.youtube.com/watch?v=-jTD74eEy2I&t=5057s)

---

### Topics to Cover

* **Data Cleaning**

  * Missing values (drop, fill, impute)
  * Outliers (IQR, Z-score methods)
  * Encoding categorical variables (Label, One-Hot)
  * Feature scaling (Min-Max, Standardization)

* **Working with DataFrames**

  * Reading/writing data
  * Aggregations (`groupby`, `agg`, `pivot_table`)
  * Joins & merges

* **Data Visualization**

  * matplotlib basics (Line, Bar, Scatter, Pie)
  * seaborn (Heatmaps, Boxplots, Pairplots)
  * Exploratory Data Analysis (EDA): trends, patterns, insights

---

### **Practice Questions**

---

#### Data Cleaning

1. Count how many missing values are in a DataFrame.
2. Show which values are missing in a DataFrame (True/False mask).
3. Remove all rows with missing values.
4. Fill missing values in a column with `0`.
5. Fill missing values in a column with `"Not Available"`.
6. Print the maximum and minimum value of a column.
7. Find values in a column greater than 100.
8. Replace all values greater than 100 with 100.
9. Sort a column to check for extreme values.
10. Remove the highest value from a numeric column.
11. Convert a column `"Gender"` with Male/Female into 0/1.
12. Create separate columns for each city from a `"City"` column (One-Hot Encoding).
13. Count how many times each category appears in a column.
14. Change all values in a column to lowercase.
15. Divide all values in a numeric column by 100.
16. Subtract the minimum value from each element in a numeric column.
17. Normalize a numeric column manually to range 0–1.
18. Show the mean and standard deviation of a numeric column.
19. Subtract the column mean from each value (basic standardization).
20. Round all values in a numeric column to 2 decimals.

---

#### Pandas + NumPy (Data Handling)

1. Create a DataFrame of 5 students with columns: Name, Age, Marks.
2. Display the first 3 rows and last 2 rows.
3. Show the shape (rows × columns) of the DataFrame.
4. Access only the `"Name"` column.
5. Filter all rows where Marks > 50.
6. Add a new column `"Result"` with values: Pass/Fail.
7. Update the Marks of the first student to 95.
8. Delete the `"Result"` column.
9. Sort the DataFrame by Marks in descending order.
10. Count the number of unique names.
11. Create a DataFrame of Sales with columns: Region, Product, Sales.
12. Calculate the total sales.
13. Calculate the average sales per product.
14. Count how many times each product appears.
15. Find max and min sales per region using `groupby`.
16. Create a pivot table showing total sales per Region vs Product.
17. Create a pivot table showing average sales per Region.
18. Create a NumPy array of numbers 1–10.
19. Find the sum, mean, and std of the array.
20. Reshape numbers 1–12 into a 3×4 matrix.
21. Create a 2D NumPy array of random integers (3×3).
22. Find the sum of each row and each column.
23. Multiply two 3×3 matrices.
24. Find max and min in an array and their indices.
25. Slice a NumPy array to get only even numbers.

---

#### Data Visualization (Matplotlib & Seaborn)

1. Create a dataset with columns → Products, Regions, Sales, Profit (10 rows).
2. Plot a line chart of Sales for all 10 rows (index as X-axis).
3. Plot a bar chart showing total sales for each product.
4. Plot a scatter plot of Sales vs Profit.
5. Create a pie chart showing total sales by region.
6. Plot a histogram of the Sales column.
7. Create a boxplot of Profit to detect outliers.
8. Create a countplot showing how many products are sold in each region.
9. Create a heatmap showing correlation between Sales and Profit.
10. Show total and average sales per region using pandas.

---

✅ That completes **Step 3: Data Preprocessing & Visualization**.