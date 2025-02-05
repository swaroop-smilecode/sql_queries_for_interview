------------------------------------------------
Suppose you want to filter data for the year 2022, then the query should be below.</br>
Remember the order of year, month & date will be 'year-month-date'
```python
SELECT * FROM tweets
WHERE tweet_date BETWEEN '2022-01-01' AND '2022-12-31'
```
------------------------------------------------
Suppose you have to filter query based on date range. For example, below query is filtering the data between july to september.
```python
SELECT
  employee_id,
  COUNT(DISTINCT query_id) AS unique_queries_count
FROM queries
WHERE query_starttime >= '2023-07-01'
  AND query_starttime < '2023-10-01'
GROUP BY employee_id;
```
------------------------------------------------
