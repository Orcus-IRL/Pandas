
# Inspecting in pandas

```python
df = load_dataset("lukebarousse/data_jobs") # loading the dataset
df # will show first 5 and last 5 rows
df.head(10) # will show first specified rows of 10 rows by default
df.tail(10) # will show last specified rows of 10 rows by default
df["job_title_short"] # to view one column
df[["job_title_short", "job_title"]] # a list is used to view multiple columns
df.iloc[90:101, 0:2] # used to return specific or range of rows(first param) and the numbers of columns (second param)
df[["job_title_short","job_title"]].iloc[90:101] # same thing but columns are specific too
#df.info() # to get info about dataset
df.describe() # will give count, mean, std, min, max, 25%, 75% for only the numerical columns(ie: int or float Dtype)
df.job_title_short.unique() # will give unique elements in that specific column
df.job_title_short == "Data Analyst" # will return boolean value if it matches the condition
df[df.job_title_short == "Data Analyst"] # putting that to the list will give the table with the matching role 

df[(df.job_title_short == "Data Analyst") & (df.salary_year_avg > 100000)] # more conditions can be given but the only symbols(&,|,!) can be used  
df[(df.job_title_short == "Data Analyst") & (df.salary_year_avg.notna())] # same example but with notna --> will give only the rows that don't have NaN in it.
```
