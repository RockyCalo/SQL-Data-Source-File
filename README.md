# SQL-Data-Source-File

Rocky Leo Calo
BSIT 3 Day Class
Goal: 
*
To practice the advance schema of a database to see the anomalies in making database table with the use of advance query so that in time when we are in the industries we are equip in database and Will trained. To prevent the redundancy of a data that can be make problem during in the operation I learn this things to our professor this learning will make the data secure and to prevent bad data. 
Database all about:
This kind of database is all about the company who sells a paper it has a 50 sales reps spread across the United States in four region this paper company sell three types of paper the regular, poster, and glossy.  This database can relate to the real world situation of SQL the problems that we encounter along the way to prevent the anomalies data in database by using SQL. I choose this type of database because this schema can help me to apply real world situation in the industries to prevent redundancy in the data. By the used of unique key in each table that has relationship it help my skills to develop more backend jobs with agile method to prevent errors in the future in the operation in any aspect which is the marketing finance. This Company consist a lot of data in the real world data is always growing  to prevent anomalies in early stage much better to design the ERD standards that our professor teach to us. 
 




Where did you get the database?
I get this database that our Professor give us online course in online school and I take it because it is free and also it helps me a lot the SQL how it work in data either big data or small data .How to CRUD the data in a database with proper query and not only CRUD but more complex query in each table.

# TABLE NAME AND DECRIPTION
WEB_EVENTS	ACCOUNTS	ORDERS	SALES-REPS	REGION
PK	PK	PK	PK	PK
FK	FK	FK	FK	

# DATABASE DEPENDENCY DIAGRAM
Data Dependency has a big rule in data table so that the data are always secure and less Redundancy. 
 
# Complex Queries:
# Query 1. 
SELECT id, account_id, occurred_at
FROM orders;
This Query you will see all the records of Id number which is in series and has also a date this is important in all data’s of database because you will see the data which in orders.
 
# Query2.
SELECT account_id
FROM orders
In this Query all data in web_events table the foreign key of account_id will pull out in the series this is important because it is a fundamentals of Query.
 
# Query 3.
Select name from accounts limit 15;
In this Query in the table of accounts the data  of name are limit into 15 row only all name in accounts are Limit into 15 in the real world scenario it has thousands or millions of data store in database if you need only 15 data this is helpful.  
  
# Query 4.
Select name from region limit 10;
In this Query in the table of Region the data of name are limit into 10 row only name of place In Region there are a lot of Region in Country if you need only 10 region this query is helpful.
 
# Query 5. 
SELECT occurred_at, account_id, channel
FROM web_events
LIMIT 5;
In this Query Table of accounts you will see first in the left side of a table the date and year which is in series order calendar date which is the first transaction to the new transaction at present.

 

# Query 6.
SELECT id, occurred_at, total_amt_usd
FROM orders
ORDER BY  occurred_at
LIMIT 10;
Write a query to return the 10 earliest orders in the orders table. Include the id, occurred_at and total_amt_usd this will help the records of orders return very early transaction of orders.
 

# Query 7.
SELECT id, account_id, total_amt_usd
FROM orders
ORDER BY total_amt_usd DESC 
LIMIT 5;
Write a query to return the top 5 orders in terms of largest total_amt_usd include the id,account_id, and total_amt_usd this will help the order that is in the top 5 from largest.
 

# Query 8.
SELECT id, account_id, total_amt_usd
FROM orders
ORDER BY total_amt_usd
LIMIT 20;
Write a query to return the lowest 20 orders in terms of smallest total_amt_usd include the id, account_id, total_amt_usd this is important because a lot of data in database and this query will return in 20 lowest orders it is easy to get the data.

 
# Query 9.
SELECT id, account_id, total_amt_usd
FROM orders
ORDER BY account_id, total_amt_usd DESC;

Write a query that displays the order ID, account ID, and total dollar amount for all the orders, sorted first by the account ID (in ascending order), and then by the total dollar amount (in descending order).
 

# Query 10.
SELECT id, account_id, total_amt_usd
FROM orders
ORDER BY total_amt_usd DESC, account_id;
Now write a query that again displays order ID, account ID, and total dollar amount for each order, but this time sorted first by total dollar amount (in descending order), and then by account ID (in ascending order).
 
# Query 11.
SELECT *
FROM orders
WHERE gloss_amt_usd >= 1000
LIMIT 5;
You will notice when using these WHERE statements, we do not need to ORDER BY unless we want to actually order our data. Our condition will work without having to do any sorting of the data. The WHERE clause allows you to filter a set of result based on specific criteria as you with Excel filter capability Filtering with WHERE allows you to answer much more meaningful questions 
 

# Query 12.
SELECT *
FROM orders
WHERE total_amt_usd < 500
LIMIT 10;
Imagine yourself as a manager of this Company  you have your most important customers and you want to show up prepared which means making sure that you are up to speed on all of their recent purchases  you can use a WHERE clause to generate a list of  all purchases made by the specific customer.  

 
# Query 13
SELECT *
FROM orders
WHERE total_amt_usd < 400
LIMIT 20;
The WHERE clause goes FROM but before ORDER BY or LIMIT As in previous queries, the clauses must be in the right order or the query will return an error. Common symbols used in WHERE statements include in this query the less than.

 
# Query 14.
SELECT *
FROM orders
WHERE total_amt_usd <= 100
LIMIT 13;
The condition will work without having to do any sorting of the data  (less than or equal to)
 
# Query 15.
SELECT *
FROM orders
WHERE total_amt_usd != 200
LIMIT 16;
WHERE clause that filter based on values in one column as we have done here you’ll the limit the result in all to rows that satisfy the condition  the idea is that each row is one data point or observation and all the information contained in that row belongs together. In this query is the not equal.
 
# Query 16.
SELECT name, website, primary_poc
FROM accounts
WHERE name = 'Exxon Mobil';
Filter the accounts table to include the company name, website, and the primary point of contact (primary_poc) just for the Exxon Mobil company in the accounts table.The WHERE statement can also be used with non-numeric data. You need to be sure to use single quotes. Not double quotes.
 
# Query 17.
SELECT id, account_id, standard_amt_usd/standard_qty AS unit_price
FROM orders
LIMIT 10;
In this Query as you can see the standard_amt_usd/standard_qty are divded as the unit price in this case Arithmetic  is functioning.
 

# Query 18
SELECT id, (standard_amt_usd/total_amt_usd)*100 AS std_percent, total_amt_usd
FROM orders
LIMIT 15;
In case of Arithmetic this time we used multiplication to multiply the std_percent total_amt_usd in the standard_amt_usd/total_usd
 
# Query 19.
SELECT id, (standard_amt_usd/total_amt_usd)+150 AS std_percent, total_amt_usd
FROM orders
LIMIT 10;
In this Query Arithmetic this time we used addition to add all the total. In each row there is a number and in columns will be add. Creating a new column that is a combination of existing columns is known as a derived column (or "calculated" or "computed" column). Usually you want to give a name, or "alias," to your new column using the AS keyword. 
= 



# Query 20.
SELECT name
FROM accounts
WHERE name LIKE 'C%';
In this Query 
The LIKE operator is extremely useful for working with text. You will use LIKE within a WHERE clause. The LIKE operator is frequently used with %. The % tells us that we might want any number of characters leading up to a particular set of characters or following a certain set of characters, as we saw with the google syntax above. Remember you will need to use single quotes for the text you pass to the LIKE operator, because of this lower and uppercase letters are not the same within the string. Searching for 'T' is not the same as searching for 't'. In other SQL environments (outside the classroom), you can use either single or double quotes.
 


# Query 21
SELECT name, primary_poc, sales_rep_id
FROM accounts
WHERE name IN ('Walmart', 'Target', 'Nordstrom');
The IN operator is useful for working with both numeric and text columns. This operator allows you to use an =, but for more than one item of that particular column. We can check one, two or many column values for which we want to pull data, but all within the same query. In the upcoming concepts, you will see the OR operator that would also allow us to perform these tasks, but the IN operator is a cleaner way to write these queries.
 



# Query 22
SELECT name
FROM accounts
WHERE name NOT LIKE '%one%';
The NOT operator is an extremely useful operator for working with the previous two operators we introduced: IN and LIKE. By specifying NOT LIKE or NOT IN, we can grab all of the rows that do not meet a particular criteria.
 

# Query 23
SELECT *
FROM orders
WHERE standard_qty > 1000 AND poster_qty = 0 AND gloss_qty = 0;
Write a query that returns all the orders where the standard_qty is over 1000, the poster_qty is 0, and the gloss_qty is 0.
 
# Query 24
SELECT *
FROM accounts
WHERE (name LIKE 'C%' OR name LIKE 'W%') 
           AND ((primary_poc LIKE '%ana%' OR primary_poc LIKE '%Ana%') 
           AND primary_poc NOT LIKE '%eana%');

Similar to the AND operator, the OR operator can combine multiple statements. Each time you link a new statement with an OR, you will need to specify the column you are interested in looking at. You may link as many statements as you would like to consider at the same time. This operator works with all of the operations we have seen so far including arithmetic operators (+, *, -, /), LIKE, IN, NOT, AND, and BETWEEN logic can all be linked together using the OR operator.

 

# Query 25
SELECT *
SELECT id
FROM orders
WHERE gloss_qty > 5000 OR poster_qty > 5000;
Similar to the AND operator, the OR operator can combine multiple statements. Each time you link a new statement with an OR, you will need to specify the column you are interested in looking at. You may link as many statements as you would like to consider at the same time. This operator works with all of the operations we have seen so far including arithmetic operators (+, *, -, /), LIKE, IN, NOT, AND, and BETWEEN logic can all be linked together using the OR operator.
 
