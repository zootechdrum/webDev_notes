## How do aliases work when making a SQL query ?

Aliases will only work in the select statement. It can't be used as a reference later on in the query . Take the following example into consideration. 

```sql 
        SELECT customer_id, sum(amount) AS total_spent FROM payment GROUP BY customer_id
```
The aliases in the above class will work. What will not work is if you tried to use total_spend as a reference at a later time in the query. 

```sql
        SELECT customer_id, sum(amount) AS total_spent
        FROM payment GROUP BY customer_id
        HAVING total_spent > 100
```

The above will not work. The total_spent aliases is only available to us in the `SELECT` clause. We can not use it in other places in the query. The query language has no idea that we declared an aliases therefore an error would be returned. 

What are aggregate functions in PostgresSQL ? 

The point of an aggregate functions is to take multiple inputs and returns a single output. 
Common aggregate functions inlcude avg() count() sum() . 
Aggregate functions only happen in the select statement or in the having clause. 

## When do we need to prepend the table name to the query ?
Take the below as an example:

```sql
SELECT film.film_id, title, inventory_id,store_id FROM film
LEFT JOIN inventory ON inventory.film_id = film.film.id
```
We need to prepend our table name to the column we are going to select if that table column name is not unique to that specific table. In the example above film_id is not unique to the film table as it also appears in our inventory table. Because of this we need to prepend it with our table name.  


## How can we GROUP BY ?

The Group BY clause must appear right after a `FROM` OR `WHERE` statement. 
In the `SELECT` statement, columns must either have an aggregate function or be in the GROUP BY call . 

```sql
    SELECT company, division, SUM(sales) FROM finance_table GROUP BY company, division
```
notice that company and division appear in the `GROUP BY` but the column in teh aggregate function does not appear after `GROUP BY` . If you want to sort results based on the aggregate function, make sure to reference the entire function . 

```sql
    SELECT company, SUM(sales) FROM finance_table GROUP BY company ORDER BY SUM(sales) LIMIT 5
```
Here is another example on how to filter based on the aggregate function performed . 
```sql
    SELECT company, SUM(sales) FROM finance_table  WHERE company != 'Google' GROUP BY company HAVING SUM(sales) > 100
```
## Performing a `LEFT OUTER JOIN`

A left outer join grabs every thing from the left table. For the table that we are joining to, the results return null if nothing matches. 

### What if we only wanted entries unique to out left table ?
```sql
    SELECT * FROM Registrations LEFT OUTER JOIN Logins ON Registration.name = Logins.name WHERE Logins.log_id IS null
```
The above example shows how we could grab entries unique to Registration . 
