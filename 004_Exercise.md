# Exercise: Data Filtering and Aggregation with Pandas

```python
import pandas as pd

# Assuming df is your DataFrame

df = df[df['job_country'] == "India"]

df = df[df['salary_year_avg'].notna()]

df.groupby('job_title_short')['salary_year_avg'].agg(['median', 'min', 'max', 'count']).sort_values(by='median', ascending=False)
```

