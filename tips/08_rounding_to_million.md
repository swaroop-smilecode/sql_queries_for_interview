Suppose you have below query.
```python
SELECT manufacturer, SUM(total_sales) AS total_sales
FROM pharmacy_sales
GROUP BY manufacturer
ORDER BY total_sales DESC
```

You want to round up `total_sales` by million(1000000). Then,
```python
SELECT manufacturer, ROUND(SUM(total_sales)/1000000) AS total_sales
FROM pharmacy_sales
GROUP BY manufacturer
ORDER BY total_sales DESC
```
