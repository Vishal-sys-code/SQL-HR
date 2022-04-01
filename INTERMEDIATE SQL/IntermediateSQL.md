**1.) Weather Observation Station 5**
```
SELECT CITY, LENGTH(CITY) FROM STATION
ORDER BY LENGTH(CITY), CITY ASC
LIMIT 1;
SELECT CITY, LENGTH(CITY) FROM STATION
ORDER BY LENGTH(CITY) DESC
LIMIT 1;
```

**2.) Binary Tree Nodes**
```
SELECT CASE
    WHEN P is NULL THEN CONCAT (N, ' Root')
    WHEN N in (SELECT DISTINCT P FROM BST) THEN CONCAT (N,' Inner')
    ELSE CONCAT(N,' Leaf')
END
from BST
order by N asc;
```