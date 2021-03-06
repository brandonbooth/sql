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
or
```
SELECT DISTINCT city FROM station WHERE city REGEXP '^[aeiou]'
```

Query the list of items ending with characters (i.e., a, e, i, o, or u) with duplicates removed:
```
SELECT DISTINCT CITY FROM STATION
WHERE lcase(CITY) LIKE '%a'
OR lcase(CITY) LIKE '%e'
OR lcase(CITY) LIKE '%i'
OR lcase(CITY) LIKE '%o'
OR lcase(CITY) LIKE '%u'
ORDER BY CITY;
```
or
```
SELECT DISTINCT city FROM station WHERE city REGEXP '[aeiou]$'
```

Does not start with characters:
```
SELECT DISTINCT CITY 
FROM STATION
WHERE lcase(CITY) NOT LIKE 'a%'
AND lcase(CITY) NOT LIKE 'e%'
AND lcase(CITY) NOT LIKE 'i%'
AND lcase(CITY) NOT LIKE 'o%'
AND lcase(CITY) NOT LIKE 'u%'
```

```
SELECT DISTINCT CITY 
FROM STATION 
WHERE CITY NOT RLIKE '^[aeiouAEIOU].*$'
```

:
```

```
