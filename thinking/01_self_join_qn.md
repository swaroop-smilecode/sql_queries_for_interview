--------------------------------------------------------------------
Suppose, let's see the question https://datalemur.com/questions/sql-well-paid-employees</br>
Think in the same lines of join</br>
You need to create a big table which is combination of employee table & manager table</br>
What should be the join condition?</br>
You need to join manager table with employee table</br> 
For each record in employee table, you need a corresponding record from manager table `ON e.manager_id = m.employee_id`</br>
```python
SELECT e.employee_id, e.name
FROM employee e 
JOIN employee m
ON e.manager_id = m.employee_id
```
Now, you have 2 tables joined together as below
![image](https://github.com/user-attachments/assets/97312d71-ed1f-466f-bf1e-f811f76c69ff)

Now, it's very simple</br>
All that you have to do is: `WHERE e.salary > m.salary`
