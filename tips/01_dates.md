Suppose you want to filter data for the year 2022, then the query should be below.</br>
Remember the order of year, month & date will be 'year-month-date'
```python
SELECT * FROM tweets
WHERE tweet_date BETWEEN '2022-01-01' AND '2022-12-31'
```
