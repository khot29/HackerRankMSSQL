# HackerRankMSSQL

## Amber's conglomerate corporation just acquired some new companies. Each of the companies follows this hierarchy
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
