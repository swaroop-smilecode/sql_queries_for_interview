This is how you ORDER_BY two columns
```python
SELECT manufacturer, ROUND(SUM(total_sales)/1000000) AS sum_total_sales
FROM pharmacy_sales
GROUP BY manufacturer
ORDER BY sum_total_sales DESC, manufacturer
```
