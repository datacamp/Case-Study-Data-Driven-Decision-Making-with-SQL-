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
- `SELECT <Field Names> FROM <Table Name> ` 

- `SELECT * FROM <Table Name>`
 
- `SELECT <Field1>, <Field2>, <Field3> FROM <Table Name>`

## <PICTURE>

- Always remember to only retrieve columns that you need. 

- `SELECT *` may cause performance to suffer from the fact that your query pulls up too much data)


`@script`
- `SELECT <Field Names> FROM <Table Name> ` 

- `SELECT * FROM Sales`
 
- `SELECT Year,Publisher, Revenue FROM Sales`

## <PICTURE>

Always remember to only retrieve columns that you need (as it may cause performance to suffer from the fact that your query pulls up too much data)


---
## Case Studies: Video Games Global Sales database

```yaml
type: "FullSlide"
key: "9e2bb70cfe"
```

`@part1`
- Retrieve all columns from the Sales table

`SELECT * FROM SALES`

> Question:  give info


`@script`
First case study, a dataset from Video Game Global Sales. This dataset is based on a Kaggle's competition. Imagine that you work in a video game industry and you are tasked to carry out market research. Your job is to analyse sales trend. 

First, lets retrieve all columns from the Sales table by executing the SELECT statement here. As, mentioned in the previous slide, only retrieve the data that you need.


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


