# Tableau-Software-functions
### **Summary: Essential Tableau Functions**

#### **1. Text Functions**
- **`CONCAT`**: Combines two or more text values into one.  
  Example: Combine first name and last name → `CONCAT([First Name], " ", [Last Name])`.  
- **`LEFT` / `RIGHT`**: Extracts the first or last characters from text.  
  Example: Take the first 4 characters → `LEFT([Product Code], 4)`.  
- **`UPPER` / `LOWER`**: Converts text to uppercase or lowercase.  
- **`TRIM`**: Removes extra spaces from the start or end of text.  

#### **2. Aggregation Functions**
- **`SUM`**: Adds up numbers.  
  Example: Total sales → `SUM([Sales])`.  
- **`AVG`**: Finds the average of numbers.  
  Example: Average profit → `AVG([Profit])`.  
- **`MIN` / `MAX`**: Finds the smallest or largest value.  
- **`COUNT` / `COUNTD`**: Counts rows or unique values.  
  Example: Number of unique customers → `COUNTD([Customer ID])`.  

#### **3. Logical Functions**
- **`IF`**: Creates conditions.  
  Example: If sales > 10,000, show "High"; otherwise, "Low".  
  → `IF [Sales] > 10000 THEN "High" ELSE "Low" END`.  
- **`CASE`**: Works like `IF` but for multiple conditions.  
  Example:  
  ```text
  CASE [Region]
    WHEN "East" THEN "Group 1"
    WHEN "West" THEN "Group 2"
    ELSE "Other"
  END
  ```
- **`ZN`**: Replaces NULL (empty) values with 0.  

#### **4. Date Functions**
- **`DATEPART`**: Pulls out a part of a date (like year or month).  
  Example: Extract the year → `DATEPART('year', [Order Date])`.  
- **`DATEDIFF`**: Finds the difference between two dates.  
  Example: Days between order and shipping → `DATEDIFF('day', [Order Date], [Ship Date])`.  
- **`TODAY`**: Gives today’s date.  

#### **5. Table Calculation Functions**
- **`WINDOW_SUM`**: Adds numbers in a range (like rows in a table).  
  Example: Total sales in a window → `WINDOW_SUM(SUM([Sales]))`.  
- **`WINDOW_AVG`**: Finds the average in a range.  
- **`WINDOW_MAX` / `WINDOW_MIN`**: Finds the largest or smallest value in a range.  
- **`RANK`**: Ranks items by a value.  
  Example: Rank categories by sales → `RANK(SUM([Sales]))`.  
- **`RUNNING_SUM`**: Adds up values step by step (cumulative).  
  Example: Cumulative sales → `RUNNING_SUM(SUM([Sales]))`.  
- **`INDEX`**: Gives a number to each row.  
- **`LOOKUP`**: Gets a value from another row.  
  Example: Previous row’s sales → `LOOKUP(SUM([Sales]), -1)`.  

#### **6. Statistical Functions**
- **`MEDIAN`**: Finds the middle value in a group of numbers.  
- **`STDEV`**: Calculates how much numbers vary (standard deviation).  
- **`VARIANCE`**: Measures the spread of numbers.  
- **`PERCENTILE`**: Finds a value at a specific percentile.  
  Example: Value at the 90th percentile → `PERCENTILE([Sales], 0.9)`.  

#### **7. Dashboard Functions**
- **`TOTAL`**: Adds all the visible rows in the view.  
- **`WINDOW_PERCENTILE`**: Finds the percentile for a range of rows.  
- **`FIRST` / `LAST`**: Shows the first or last position of a row in a view.

# Tableau Chart Types and Their Uses  

This document provides a quick reference to common chart types in Tableau and their use cases.  

## Chart Types  

### 1. **Bar Chart**  
- **Use:** Compare categorical data side by side. Best for showing rankings, trends, or comparisons.  

### 2. **Line Chart**  
- **Use:** Analyze trends over time (e.g., sales, profits, or performance over months or years).  

### 3. **Area Chart**  
- **Use:** Similar to a line chart but emphasizes the magnitude of change over time by filling the area under the line.  

### 4. **Pie Chart**  
- **Use:** Show proportions or percentages of a whole. Best for up to 5 categories.  

### 5. **Scatter Plot**  
- **Use:** Analyze relationships between two numerical variables (e.g., sales vs. profit).  

### 6. **Histogram**  
- **Use:** Display the distribution of a single continuous variable (e.g., frequency of sales within ranges).  

### 7. **Box Plot (or Box-and-Whisker Plot)**  
- **Use:** Show the distribution and variability of data, highlighting medians, quartiles, and outliers.  

### 8. **Tree Map**  
- **Use:** Represent hierarchical data or proportions using nested rectangles.  

### 9. **Heat Map**  
- **Use:** Visualize data density or intensity across a matrix using color gradients.  

### 10. **Gantt Chart**  
- **Use:** Track schedules, timelines, or project tasks over time.  

### 11. **Bubble Chart**  
- **Use:** Visualize relationships with three variables using bubble size as an additional measure.  

### 12. **Dual-Axis Chart**  
- **Use:** Compare two measures with different axes on the same chart (e.g., sales and profit trends).  

### 13. **Map (Geographical Chart)**  
- **Use:** Display data geographically, such as sales by region or customer distribution.  

### 14. **Bullet Chart**  
- **Use:** Compare a measure against a target or benchmark.  

### 15. **Waterfall Chart**  
- **Use:** Show cumulative impacts of sequential positive and negative changes (e.g., profit contribution).  

### 16. **Funnel Chart**  
- **Use:** Represent stages in a process, often used for sales or conversion funnels.  

---

