# SQL Lesson 9: Queries with expressions

## List all movies and their combined sales in millions of dollars
```sql
SELECT title, (domestic_sales + international_sales) / 1000000 AS sales  FROM movies
JOIN boxoffice ON movies.id = boxoffice.movie_id;
```

## List all movies and their ratings in percent
```sql
SELECT title, rating * 10 AS rating FROM movies
JOIN boxoffice ON movies.id = boxoffice.movie_id
```

## List all movies that were released on even number years
```sql

SELECT * FROM movies
WHERE year % 2 = 0
```