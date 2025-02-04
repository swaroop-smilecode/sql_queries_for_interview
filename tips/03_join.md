When you are writing the query, if you just write `JOIN`, then it means that the result will contain intersection data</br>
Based on question, sometimes you need not only intersection data but also either complete data from left side table / right side table</br>
If you want data from left side table, then use LEFT OUTER JOIN</br>
If you want data from right side table, then use RIGHT OUTER JOIN</br>

Let's understand through an example.</br>
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
