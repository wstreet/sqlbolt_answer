# SQL Lesson 6: Multi-table queries with JOINs

## Find the domestic and international sales for each movie 
``` sql
SELECT movies.title, boxoffice.domestic_sales, boxoffice.international_sales
FROM movies
INNER JOIN boxoffice ON movies.id = boxoffice.movie_id;
```

## Show the sales numbers for each movie that did better internationally rather than domestically
``` sql
SELECT movies.title, boxoffice.domestic_sales, boxoffice.international_sales
FROM movies
INNER JOIN boxoffice ON movies.id = boxoffice.movie_id
WHERE international_sales > domestic_sales;
```

## List all the movies by their ratings in descending order
```sql
SELECT *
FROM movies
INNER JOIN boxoffice ON movies.id = boxoffice.movie_id
ORDER BY rating DESC
```