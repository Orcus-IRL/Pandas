
# Cleaning Data using pandas

```python
df['job_posted_date'] = pd.to_datetime(df['job_posted_date']) # to convert str to datetime datatype and also don't use dot notation when assigning

df['job_posted_month'] = df['job_posted_date'].dt.month # created a new column and assigned the month to it 

df.sort_values(by='job_posted_date') # used to sort based on a column ('by' keyword is used)

df.sort_values(by='job_posted_date', inplace=True) # the changes will be affected in the original df as well when inplace=True

df.drop(labels='salary_hour_avg', axis=1, inplace=True) # to delete something that is specified, in this case a column (axis=1) and that column name

df.dropna(axis=0, subset=['salary_year_avg'], inplace=True) # to remove all the NaN values in that column and remove rows (axis=0) as well. The columns are given in a list with keyword argument 'subset'

```

