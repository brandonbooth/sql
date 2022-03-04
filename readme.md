# SQL programming Notes
by [Brandon Booth](https://brandon-booth.com/) - Winter 2022


## Table of Contents
- [GettingStarted](#GettingStarted)


**Helpful links:**
- https://www.hackerrank.com/


## GettingStarted

### Finding even and odd values
To find rows where a specified column has even values:
```
SELECT * 
FROM table_name 
WHERE mod(column_name,2) = 0;
```

To find rows where a specified column has odd values:
```
SELECT * 
FROM table_name 
WHERE mod(column_name,2) <> 0;
```

To find rows where a specified column has even values and remove duplicates:
```
Select DISTINCT City
from Station
WHERE mod(ID,2) = 0
```

To calculate difference in counts:
```
select (count(CITY)- count(distinct CITY)) 
from STATION
```

Select multiple items by length:
```
select CITY,LENGTH(CITY) from STATION order by Length(CITY) asc, CITY asc, CITY limit 1; 
select CITY,LENGTH(CITY) from STATION order by Length(CITY) desc, CITY asc, CITY limit 1; 
```

Query the list of items starting with characters (i.e., a, e, i, o, or u) with duplicates removed:
```
SELECT DISTINCT 
CITY 
FROM STATION 
WHERE lower(substr(CITY,1,1)) in ('a','e','i','o','u')
```


x:
```

```

:
```

```

:
```

```

:
```

```
