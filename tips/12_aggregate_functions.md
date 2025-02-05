#### Most frequently used aggregate functions
- MAX
- MIN
- SUM
- AVG
- For calculating mean, you don't use function. Instead, sum(column_x) / sum(column_y) 

#### GROUP BY is not mandatory
It's not mandatory to use GROUP BY when using aggregate functions.</br>
If you don't use GROUP BY, then only one result will be returned for the whole table on which you are running the query.</br>
But, if you use the GROUP BY, then whole table gets split into different tables & the aggregate function runs on those small tables</br>
because of which you will see multilple results returned for the query.
