---
id: d5sodtya7p4i9a7rf3vjnd1
title: Analyze Data to Answer Questions
desc: ''
updated: 1651715583032
created: 1650854824278
---

### The analysis process

The process used to make sense of the data is collected.

The goal of analysis is to identify trends and relationships within data, so you can accurately answer question you're asking.

#### The phases of analysis

1. Organize data
2. Format and adjust data
3. Get input from others
4. Transform data

### Organize data for analysis

The organization of datasets is really important for data analysts. Most of the datasets you will use will be organized as tables. Tables are helpful because they let you manipulate your data and categorize it. Having distinct categories and classifications lets you focus on, and differentiate between, your data quickly and easily.

Data analysts also need to format and adjust data when performing an analysis. **Sorting** and **filtering** are two ways you can keep things organized when you format and adjust data to work with it. For example, a filter can help you find errors or outliers, so you can fix or flag them before your analysis. **Outliers** are data points that are very different from similarly collected data and might not be reliable values. The benefit of filtering the data is that after you fix errors or identify outliers, you can remove the filter and return the data to its original organization.

![Sorting versus filtering](/assets/images/2022-04-26-07-06-10.png)


### Sort sheet

All the data in a spreadsheet is shorted by the ranking of a specific sorted column - data across rows is kept together.

### Sort range

Nothing else on the spreadsheet is arranged beside the specified cells in a column.

### Customized sort order

When you sort data in a spreadsheet using multiple conditions, you can specify the order of the sorting.

### Data Formatting

Data formatting is a process that helps you organize and format data for analysis.

In correctly formatted data can:

- Leads to mistakes
- Take time to fix
- Affect stakeholders decision-making

### Advanced spreadsheet tips and tricks

- [Keyboard shortcuts for Google Sheets - Computer - Google Docs Editors Help](https://support.google.com/docs/answer/181110): This is a great resource for quickly learning a range of keyboard shortcuts that can make regular tasks quicker and easier, like navigating your spreadsheet or accessing formulas and functions. This list contains shortcuts for the desktop and mobile versions of Google Sheets so that you can apply them to your work no matter what device you are using.
- [Google Sheets function list - Google Docs Editors Help](https://support.google.com/docs/table/25273?hl=en): This is a comprehensive list of the Google Sheets functions and syntax. Each function is listed with a link to learn more.
- [20 Google Sheets Formulas You Must Know](https://automate.io/blog/google-spreadsheet-formulas/): This blog article summarizes and describes 20 of the most useful Google Sheets formulas.
- [18 Google Sheets Formulas Tips & Techniques You Should Know](https://www.benlcollins.com/spreadsheets/google-sheets-formulas-techniques/): These are tips for using Google Sheets shortcuts when working with formulas.

### Data Aggregation

*Aggregation*: Collecting** or gathering many pieces into a while.

**Data aggregation**: The process of gathering data from multiple sources in order to combine it into a single summarized collection.

Data can also be aggregated over a given time period to provide statistics such as:

- Averages
- Minimums
- Maximums
- Sums

### VLOOKUP (Vertical Lookup)

A function that searches for a certain value in a column to return a corresponding piece of information.

```cell
=VLOOKUP(value, range, col, [exact])
```

### VALUE

A function that converts a text string that represents a number to numerical value.

```cell
=VALUE(text)
```

### Troubleshooting questions

- How should I prioritize these issues?
- In a single sentence, what's the issue I'm facing?
- What resource can help me to solve this problem?

### Understanding SQL joins

A SQL clause that is used to combine rows from two or more tables based on a related column.

There four common joins:

- Inner join
- Left join
- Right join
- Outer join (full outer join)

![Inner & Full Joins](/assets/images/2022-05-05-06-39-49.png)
![Left & Right Joins](/assets/images/2022-05-05-07-04-20.png)

### Inner join

A function that returns records with matching values in both tables.

```sql
SELECT * FROM table1 INNER JOIN table2 ON table1.column = table2.column
```

### Left join

A function that will return all the records from the left table, and only the matching records from the right table.

**Note:** The table mentioned first is left, and the table mentioned second is right.

```sql
SELECT * FROM table1 LEFT JOIN table2 ON table1.column = table2.column
```

### Right join

A function that will return all the records from the right table, and only the matching records from the left table.

```sql
SELECT * FROM table1 RIGHT JOIN table2 ON table1.column = table2.column
```

### Outer join

A function that combines `RIGHT` and `LEFT` join to return all matching records from both tables.

```sql
SELECT * FROM table1 FULL OUTER JOIN table2 ON table1.column = table2.column
```

### JOIN Reference

- [SQL Join Reference](https://www.w3schools.com/sql/sql_join.asp)
- [SQL Joins - The Ultimate Guide](https://www.essentialsql.com/introduction-database-joins/)
- [SQL Join Types Explained Visually](https://dataschool.com/how-to-teach-people-sql/sql-join-types-explained-visually/)
- [SQL JOIN - Bring Data Together](https://towardsdatascience.com/sql-join-8212e3eb9fde)
- [SQL JOIN](https://www.dofactory.com/sql/join)

### Count and Count Distinct

`COUNT`: A query that returns the number of rows in a specified range.

```sql
SELECT COUNT(*) FROM table
```

`COUNT DISTINCT`: A query that returns the number of distinct values in a specified range.

```sql
SELECT COUNT(DISTINCT column) FROM table
```

### SQL Sub-Query

`SQL SUBQUERY`: A SQL query that is nested inside a larger query.

```sql
SELECT * FROM table WHERE column IN (SELECT column FROM table)
```