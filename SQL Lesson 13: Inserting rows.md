# SQL Lesson 13: Inserting rows

## Add the studio's new production, Toy Story 4 to the list of movies (you can use any director)
```sql
INSERT INTO movies (id, title, director, year, length_minutes) VALUES (4, "Toy Story 4", "John lasseter", "2023", 98)
```

## Toy Story 4 has been released to critical acclaim! It had a rating of 8.7, and made 340 million domestically and 270 million internationally. Add the record to the BoxOffice table
```sql
INSERT INTO boxoffice VALUES (4, 8.7, 3400000000, 2700000000)
```