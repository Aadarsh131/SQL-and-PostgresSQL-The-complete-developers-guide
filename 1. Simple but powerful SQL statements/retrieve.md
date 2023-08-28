 # Retrieve Table data

 1. **All rows**
 ```sql
 SELECT * FROM cities
 ```
 
 <br>

 2. **Calculated rows**
 ```sql
SELECT name, population/area FROM cities
 ```
 > - shows 2 columns of ``name`` and ``?column?``(a temp unnamed column name)
> - ``?column?`` contains the calculated value of divided value of `popluation` by `area`
 
 <br>

 ```sql
SELECT name, population/area AS density FROM cities
 ```
 > this will create the column name for storing `population/area` as `density`