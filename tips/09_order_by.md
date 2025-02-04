This is how you ORDER_BY two columns
```python
SELECT manufacturer, ROUND(SUM(total_sales)/1000000) AS total_sales
FROM pharmacy_sales
GROUP BY manufacturer
ORDER BY total_sales DESC, manufacturer
```
