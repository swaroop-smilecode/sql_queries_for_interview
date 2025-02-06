------------------------------------------------
#### Filtering query based on date range
Remember the order of year, month & date will be 'year-month-date'
```python
SELECT * FROM tweets
WHERE tweet_date BETWEEN '2022-01-01' AND '2022-12-31'
```
------------------------------------------------
#### Filtering query based on date range. For example, below query is filtering the data between july to september.
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
#### Adding 1 day to time stamp
`INTERVAL '1 day'`
```python
SELECT DISTINCT e.user_id
FROM emails e
JOIN texts t
ON e.email_id = t.email_id
WHERE t.action_date = e.signup_date + INTERVAL '1 day'
  AND t.signup_action = 'Confirmed';
```
------------------------------------------------
#### Extracting month from time stamp
```python
SELECT EXTRACT(MONTH FROM time_stamp) mth
FROM reviews
```
