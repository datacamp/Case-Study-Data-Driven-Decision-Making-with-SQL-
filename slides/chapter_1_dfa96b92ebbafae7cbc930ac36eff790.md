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
## Why SQL?

```yaml
type: "FullSlide"
key: "261a7ff134"
```

`@part1`
SQL


`@script`



---
## What is SQL?

```yaml
type: "FullSlide"
key: "19ff28420e"
```

`@part1`
- Structured Query Language {{2}}

- Used to accessing & interrogating relational databases {{3}}

- Perform fundamental data exploring tasks such as {{4}}

    - retrieve data {{5}}

    - manipulate data {{6}}

    - aggregate data {{7}}


`@script`
- Structured Query Language

- Used to accessing & interrogating relational databases (is a language that is widely used by different database platforms and as a result some SQL syntax and functions may vary however pretty much similar and pretty much standard)
Perform fundamental data exploring tasks such as 
retrieve data
manipulate data 
aggregate data 
You will learn how to build a simple SQL query
SQL Syntax SELECT...FROM
(more advanced queries that include ) SQL aggregated functions
Difference type of JOINs when working with multiple tables




Why do we use SQL to assist us with data driven decisions? 

one of the first reasons would be that companies mostly store data in Relational Database Management Systems (RDBMS) or in Relational Data Stream Management Systems (RDSMS) and you need SQL to access that data. SQL is the lingua franca of data: it gives you the ability to interact with almost any database or to even build your own locally!

Not only SQL is a must-have skill for data scientists,  
What is SQL?

Used to accessing relational databases (is a language that is widely used by different database platforms and as a result some SQL syntax and functions may vary however pretty much similar and pretty much standard)


---
## What is relational database?

```yaml
type: "FullSlide"
key: "b6de51e38e"
```

`@part1`
Table = database object where data is stored. It has field(s) and  column(s)

![](https://github.com/nujcharee/courses/blob/master/Screen%20Shot%202018-09-16%20at%2000.27.11.png?raw=true)


`@script`
Before deep diving into SQL, it’s important to have a basic understanding of relational database concept.

Relational databases organize data into “tables” consisting of rows and columns. Each column in a database has a specific data type text, number, date and so on. 

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

- `SELECT *` may cause performance to suffer from the fact that your query pulls up too much data) {{4}}

- The semi-colon (;) indicates that SQL statment is complete and is ready to be interpreted {{5}}


`@script`
- `SELECT <Field Names> FROM <Table Name> ` 

- `SELECT * FROM Sales`
 
- `SELECT Year,Publisher, Revenue FROM Sales`


Always remember to only retrieve columns that you need (as it may cause performance to suffer from the fact that your query pulls up too much data)


---
## Case Studies: Video Games Global Sales database

```yaml
type: "FullSlide"
key: "9e2bb70cfe"
```

`@part1`
- Retrieve all columns from the Sales table {{1}}

```
SELECT * FROM SALES`
``` {{2}}
**Question:  What's the overall sales look like? ** {{3}}

```
SELECT Rank, Name, Platform, Year, Genre, GLobal_Sales FROM SALES
``` {{4}}

![](https://github.com/nujcharee/courses/blob/master/Screen%20Shot%202018-09-15%20at%2023.52.37.png?raw=True) {{5}}


`@script`
First case study, we will use a dataset from Video Game Global Sales. This dataset is based on a Kaggle's competition. Imagine that you work in a video game industry and you are tasked to carry out market research. Your job is to analyse sales trend. 

First, lets retrieve all columns from the Sales table by executing the SELECT statement below:

The first question you may want answered is: What's all sales look like?

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

**List records of Sales in 2016? **
{{3}}
```
SELECT Rank, Name, Platform, Year, Genre, GLobal_Sales FROM SALES
WHERE Year = 2016 ORDER BY Rank
``` {{4}}

![](https://github.com/nujcharee/courses/blob/master/Screen%20Shot%202018-09-16%20at%2000.14.48.png?raw=true) {{5}}


`@script`
WHERE is used to apply condition(s) to a query. It can filter out the rows that we want to show.
 
In our case the only rows we want to consider are those where the value of the year column is 2016. 

You can improve queries built earlier by adding WHERE keyword followed by condition to apply, in this case its Year = 2016


---
## Text Fields vs. Numeric Fields

```yaml
type: "TwoColumns"
key: "b7e5a08489"
```

`@part1`
- In this database, there are 2 data types: Text and Numeric

- Text requires single quotes around text values 

- Numeric fields should not be enclosed in quotes


`@part2`
**Question:  How does FIFA 17 game perform through the year? ** 

```
SELECT Rank
, Name
, Platform
, Year
, Genre 
FROM SALES 
WHERE Name = 'FIFA 17'
```

![](https://github.com/nujcharee/courses/blob/master/Screen%20Shot%202018-09-16%20at%2000.50.29.png?raw=true)


`@script`
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

- GROUP BY split the table into different piles based on the value of each row


`@script`
The most interesting functions of SQL


---
## Practice time!

```yaml
type: "FinalSlide"
key: "b240739c0d"
```

`@script`


