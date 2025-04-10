
# SQL Quiz and Answers

This document contains a series of SQL questions, their corresponding answers, and explanations.

---

## Question 1

What is the output of the SQL query?
```sql
SELECT 'a';
```
**Answer:**
The query returns a single-column result set with the column name `'a'` and a single row containing the value `'a'`.

**Explanation:**
`SELECT` statements do not necessarily need tables. `SELECT` can be used to get any value or array of values. For example, to learn more, run the queries listed below.
```sql
SELECT 'a', 'b', 'c';
```

---

## Question 2

What is the output of the SQL query?
```sql
SELECT * FROM customer_t WHERE 1=2;
```
**Answer:**
The query returns zero rows.

**Explanation:**
`1=2` is a condition that is always false because 1 is never equal to 2.
The `WHERE` clause filters rows based on this condition, meaning no rows will satisfy the condition.
As a result, the query returns zero rows.

---

## Question 3

What SQL element can temporarily rename a column or table heading?

**Answer:**
`ALIAS`

**Explanation:**
A table or a column name in a table can be given a temporary name using SQL aliases. 
SQL aliases are specified using the `AS` clause.

---

## Question 4

What is the output of the SQL query?
```sql
SELECT NULL;
```
**Answer:**
It’ll return a column with header `NULL` and one row with no value.

**Explanation:**
In SQL, `NULL` represents an unknown or missing value. 
It is not equivalent to zero or an empty string.
When you execute `SELECT NULL;`, the query returns a single row containing `NULL` as the value.
Since `NULL` has no specific representation, database clients usually display it as NULL or leave it blank depending on the interface.

---

## Question 5

Select True/False for the following statement:
"We can retrieve unique values by using the `DISTINCT` function in the `SELECT statement`."

**Answer:**
`True`

**Explanation:**
You can retrieve unique values using the `DISTINCT` keyword in a `SELECT` statement.

---

## Question 6
What does the following query do?

```SQL
SELECT * FROM customer_t WHERE customer_age != 20;
```

**Answer:**
It will fetch all the details of the customers whose age is not equal to 20.

**Explanation:**
The symbol `!=` denotes "not equal to".
The above query will fetch all the columns from the `customer_t` table where the `customer_age` is not equal to 20.

---

## Question 7
How many customers are between 15 and 25 years old?

**Answer:**
2

**Explanation:**
```SQL
SELECT COUNT(*) FROM customer_t WHERE customer_age BETWEEN 15 AND 25;
```
This query will fetch the details of customers whose age is between 15 and 25 using the `BETWEEN` operator.

---

## Question 8
How many customers reside in Chicago?

**Answer:**
2

**Explanation:**
```SQL
SELECT COUNT(*) FROM customer_t WHERE city = 'Chicago';
```
This query will fetch the details of customers whose city is Chicago.

---

## Question 9
How many customers don’t reside in New York?

**Answer:**
3

**Explanation:**
```SQL
SELECT COUNT(*) FROM customer_t WHERE city != 'New York';
```
This query will fetch the details of customers who are not from the city of New York. 
The condition is specified in the `WHERE` clause.

---

## Question 10
How many customers have a tenure of 1 or 2?

**Answer:**
2

**Explanation:**

```SQL
SELECT COUNT(*) FROM customer_t WHERE tenure = 1 OR tenure = 2;
```
The correct result can be provided by using the `OR` operator. 
This query demonstrates the correct way to use the `OR` operator in the `WHERE` clause.

```SQL
SELECT COUNT(*) FROM customer_t WHERE tenure IN (1,2);
```
The correct result can also be obtained using the `IN` operator.


