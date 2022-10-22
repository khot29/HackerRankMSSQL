# HackerRankMSSQL

# Easy
- ## Write a query identifying the type of each record in the TRIANGLES table using its three side lengths. Output one of the following statements for each record in the table
```
select case
when A + B <= C or A + C <= B OR B + C <= A then 'Not A Triangle'
when A = B and B = C then 'Equilateral'
when A = B or B = C or A = C then 'Isosceles'
ELSE 'Scalene'
END
FROM TRIANGLES;
```

# Medium
- ## Consider P1(a,b) and P2(c,d) to be two points on a 2D plane.
```
select Cast(max(lat_n)-min(lat_n) + max(long_w)-min(long_w) as decimal(12,4)) from station
```


# Advance
- ## Amber's conglomerate corporation just acquired some new companies. Each of the companies follows this hierarchy
```
select c.company_code,c.founder,
Count(distinct(e.lead_manager_code)),
count(distinct(e.senior_manager_code)),
Count(distinct(e.manager_code)),
Count(distinct(e.employee_code))
from company as c
inner join employee as e
on  c.company_code = e.company_code
group by c.company_code,c.founder
order by c.company_code
```
