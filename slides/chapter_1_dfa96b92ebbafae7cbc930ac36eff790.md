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
title: Business Intelligent Specialist / Data Scientist


`@script`
Hi, I am Nujcharee Haswell (Ped), welcome to this course “Case Study: Data Driven Decision Making with SQL”. 

In this video, you'll be learning about building basic SQL queries.


---
## What is SQL?

```yaml
type: "FullSlide"
key: "19ff28420e"
```

`@part1`
- Structured Query Language {{2}}

- Used to access & interrogate relational databases {{3}}

- Perform fundamental data exploring tasks such as {{4}}

    - retrieve data {{5}}

    - manipulate data {{6}}

    - summarise data {{7}}

- Many more {{8}}


`@script`
- Structured Query Language

- Used to access & interrogate relational databases (is a language that is widely used by different database platforms and as a result some SQL syntax and functions may vary however pretty much similar and pretty much standard)

- Perform fundamental data exploring tasks such as 
- retrieve data
- manipulate data 
- summarise data 
And many more

You will learn how to build a simple SQL query
SQL Syntax SELECT...FROM
and SQL summarising functions. Later in the course you will learn the difference type of JOINs when working with multiple tables


---
## What is relational database?

```yaml
type: "TwoColumns"
key: "9810dbbd56"
```

`@part1`
- Tables
    
    - fields / columns
    
    - rows / records

- Relationship between tables


`@part2`
![](https://github.com/nujcharee/courses/blob/master/Screen%20Shot%202018-09-16%20at%2000.27.11.png?raw=true) {{2}}


`@script`
Before deep diving into SQL, it’s important to have a basic understanding of relational database concept.

Relational databases organise data into “tables” consisting of rows and columns. Each column in a database has a specific data type text, number, date and so on. 

There are multiple database platforms as a result SQL will vary slightly. on this course we will focus on MS SQL Database. However if you chose to focus on a different environment such as PosgresSQL, Datacamp also offers a course “Joining data in Postgresql course” by Chester Ismay which may interest you.

Later in the course you will see the difference types of aggregated functions which only work with certain data types. 

Once you understand the basis of SQL syntax and functions when working with a relational database, you will be able to apply techniques to solve real world problems with confidence.


---
## What is relational database?

```yaml
type: "FullSlide"
key: "b6de51e38e"
```

`@part1`
- Tables
    
    - fields / columns
    
    - rows / records


![](https://github.com/nujcharee/courses/blob/master/Screen%20Shot%202018-09-16%20at%2000.27.11.png?raw=true) {{2}}


`@script`
Before deep diving into SQL, it’s important to have a basic understanding of relational database concept.

Relational databases organise data into “tables” consisting of rows and columns. Each column in a database has a specific data type text, number, date and so on. 

There are multiple database platforms as a result SQL will vary slightly. on this course we will focus on MS SQL Database. However if you chose to focus on a different environment such as PosgresSQL, Datacamp also offers a course “Joining data in Postgresql course” by Chester Ismay which may interest you.

Later in the course you will see the difference types of aggregated functions which only work with certain data types. 

Once you understand the basis of SQL syntax and functions when working with a relational database, you will be able to apply techniques to solve real world problems with confidence.


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
SELECT * FROM <Table Name>;
SELECT <Field1>, <Field2>, <Field3> FROM <Table Name>;
``` {{2}}
- Always remember to only retrieve columns that you need {{3}}

- `SELECT *` may cause performance to suffer from the fact the query pulls up too much data {{4}}

- The semi-colon (;) indicates that SQL statment is complete and is ready to be interpreted {{5}}


`@script`
A Select statement begins with SELECT keyword followed by FROM clause.

The top select statement will retrieve data from a single column from a single table. While the second select statement select ALL columns within a table. Last select statement select three fields from a table.

Always remember to only retrieve columns that you need as SELECT ALL columns may cause performance to suffer from the fact that query pulls up too much data)

It is also a good practise to always put the semi-colon (;) which indicates that SQL statment is complete and is ready to be interpreted


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
**Question:  What is the name of the game at Number 1 in year 2006 ** {{3}}

```
SELECT Name, Year FROM Sales where Rank = 1;
``` {{4}}
**Answer:  Wii Sport ** {{5}}


`@script`
Let's practice this in the first case study.

We will use a database from Kaggle's Video Game Global Sales competition. Imagine that you work in a video game industry and you are tasked to carry out a market research. Your job is to analyse sales trend. 

Let's have a quick glance over the Sales table here. Think about the SELECT statement needed to retrieve ALL columns from this table.

First, you will use SELECT * (asterisk) FROM Sales;

The first question you may want answered is: What's all sales look like? Let's think about how you will write this in a select statement.

You can revise the first query by only retrieving the columns you want in your result.


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
SELECT Rank, Name, Platform, Year, Genre, Global_Sales FROM SALES
WHERE Year = 2016 ORDER BY Rank
``` {{5}}

**Answer: Looks like soccer on PS4 is doing pretty awesome worldwide! **
{{6}}


`@script`
WHERE and ORDER keywords are optional from select statement.

WHERE is used to apply condition(s) to a query. It can filter out the rows that we want to show while ORDER BY is used if the result rows should be in a specific order
 
Let's look at this question. What games were sold in year 2016? Think about what select statement requires to return this result.


---
## Text Fields vs. Numeric Fields

```yaml
type: "FullCodeSlide"
key: "c48ac2161e"
```

`@part1`
- Text requires single quotes around text values {{2}}

- Numeric fields should not be enclosed in quotes {{3}}

**Question:  How does FIFA 17 game perform through the year? ** {{4}}

```
SELECT Rank , Name, Platform, Year, Genre FROM SALES WHERE Name = 'FIFA 17' 
``` {{5}}

![](https://github.com/nujcharee/courses/blob/master/Screen%20Shot%202018-09-16%20at%2000.50.29.png?raw=true) {{6}}


`@script`
Recall from the previous slides that Sale table is consisted of text and numeric data type. 

SQL requires single quotes around text values  while this may differ in other database platforms e.g use of double quotes instead. However, numeric fields should not be enclosed in quotes

We will learn more about these two data types in later chapters.


---
## Summarising data

```yaml
type: "FullSlide"
key: "b68404a3f8"
```

`@part1`
- Simple aggregate functions such as count, minimum, maximum, average, and sum {{1}}

```
SELECT COUNT(Name) FROM Sales;

SELECT AVG(Global_Sales) FROM Sales;

SELECT MIN(Global_Sales) FROM Sales; 

SELECT MAX(Global_Sales) FROM Sales; 

SELECT SUM(Global_Sales) FROM Sales; 
``` {{2}}

- GROUP BY split the table into different piles based on the value of each row {{3}}


`@script`
The most interesting functions of SQL


---
## Let's practice!

```yaml
type: "FinalSlide"
key: "b240739c0d"
```

`@script`
Time to put this into practice.

