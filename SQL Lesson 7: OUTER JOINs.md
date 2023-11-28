# SQL Lesson 7: OUTER JOINs

## Find the list of all buildings that have employees

```sql
SELECT DISTINCT buildings.building_name  FROM buildings
LEFT JOIN employees ON buildings.building_name = employees.building
WHERE employees.name IS NOT null;
```

## Find the list of all buildings and their capacity
```sql
SELECT * from buildings
```

## List all buildings and the distinct employee roles in each building (including empty buildings)
```sql

SELECT DISTINCT role, buildings.*  FROM buildings
LEFT JOIN employees  ON buildings.building_name = employees.building;
```