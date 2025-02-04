Suppose you have below query
```python
SELECT manufacturer, ROUND(SUM(total_sales)/1000000) AS sum_total_sales
FROM pharmacy_sales
GROUP BY manufacturer
ORDER BY SUM(total_sales) DESC, manufacturer
```

You want to concatinate something to the select columns so that it gets displayed nice. This is how you do it.
```python
SELECT manufacturer, CONCAT('$' || ROUND(SUM(total_sales)/1000000) || ' million') AS sum_total_sales
FROM pharmacy_sales
GROUP BY manufacturer
ORDER BY SUM(total_sales) DESC, manufacturer
```
