# Analyzing Data in Pandas

This guide provides an overview of some common aggregate functions used in pandas for data analysis. Below are examples demonstrating how to apply these functions on a DataFrame `df`.

```python
df.describe() # will give some of the aggregate functions results as a result 
# There are many aggregate functions, but we will cover some here.

df.count() # count will give the number of values present in each column.

df.salary_year_avg.median() # will give the median for numerical columns.

df.salary_year_avg.min() # will give the minimum value in the column.

df.salary_year_avg.idxmin() # will give the index value for the minimum value in that column.

df.job_title_short.value_counts() # will count and give how many people are in each position.

df.groupby('job_title_short')['salary_year_avg'].min() # groupby is used to combine columns, and aggregate functions can be used on numerical columns (should be inside a list).
# Syntax for groupby:
# df.groupby(["list of columns to be grouped"])['list of columns to aggregate'].aggregate_function

df.groupby('job_title_short')[['salary_year_avg', 'salary_hour_avg']].median() # groupby with multiple aggregated columns.

df.groupby('job_title_short')['salary_year_avg'].agg(['min', 'median']) # agg is used to apply multiple aggregate functions to a column.
```
