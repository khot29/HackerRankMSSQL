# Basic Select
#### Reversing the select query I
### Query all columns for all American cities in the CITY table with populations larger than 100000. The CountryCode for America is USA.
- Select * from city 
  where population > 100000 and countrycode = "USA"

--------------------------------------------------------------------------------------------------------------------------------------------------------------------

#### Reversing the select query II
### Query the NAME field for all American cities in the CITY table with populations larger than 120000. The CountryCode for America is USA.
- select Name from city
  where population > 120000 and countrycode = "USA";
--------------------------------------------------------------------------------------------------------------------------------------------------------------------

#### Select ALL
### Query all columns (attributes) for every row in the CITY table.
- Select * from City
--------------------------------------------------------------------------------------------------------------------------------------------------------------------

#### Select by ID
### Query all columns for a city in CITY with the ID 1661.
- select * from city 
  where id = 1661
 --------------------------------------------------------------------------------------------------------------------------------------------------------------------
 
#### Japanese Cities Attributes
### Query all attributes of every Japanese city in the CITY table. The COUNTRYCODE for Japan is JPN.
- select * from city 
  where countrycode = "JPN"
 --------------------------------------------------------------------------------------------------------------------------------------------------------------------
 
#### Japanese Cities' Names
### Query the names of all the Japanese cities in the CITY table. The COUNTRYCODE for Japan is JPN.
- Select name from city 
  where countrycode = "JPN"
 --------------------------------------------------------------------------------------------------------------------------------------------------------------------
 
#### Weather Observation Station 1
### Query a list of CITY and STATE from the STATION table.
- select city , state from station
 --------------------------------------------------------------------------------------------------------------------------------------------------------------------

#### Weather Observation Station 3
### Query a list of CITY names from STATION for cities that have an even ID number. Print the results in any order, but exclude duplicates from the answer.
- select distinct(city) from station 
  where id % 2 = 0;
 --------------------------------------------------------------------------------------------------------------------------------------------------------------------
 
#### Weather Observation Station 4
### Find the difference between the total number of CITY entries in the table and the number of distinct CITY entries in the table.
- select count(city) - count(distinct(city)) from station
 --------------------------------------------------------------------------------------------------------------------------------------------------------------------

#### Weather Observation Station 5
### Query the two cities in STATION with the shortest and longest CITY names, as well as their respective lengths (i.e.: number of characters in the name). If there is more than one smallest or largest city, choose the one that comes first when ordered alphabetically.
- select top 1 city, len(city) from station
  order by len(city),city;
- select top 1 city, len(city) from station
  order by len(city) desc;
 --------------------------------------------------------------------------------------------------------------------------------------------------------------------

#### Weather Observation Station 6
### Query the list of CITY names starting with vowels (i.e., a, e, i, o, or u) from STATION. Your result cannot contain duplicates.
- select city from station 
  where city like "[aeiou]%"
