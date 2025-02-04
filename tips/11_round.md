`ROUND` function can round only `DECIMAL` numbers, not integers. Hence, if you have integer numbers,</br>
type caste them to decimal numbers before applying ROUND function.

```python
SELECT ROUND((SUM(item_count::DECIMAL*order_occurrences) / SUM(order_occurrences)),1)
FROM items_per_order
```
