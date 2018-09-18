---
title: Insert title here
key: dfa96b92ebbafae7cbc930ac36eff790

---
## Welcome

```yaml
type: "TitleSlide"
key: "8ed49f4555"
```

`@lower_third`

name: Nujcharee Haswell (Ped)
title: Data Intelligence Specialist / Data Scientist


`@script`
Hi, welcome to the course I’m Nujcharee Haswell and I’m a data intelligence specialist and a data scientist. I’ll be your instructor for Case Study Data Driven Decision Making with SQL.


---
## What is SQL?

```yaml
type: "FullSlide"
key: "19ff28420e"
```

`@part1`
- Structured Query Language {{2}}

- Used to  {{3}}

    - retrieving data {{4}}

    - manipulating data {{5}}

    - summarising data {{6}}

- Explore and summarise a real life database. {{7}}


`@script`
SQL Stands for structured query language.

You can use SQL to interact with relational databases and other things such as retrieving, manipulating or aggregating data and many more.

In this video you will be building sql queries to explore and summarise a real life database.


---
## What is relational database?

```yaml
type: "TwoColumns"
key: "9810dbbd56"
```

`@part1`
- Data organised in "Table" objects {{1}} 
    
    - rows {{2}}
    
    - columns {{3}}

- More than one tables in the database {{4}}

- Can JOIN these tables to build queries where relationship between tables exist {{5}}


`@part2`
![](https://github.com/nujcharee/courses/blob/master/Screen%20Shot%202018-09-16%20at%2019.56.50.png?raw=true) {{3}}


`@script`
Before deep diving into SQL, it’s important to have a basic understanding of relational database concept.

Relational databases organise data into “table” objects consisting of rows and columns. Each column in a database has a specific data type such as text, number, date and so on. 

There are usually more than one tables in a database.

They can be joined to build queries where relationships between tables exist.

You will be learning more about JOINing tables later in the course.


---
## Basic SQL Query

```yaml
type: "FullSlide"
key: "5ee4acfdd2"
```

`@part1`
- Select statement begins with SELECT keyword {{1}}

```
SELECT <Field Names> FROM <Table Name>;
``` {{2}}

```
SELECT * FROM <Table Name>;
``` {{3}}

```
SELECT <Field1>, <Field2>, <Field3> FROM <Table Name>;
``` {{4}}

- Always remember to only retrieve columns that you need {{5}}

- `SELECT *` may cause performance to suffer from the fact the query pulls up too much data {{6}}

- The semi-colon (;) indicates that SQL statment is complete and is ready to be interpreted {{7}}


`@script`
A Select statement begins with SELECT keyword followed by FROM clause.

The first select statement will retrieve data from a single column from a single table. 

The special character asterisk can be used in a select statement in order to retrieve ALL columns from a table as you can see in the second select statement.

It is possible to select more than one columns from a table as per the third sample right here.

Always remember to only retrieve columns that you need as SELECT ALL columns may cause performance to suffer from the fact that query pulls up too much data.


It is also a good practise to always put the semi-colon (;) which indicates that SQL statement is complete and is ready to be interpreted.


---
## Case Studies: Video Games Global Sales database

```yaml
type: "FullSlide"
key: "9e2bb70cfe"
```

`@part1`
![](https://github.com/nujcharee/courses/blob/master/Screen%20Shot%202018-09-16%20at%2011.29.09.png?raw=true) {{1}}

```
SELECT * FROM SALES;
``` {{2}}
**Question:  What is the name of Number 1 game in 2006? ** {{3}}

```
SELECT Name, Year FROM Sales WHERE Rank = 1;
``` {{4}}
**Answer:  Wii Sport ** {{5}}


`@script`
Let’s apply this with a real database. For the first case study you will use a database from Kaggle's Video Game Global Sales competition. Imagine that you work in a video game industry and you are tasked to carry out a market research. Your job is to analyse sales trend. 

Let's have a quick glance over the Sales table here. Think about the SELECT statement needed to retrieve ALL columns from this table.

You will use SELECT *  FROM Sales;

The first question you may want answered is: What is the name of Number 1 game in 2006? Let's think about how you will write this in a select statement.

That’s right.


---
## WHERE and ORDER BY

```yaml
type: "FullSlide"
key: "73171c367d"
```

`@part1`
- WHERE is used to apply condition(s) to a query {{1}}

- ORDER BY is used if the result rows should be in a specific order {{2}}

**Question: What games were sold in 2016? **
{{3}}

![](https://github.com/nujcharee/courses/blob/master/Screen%20Shot%202018-09-16%20at%2000.14.48.png?raw=true) {{4}}

```
SELECT Rank, Name, Platform, Year, Genre, Global_Sales FROM Sales
WHERE Year = 2016 ORDER BY Rank;
``` {{5}}

**Answer: Looks like soccer on PS4 is doing pretty awesome worldwide! **
{{6}}


`@script`
WHERE and ORDER keywords are optional from select statement.

You noticed that in the last SQL query, WHERE is used to apply condition(s) to a query. It can filter out the rows that we want to show while ORDER BY is used if the result rows should be in a specific order
 
Let's look at this question. What games were sold in 2016? 

Think about what select statement requires to return this result.

There you got it.


---
## Summarising data

```yaml
type: "FullSlide"
key: "b68404a3f8"
```

`@part1`
- Aggregate functions such as count, minimum, maximum, average, and sum {{1}}

```
SELECT COUNT(Name) FROM Sales;

SELECT AVG(Global_Sales) FROM Sales;

SELECT MIN(Global_Sales) FROM Sales; 

SELECT MAX(Global_Sales) FROM Sales; 

SELECT SUM(Global_Sales) FROM Sales; 
``` {{2}}

- GROUP BY split the table into different groups based on the value of each row {{3}}

**Question:  What is Nintendo's highest selling group by year? ** {{4}}

```
SELECT MAX(NA_SALES) FROM SALES WHERE Publisher = 'Nintendo'
GROUP BY Year;
``` {{5}}

**Answer: The highest selling in 2006 is $41.49 million thanks to Wii Sport ** {{6}}


`@script`
After exploring content of a table next you may need to summarize data. SQL has keywords for aggregate functions namely

COUNT, which is a keyword used to return total number of rows

We use AVG keyword in order to find the average of a given value. 

As for MIN and MAX, they are used to find the minimum and maximum value of a table respectively.

And SUM keyword is used to find the sum of a given value

These functions are usually followed by GROUP BY keyword which is use to split the table into different groupa based on the value of each row.

Let’s put this together to answer a question 

What is Nintendo's highest selling group by year?

Answer: The highest selling in 2006 is $41.49 million thanks to Wii Sport


---
## Let's practice!

```yaml
type: "FinalSlide"
key: "b240739c0d"
```

`@script`
Its your turn to practise!

