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
