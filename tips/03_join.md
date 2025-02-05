-----------------------------------------------
When you are writing the query, if you just write `JOIN`, then it means that the result will contain intersection data</br>
Based on question, sometimes you need not only intersection data but also either complete data from left side table / right side table</br>
If you want data from left side table, then use LEFT OUTER JOIN</br>
If you want data from right side table, then use RIGHT OUTER JOIN</br>

<ins>Example 1:</ins></br>
Look at the question https://datalemur.com/questions/sql-page-with-no-likes</br>
In this case, LEFT OUTER JOIN has to be used not just JOIN
```python
SELECT pages.page_id
FROM pages
LEFT OUTER JOIN page_likes
ON pages.page_id = page_likes.page_id
WHERE page_likes.liked_date IS NULL
ORDER BY pages.page_id
```
<ins>Example 2:</ins></br>
Look at the question https://datalemur.com/questions/sql-ibm-db2-product-analytics</br>
Here; there are two tables named employees & queries --> you want to find out employee & the no of unique queries they ran</br>
employees is the left table & queries is the right table.</br>
Here is the critical point. Even though there is no entry for an employee in the queries table, his name should come in the result</br>
The reason is that the question says, even though an employee did not ran a single query, his name should be part of the result</br>
What this implies is that we want all the data from left table even though there is no matching data present in the right table.</br>
How can you do that `LEFT JOIN` / `LEFT OUTER JOIN`

-----------------------------------------------

`LEFT JOIN` and `LEFT OUTER JOIN` mean the same

-----------------------------------------------
