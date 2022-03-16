# Basic SQL
This contains the practice session of the SQL practicing from the Hackerrank. It is just the basic part of it. 
Practice Link: [basicsql.com](https://www.hackerrank.com/domains/sql?filters%5Bskills%5D%5B%5D=SQL%20%28Basic%29)

Questions and Queries will be written below.

**1.) Revisiting the Select Query I** 
```
select * from city where population>100000 and countrycode = 'USA';
```

**2.) Revisiting the Select Query II**
```
select name from city where population>120000 and countrycode = 'USA';
```

**3.) Select All**
```
select * from city; OR select all from city;
```

**4.) Select By ID** 
```
select * from city where ID = 1661;
```

**5.) Japanese Cities' Attributes** 
```
select * from city where countrycode = 'JPN';
```

**6.) Japanese Cities' Names**
```
select name from city where countrycode = 'JPN';
```

**7.) Weather Observation Station 1**
```
select city,state from station;
```

**8.) Weather Observation Station 3**
```
SELECT DISTINCT(CITY) FROM STATION WHERE (ID%2)=0 ;
```

**9.) Weather Observation Station 4**
```
select count(city) - count(distinct(city)) from station;
```

**10.) Weather Observation Station 5**


**11.) Weather Observation Station 6**
```
SELECT DISTINCT CITY FROM STATION WHERE LEFT(City,1) IN ('a','e','i','o','u');   [MYSQL]
```

**12.) Weather Observation Station 7**
```
SELECT DISTINCT CITY FROM STATION WHERE RIGHT(City,1) IN ('a','e','i','o','u');   [MYSQL]
```

**13.) Weather Observation Station 8**
```
SELECT DISTINCT CITY FROM STATION WHERE LEFT(City,1) IN ('a','e','i','o','u') AND RIGHT(City,1) IN ('a','e','i','o','u');    [MYSQL]
```

**14.) Weather Observation Station 9**
```
SELECT DISTINCT CITY FROM STATION WHERE LEFT(City,1) NOT IN ('a','e','i','o','u'); [MYSQL]
```

**15.) Weather Observation Station 10**
```
SELECT DISTINCT CITY FROM STATION WHERE RIGHT(City,1) NOT IN ('a','e','i','o','u');  [MYSQL]
```

**16.) Weather Observation Station 11**
```
SELECT DISTINCT CITY FROM STATION WHERE LEFT(City,1) not IN ('a','e','i','o','u') OR RIGHT(City,1) NOT IN ('a','e','i','o','u');    [MYSQL]
```


**17.) Weather Observation Station 12** 
```
select distinct city from station where city regexp '^[^aeiou].*[^aeiou]$'
```

**18.) Higher than 75 marks**
```
SELECT name FROM students WHERE marks>75 ORDER BY Right(name,3),id ASC; 
```

**19.) Employee Names**
```
SELECT name FROM Employee ORDER BY name ASC;
```

**20.) Employee Salaries**
```
SELECT name FROM Employee WHERE salary > 2000 and months < 10 ORDER BY employee_id ASC;
```

**21.) Types of Triangles**
```
SELECT CASE
        WHEN a+b>c AND b+c>a AND a+c>b THEN
            CASE
                WHEN a = b AND b = c THEN 'Equilateral'
                WHEN a = b OR b = c OR a = c THEN 'Isosceles'
                ELSE 'Scalene'
            END
        ELSE 'Not A Triangle'
    END
FROM TRIANGLES;
```

**22.) Revising Aggregate - The Count Function**
```
SELECT Count(name) from CITY where population > 100000;
```

**23.) Revising Aggregate - The Sum Function**
```
select sum(population) from city where district = 'California';
```

**24.) Revising Aggregate - Averages**
```
select avg(population) from city where district = 'California';
```

**25.) Revising Aggregate - Average Population**
```
select round(avg(population)) from city;
```

**26.) Japan Population**
select sum(population) from city where countrycode = 'JPN';

**27.) Population Density Difference**
select max(population) - min(population) from city;

**28.) The Blunder**
