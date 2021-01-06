# SQL-Data-Source-File


Goal: 

To practice the advance schema of a database to see the anomalies in making database table with the use of advance query so that in time when we are in the industries we are equip in database and Will trained. To prevent the redundancy of a data that can be make problem during in the operation I learn this things to our professor this learning will make the data secure and to prevent bad data. 
Database all about:
This kind of database is all about the company who sells a paper it has a 50 sales reps spread across the United States in four region this paper company sell three types of paper the regular, poster, and glossy.  This database can relate to the real world situation of SQL the problems that we encounter along the way to prevent the anomalies data in database by using SQL. I choose this type of database because this schema can help me to apply real world situation in the industries to prevent redundancy in the data. By the used of unique key in each table that has relationship it help my skills to develop more backend jobs with agile method to prevent errors in the future in the operation in any aspect which is the marketing finance. This Company consist a lot of data in the real world data is always growing  to prevent anomalies in early stage much better to design the ERD standards that our professor teach to us. 

![image](https://user-images.githubusercontent.com/72955529/103714462-aba37780-4ff9-11eb-876d-dc7c3e29937b.png)

 

Where did you get the database?
I get this database that our Professor give us online course in online school and I take it because it is free and also it helps me a lot the SQL how it work in data either big data or small data .How to CRUD the data in a database with proper query and not only CRUD but more complex query in each table.

# TABLE NAME AND DECRIPTION
WEB_EVENTS	ACCOUNTS	ORDERS	SALES-REPS	REGION </br>
![New Project](https://user-images.githubusercontent.com/72955529/103714976-5a47b800-4ffa-11eb-80fa-d2f1d33004a7.png)

# DATABASE DEPENDENCY DIAGRAM
Data Dependency has a big rule in data table so that the data are always secure and less Redundancy. 
![New Project (1)](https://user-images.githubusercontent.com/72955529/103715096-b6aad780-4ffa-11eb-8d9c-478b1598b6c5.png)

 
# Complex Queries:
# Query 1. 
SELECT id, account_id, occurred_at
FROM orders;
<br></br>
This Query you will see all the records of Id number which is in series and has also a date this is important in all data’s of database because you will see the data which in orders.
<br><br>
![image](https://user-images.githubusercontent.com/72955529/103715228-04274480-4ffb-11eb-96bb-89dd70add4ee.png)

# Query2.
SELECT account_id
FROM orders
<br></br>
In this Query all data in web_events table the foreign key of account_id will pull out in the series this is important because it is a fundamentals of Query.
<br></br>
![image](https://user-images.githubusercontent.com/72955529/103715359-5e280a00-4ffb-11eb-93b8-36a7a2361863.png)

# Query 3.
Select name from accounts limit 15;
<br></br>
In this Query in the table of accounts the data  of name are limit into 15 row only all name in accounts are Limit into 15 in the real world scenario it has thousands or millions of data store in database if you need only 15 data this is helpful.  
<br></br>
![image](https://user-images.githubusercontent.com/72955529/103715471-ad6e3a80-4ffb-11eb-9757-b0f80d714ba7.png)

# Query 4.
Select name from region limit 10;
<br></br>
In this Query in the table of Region the data of name are limit into 10 row only name of place In Region there are a lot of Region in Country if you need only 10 region this query is helpful.
<br></br>
![image](https://user-images.githubusercontent.com/72955529/103715516-c8d94580-4ffb-11eb-9092-acb7b8e5b762.png)

 
# Query 5. 
SELECT occurred_at, account_id, channel
FROM web_events
LIMIT 5;
<br></br>
In this Query Table of accounts you will see first in the left side of a table the date and year which is in series order calendar date which is the first transaction to the new transaction at present.
<br></br>
![image](https://user-images.githubusercontent.com/72955529/103715552-e0183300-4ffb-11eb-8044-a216e07f1c39.png)


 

# Query 6.
SELECT id, occurred_at, total_amt_usd
FROM orders
ORDER BY  occurred_at
LIMIT 10;
<br></br>
Write a query to return the 10 earliest orders in the orders table. Include the id, occurred_at and total_amt_usd this will help the records of orders return very early transaction of orders.
<br></br>
![image](https://user-images.githubusercontent.com/72955529/103715580-f8884d80-4ffb-11eb-96bd-24f2a3248897.png)


# Query 7.
SELECT id, account_id, total_amt_usd
FROM orders
ORDER BY total_amt_usd DESC 
LIMIT 5;
<br></br>
Write a query to return the top 5 orders in terms of largest total_amt_usd include the id,account_id, and total_amt_usd this will help the order that is in the top 5 from largest.
<br></br>
![image](https://user-images.githubusercontent.com/72955529/103715611-0b9b1d80-4ffc-11eb-938d-468e46e9a270.png)

 

# Query 8.
SELECT id, account_id, total_amt_usd
FROM orders
ORDER BY total_amt_usd
LIMIT 20;
<br></br>
Write a query to return the lowest 20 orders in terms of smallest total_amt_usd include the id, account_id, total_amt_usd this is important because a lot of data in database and this query will return in 20 lowest orders it is easy to get the data.
<br></br>
![image](https://user-images.githubusercontent.com/72955529/103715661-2bcadc80-4ffc-11eb-8339-7be3a566e6a5.png)

 
# Query 9.
SELECT id, account_id, total_amt_usd
FROM orders
ORDER BY account_id, total_amt_usd DESC;
<br></br>
Write a query that displays the order ID, account ID, and total dollar amount for all the orders, sorted first by the account ID (in ascending order), and then by the total dollar amount (in descending order).
 <br></br>
![image](https://user-images.githubusercontent.com/72955529/103715695-40a77000-4ffc-11eb-8d56-248f39c7c914.png)


# Query 10.
SELECT id, account_id, total_amt_usd
FROM orders
ORDER BY total_amt_usd DESC, account_id;
<br></br>
Now write a query that again displays order ID, account ID, and total dollar amount for each order, but this time sorted first by total dollar amount (in descending order), and then by account ID (in ascending order).
<br></br>
![image](https://user-images.githubusercontent.com/72955529/103715722-51f07c80-4ffc-11eb-95b0-9683b3570142.png)

# Query 11.
SELECT *
FROM orders
WHERE gloss_amt_usd >= 1000
LIMIT 5;
<br></br>
You will notice when using these WHERE statements, we do not need to ORDER BY unless we want to actually order our data. Our condition will work without having to do any sorting of the data. The WHERE clause allows you to filter a set of result based on specific criteria as you with Excel filter capability Filtering with WHERE allows you to answer much more meaningful questions 
<br></br>
![image](https://user-images.githubusercontent.com/72955529/103715767-6cc2f100-4ffc-11eb-98f9-9e080de9a5eb.png)


# Query 12.
SELECT *
FROM orders
WHERE total_amt_usd < 500
LIMIT 10;
<br></br>
Imagine yourself as a manager of this Company  you have your most important customers and you want to show up prepared which means making sure that you are up to speed on all of their recent purchases  you can use a WHERE clause to generate a list of  all purchases made by the specific customer.  
<br></br>
![image](https://user-images.githubusercontent.com/72955529/103715810-7e0bfd80-4ffc-11eb-8c41-d9e5d4f2e75c.png)

 
# Query 13
SELECT *
FROM orders
WHERE total_amt_usd < 400
LIMIT 20;
<br></br>
The WHERE clause goes FROM but before ORDER BY or LIMIT As in previous queries, the clauses must be in the right order or the query will return an error. Common symbols used in WHERE statements include in this query the less than.
<br></br>
![image](https://user-images.githubusercontent.com/72955529/103715845-92e89100-4ffc-11eb-8b42-f4e46d3b2b62.png)

 
# Query 14.
SELECT *
FROM orders
WHERE total_amt_usd <= 100
LIMIT 13;
<br></br>
The condition will work without having to do any sorting of the data  (less than or equal to)
<br></br>
![image](https://user-images.githubusercontent.com/72955529/103715944-d511d280-4ffc-11eb-8322-16816969fccc.png)
 
# Query 15.
SELECT *
FROM orders
WHERE total_amt_usd != 200
LIMIT 16;
<br></br>
WHERE clause that filter based on values in one column as we have done here you’ll the limit the result in all to rows that satisfy the condition  the idea is that each row is one data point or observation and all the information contained in that row belongs together. In this query is the not equal.
<br></br>
![image](https://user-images.githubusercontent.com/72955529/103715988-eeb31a00-4ffc-11eb-9ab0-aeee0b25f9a3.png)

# Query 16.
SELECT name, website, primary_poc
FROM accounts
WHERE name = 'Exxon Mobil';
<br></br>
Filter the accounts table to include the company name, website, and the primary point of contact (primary_poc) just for the Exxon Mobil company in the accounts table.The WHERE statement can also be used with non-numeric data. You need to be sure to use single quotes. Not double quotes.
<br></br>
![image](https://user-images.githubusercontent.com/72955529/103716031-02f71700-4ffd-11eb-91d7-a3ac995b680d.png)

# Query 17.
SELECT id, account_id, standard_amt_usd/standard_qty AS unit_price
FROM orders
LIMIT 10;
<br></br>
In this Query as you can see the standard_amt_usd/standard_qty are divded as the unit price in this case Arithmetic  is functioning.
<br></br>
![image](https://user-images.githubusercontent.com/72955529/103716062-14402380-4ffd-11eb-9381-421f50102916.png)


# Query 18
SELECT id, (standard_amt_usd/total_amt_usd)*100 AS std_percent, total_amt_usd
FROM orders
LIMIT 15;
<br></br>
In case of Arithmetic this time we used multiplication to multiply the std_percent total_amt_usd in the standard_amt_usd/total_usd
<br></br>
![image](https://user-images.githubusercontent.com/72955529/103716091-291cb700-4ffd-11eb-8e30-63fbbb9e35c8.png)

# Query 19.
SELECT id, (standard_amt_usd/total_amt_usd)+150 AS std_percent, total_amt_usd
FROM orders
LIMIT 10;
<br></br>
In this Query Arithmetic this time we used addition to add all the total. In each row there is a number and in columns will be add. Creating a new column that is a combination of existing columns is known as a derived column (or "calculated" or "computed" column). Usually you want to give a name, or "alias," to your new column using the AS keyword. 
<br></br>
![image](https://user-images.githubusercontent.com/72955529/103716146-3f2a7780-4ffd-11eb-98fa-e8d0df02dc04.png)



# Query 20.
SELECT name
FROM accounts
WHERE name LIKE 'C%';
</br></br>
In this Query 
The LIKE operator is extremely useful for working with text. You will use LIKE within a WHERE clause. The LIKE operator is frequently used with %. The % tells us that we might want any number of characters leading up to a particular set of characters or following a certain set of characters, as we saw with the google syntax above. Remember you will need to use single quotes for the text you pass to the LIKE operator, because of this lower and uppercase letters are not the same within the string. Searching for 'T' is not the same as searching for 't'. In other SQL environments (outside the classroom), you can use either single or double quotes.
 
<br></br>
![image](https://user-images.githubusercontent.com/72955529/103716170-51a4b100-4ffd-11eb-8ebd-7a5835a45dc1.png)


# Query 21
SELECT name, primary_poc, sales_rep_id
FROM accounts
WHERE name IN ('Walmart', 'Target', 'Nordstrom');
<br></br>
The IN operator is useful for working with both numeric and text columns. This operator allows you to use an =, but for more than one item of that particular column. We can check one, two or many column values for which we want to pull data, but all within the same query. In the upcoming concepts, you will see the OR operator that would also allow us to perform these tasks, but the IN operator is a cleaner way to write these queries.
 
<br></br>
![image](https://user-images.githubusercontent.com/72955529/103716279-97fa1000-4ffd-11eb-9081-cea3bc21bdfa.png)



# Query 22
SELECT name
FROM accounts
WHERE name NOT LIKE '%one%';
<br></br>
The NOT operator is an extremely useful operator for working with the previous two operators we introduced: IN and LIKE. By specifying NOT LIKE or NOT IN, we can grab all of the rows that do not meet a particular criteria.
<br></br>
![image](https://user-images.githubusercontent.com/72955529/103716312-aa744980-4ffd-11eb-8563-2026fe80b4da.png)


# Query 23
SELECT *
FROM orders
WHERE standard_qty > 1000 AND poster_qty = 0 AND gloss_qty = 0;
<br></br>
Write a query that returns all the orders where the standard_qty is over 1000, the poster_qty is 0, and the gloss_qty is 0.
<br></br>
![image](https://user-images.githubusercontent.com/72955529/103716339-beb84680-4ffd-11eb-87b9-0643cfd512ef.png)

 
# Query 24
SELECT *
FROM accounts
WHERE (name LIKE 'C%' OR name LIKE 'W%') 
           AND ((primary_poc LIKE '%ana%' OR primary_poc LIKE '%Ana%') 
           AND primary_poc NOT LIKE '%eana%');
<br></br>
Similar to the AND operator, the OR operator can combine multiple statements. Each time you link a new statement with an OR, you will need to specify the column you are interested in looking at. You may link as many statements as you would like to consider at the same time. This operator works with all of the operations we have seen so far including arithmetic operators (+, *, -, /), LIKE, IN, NOT, AND, and BETWEEN logic can all be linked together using the OR operator.
<br></br>
![image](https://user-images.githubusercontent.com/72955529/103716362-d099e980-4ffd-11eb-8679-481e3798aa10.png)

 

# Query 25
SELECT *
SELECT id
FROM orders
WHERE gloss_qty > 5000 OR poster_qty > 5000;
<br></br>
Similar to the AND operator, the OR operator can combine multiple statements. Each time you link a new statement with an OR, you will need to specify the column you are interested in looking at. You may link as many statements as you would like to consider at the same time. This operator works with all of the operations we have seen so far including arithmetic operators (+, *, -, /), LIKE, IN, NOT, AND, and BETWEEN logic can all be linked together using the OR operator.
 <br></br>
 ![image](https://user-images.githubusercontent.com/72955529/103716394-e4455000-4ffd-11eb-85d0-26f3b45d7a98.png)

