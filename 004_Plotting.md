# Plotting with Pandas

Pandas has a built-in plotting library that can be used to plot dataframes and series. The plotting library is built on top of matplotlib.

## Plotting Series
```python
df['job_posted_date'] = pd.to_datetime(df['job_posted_date'])

job_counts = df.job_title_short.value_counts()

job_counts = df.job_title_short.value_counts()

job_counts.plot(kind='bar') #pandas.series.plot() can be used to plot for series values and pandas.Dataframe.plot() can be used to plot entire dataframe with x, y and kind values provided

plt.show()
```

## Plotting DataFrames
```python
df.plot(x='job_posted_date', y='job_title_short', kind='bar')
```



