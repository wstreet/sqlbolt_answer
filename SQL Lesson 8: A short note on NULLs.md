# SQL Lesson 8: A short note on NULLs

## Find the name and role of all employees who have not been assigned to a building
```sql
SELECT name, role FROM employees
WHERE building IS NULL;
```

## Find the names of the buildings that hold no employees
```sql
SELECT DISTINCT building_name FROM buildings
LEFT JOIN employees ON buildings.building_name = employees.building
WHERE name IS NULL;
```