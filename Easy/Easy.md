# Easy
- ## Given the CITY and COUNTRY tables, query the sum of the populations of all cities where the CONTINENT is 'Asia'.
     Note: CITY.CountryCode and COUNTRY.Code are matching key columns.
```
select sum(city.population) from city 
inner join country 
on city.countrycode = country.code
where country.continent = 'Asia';
```
