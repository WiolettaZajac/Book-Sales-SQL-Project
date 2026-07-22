# Book Sales Analysis Using SQL

## Project Overview

This project explores a dataset of Amazon bestselling books from 2009 to 2019 using MySQL. 
The aim was to practise basic SQL skills by answering a range of questions about books, authors, prices, reviews and genres. 
This project helped me gain confidence in writing SQL queries and working with real-world data.

## Dataset

The dataset contains information about Amazon's bestselling books, including:

- Book title
- Author
- User rating
- Number of reviews
- Price
- Year of publication
- Genre

## Table Creation

I used following SQL statement to create the `book_sales` table.

```sql
CREATE TABLE book_sales (
    Name VARCHAR(255),
    Author VARCHAR(150),
    User_Rating DECIMAL(3,2),
    Reviews INT,
    Price INT,
    Year INT,
    Genre VARCHAR(50)
);
```

## Database Schema

This simple project uses a single table called `book_sales`. The table stores information about Amazon bestselling books, including the book title, author, user rating, number of reviews, price, year and genre.

![Database Schema](Screenshots/schema.png)

## Example SQL Query

The following query finds the top 10 authors with the most bestselling books.

```sql
SELECT Author,
       COUNT(*) AS Books
FROM book_sales
GROUP BY Author
ORDER BY Books DESC
LIMIT 10;
```

## Example SQL Query

The following query calculates the average price of books by genre.

```sql
SELECT Genre,
       ROUND(AVG(Price),2) AS Average_Price
FROM book_sales
GROUP BY Genre;
```

## Example SQL Query

The following query returns the 10 most reviewed books.

```sql
SELECT Name,
       Reviews
FROM book_sales
ORDER BY Reviews DESC
LIMIT 10;
```



## SQL Skills Used

Throughout this project, I used the following SQL concepts:

- SELECT
- WHERE
- ORDER BY
- GROUP BY
- HAVING
- COUNT()
- SUM()
- AVG()
- LIMIT

## Questions Answered

Some of the questions I answered include:

- Which books have the highest user ratings?
- Which books have the most reviews?
- What is the average price of a bestselling book?
- Which genre has the most bestselling books?
- Which authors appear most often in the dataset?
- How many bestselling books were published each year?

## What I Learned

This project gave me practical experience with SQL and helped me understand how to retrieve, filter, sort and summarise data. 
It also improved my confidence in using aggregate functions and writing queries to answer business-style questions.


## Conclusion

This was my first SQL project and a good introduction to analysing data with SQL. It strengthened my understanding of the basics and prepared me for working on more advanced SQL projects in the future.


## Source

Dataset: Amazon Top 50 Bestselling Books 2009–2019

Available from: https://www.kaggle.com/datasets/sootersaalu/amazon-top-50-bestselling-books-2009-2019
