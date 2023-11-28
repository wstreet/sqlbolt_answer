# SQL Lesson 12: Order of execution of a Query

## Find the number of movies each director has directed
```sql
SELECT director, count(*) FROM movies
GROUP BY director;
```


## Find the total domestic and international sales that can be attributed to each director

```sql
SELECT director, SUM(Domestic_sales + International_sales) FROM movies
 JOIN boxoffice ON Movies.id = Boxoffice.movie_id
GROUP BY director;
```