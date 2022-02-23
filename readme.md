# SQL programming Notes
by [Brandon Booth](https://brandon-booth.com/) - Winter 2022


## Table of Contents
- [GettingStarted](#GettingStarted)


**Helpful links:**
- https://www.hackerrank.com/


## GettingStarted

### Finding even and odd values
To find rows where a specified column has even values:
SELECT * 
FROM table_name 
WHERE mod(column_name,2) = 0;

To find rows where a specified column has odd values:
<br />
SELECT * 
FROM table_name 
WHERE mod(column_name,2) <> 0;

To find rows where a specified column has even values and remove duplicates:
<br />
Select DISTINCT City
from Station
WHERE mod(ID,2) = 0

To calculate difference in counts:
<br />
select (count(CITY)- count(distinct CITY)) 
from STATION
