# Insert single or multiple row

1. ***Single row***
```sql
INSERT INTO cities (name, country, population, area)
VALUES ('Tokyo', 'Japan', 38505000, 8223);
```

2. __*Multiple rows*__
```sql
INSERT INTO cities (name, country, population, area)
VALUES 
  ('Delhi', 'India', 28125000, 2240),
  ('Shanghai', 'China', 22125000, 4015),
  ('Sao Paulo', 'Brazil', 20935000, 3043);
```