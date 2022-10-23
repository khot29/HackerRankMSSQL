# HackerRankMSSQL

# Easy
- ## Given the CITY and COUNTRY tables, query the sum of the populations of all cities where the CONTINENT is 'Asia'.
     Note: CITY.CountryCode and COUNTRY.Code are matching key columns.
```
select sum(city.population) from city 
inner join country 
on city.countrycode = country.code
where country.continent = 'Asia';
```

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
- ## A median is defined as a number separating the higher half of a data set from the lower half. Query the median of the Northern Latitudes (LAT_N) from STATION and round your answer to 4 decimal places.
```
select top 1 tableT.uniqueV from (select top 50 percent cast(lat_n as decimal(12,4))uniqueV  from station order by lat_n) as tableT
order by tableT.uniqueV desc
```
- ## You are given two tables: Students and Grades. Students contains three columns ID, Name and Marks.
```
select 
case 
when grades.grade < 8 then null
else Students.Name
end,
grades.Grade,Students.Marks
from Students, grades
where Students.Marks >= grades.min_mark and Students.Marks <= grades.max_mark
order by grades.Grade desc,Students.Name
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
