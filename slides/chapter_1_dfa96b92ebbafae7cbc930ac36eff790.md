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
## Basic SQL Query

```yaml
type: "FullSlide"
key: "5ee4acfdd2"
```

`@part1`
- Retrieving data using SELECT keyword {{1}}

- Summarising data with SQL aggregated functions {{2}}

- Difference type of JOINs when working with multiple tables {{3}}


`@script`
- Retrieving data using SELECT keyword (typical first task to perform on data analysis is to retrieve data, you will use SELECT statement to perform this task) 

more advanced queries that include ) SQL aggregated functions
Difference type of JOINs when working with multiple tables


---
## Case Studies

```yaml
type: "FullSlide"
key: "9e2bb70cfe"
```

`@part1`
1. Video Games Sales
2. Speed Dating Experiment
3. Daily Happiness and Staff Turnover
4. Refugee Analysis


`@script`



---
## Basic SQL query

```yaml
type: "FullCodeSlide"
key: "fdaac2c0b1"
```

`@part1`
You will learn:

- Build a basic query using `SELECT` keyword

- List of columns and expressions

- `FROM` clause

- `WHERE` and `ORDER BY`

`SELECT <column or column expression>`

`SELECT Rank, Name, Platform, Year, Genre FROM SALES`


`@script`
Select statement begins with the SELECT keyword followed by a column or list of columns you wish to include in the result set.

For example, you can choose a single column from a table sales using this expression

[code]

To complete this query statement, you will add FROM clause. In this chapter you will use statements that have just a single table following FROM clause.

The WHERE and ORDER BY clause are optional and can be used to filter and sort the data which will be explained in later chapters.

For this chapter, you'll be using a database containing Kaggle's Video Game Global Sales information. To the right, underneath the editor, you can see the data in this a table of the database


---
## Case Study: Video Game Sales Analysis

```yaml
type: "FullSlide"
key: "84c343c104"
```

`@part1`
`SELECT` statement be followed by columns and or expression

- `JP_Sales + - EU_Sales`

WHERE clause can use logical operators such as AND, OR to filter  only rows where conditions in WHERE clause is met will return in there result.


`@script`



---
## Let's get practice!

```yaml
type: "FinalSlide"
key: "b240739c0d"
```

`@script`


