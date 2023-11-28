# SQL Review5: Simple SELECT Queries

## List all the Canadian cities and their populations
```sql
SELECT * FROM north_american_cities
WHERE country = "Canada";
```

## Order all the cities in the United States by their latitude from north to south
```sql
SELECT city FROM north_american_cities where country = "United States" order by latitude desc;

```

## List all the cities west of Chicago, ordered from west to east
```sql
SELECT * FROM north_american_cities
WHERE Longitude < -87.629798
ORDER BY longitude ASC
```

## List the two largest cities in Mexico (by population) 

```sql
SELECT * FROM north_american_cities
WHERE Country = "Mexico"
ORDER BY Population DESC
LIMIT 2
```

## List the third and fourth largest cities (by population) in the United States and their population
```sql
SELECT * FROM north_american_cities
WHERE Country = "United States"
ORDER BY Population DESC
LIMIT 2 OFFSET 2
```