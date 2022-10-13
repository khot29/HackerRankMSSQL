# HackerRankMSSQL

# Easy
1 ## Write a query identifying the type of each record in the TRIANGLES table using its three side lengths. Output one of the following statements for each record in the table
```
select case
when A + B <= C or A + C <= B OR B + C <= A then 'Not A Triangle'
when A = B and B = C then 'Equilateral'
when A = B or B = C or A = C then 'Isosceles'
ELSE 'Scalene'
END
FROM TRIANGLES;
```

# Advance
1 ## Amber's conglomerate corporation just acquired some new companies. Each of the companies follows this hierarchy
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
