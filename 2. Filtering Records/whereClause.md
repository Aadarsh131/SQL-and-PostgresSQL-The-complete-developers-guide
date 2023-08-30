# WHERE clause to filter our data

```sql
SELECT *, population/area as density FROM cities WHERE area IN (4015, 2240)
```
> will show all the columns(*), including the new `density` column, of any rows which has `area` column's value as 4015 or 2240

<br>



```sql
SELECT *, population/area as density FROM cities WHERE population/area > 3000
```
> will filter out the rows based on `density` column, if its value is >3000
>
>
>**NOTE**:
>```sql
>SELECT *, population/area as density FROM cities WHERE density > 3000
>```
>> ERROR: ***column "density" does not exist***<br>

