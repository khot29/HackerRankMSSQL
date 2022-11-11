# Basic Select
#### Reversing the select query I
### Query all columns for all American cities in the CITY table with populations larger than 100000. The CountryCode for America is USA.
```
  Select * from city 
  where population > 100000 and countrycode = "USA"
```
<HR>

#### Reversing the select query II
### Query the NAME field for all American cities in the CITY table with populations larger than 120000. The CountryCode for America is USA.
```
  select Name from city
  where population > 120000 and countrycode = "USA";
```
<HR>

#### Select ALL
### Query all columns (attributes) for every row in the CITY table.
```
  Select * from City
```
<HR>

#### Select by ID
### Query all columns for a city in CITY with the ID 1661.
```
  select * from city 
  where id = 1661
```
 <HR>
 
#### Japanese Cities Attributes
### Query all attributes of every Japanese city in the CITY table. The COUNTRYCODE for Japan is JPN.
```
  select * from city 
  where countrycode = "JPN"
```
 <HR>
 
#### Japanese Cities' Names
### Query the names of all the Japanese cities in the CITY table. The COUNTRYCODE for Japan is JPN.
```
  Select name from city 
  where countrycode = "JPN"
```
 <HR>
 
#### Weather Observation Station 1
### Query a list of CITY and STATE from the STATION table.
```
  select city , state from station
```
 <HR>

#### Weather Observation Station 3
### Query a list of CITY names from STATION for cities that have an even ID number. Print the results in any order, but exclude duplicates from the answer.
```
  select distinct(city) from station 
  where id % 2 = 0;
```
 <HR>
 
#### Weather Observation Station 4
### Find the difference between the total number of CITY entries in the table and the number of distinct CITY entries in the table.
```
  select count(city) - count(distinct(city)) from station
```
 <HR>

#### Weather Observation Station 5
### Query the two cities in STATION with the shortest and longest CITY names, as well as their respective lengths (i.e.: number of characters in the name). If there is more than one smallest or largest city, choose the one that comes first when ordered alphabetically.
```
  select top 1 city, len(city) from station
  order by len(city),city;
  select top 1 city, len(city) from station
  order by len(city) desc;
```
 <HR>

#### Weather Observation Station 6
### Query the list of CITY names starting with vowels (i.e., a, e, i, o, or u) from STATION. Your result cannot contain duplicates.
```
  select city from station 
  where city like "[aeiou]%"
```
<HR>
  
#### Weather Observation Station 7
### Query the list of CITY names ending with vowels (a, e, i, o, u) from STATION. Your result cannot contain duplicates.
```
  select distinct(city) from station 
  where city like "%[aeiou]"
```
 <HR>
  
#### Weather Observation Station 8
### Query the list of CITY names from STATION which have vowels (i.e., a, e, i, o, and u) as both their first and last characters. Your result cannot contain duplicates.
```
  select distinct(city) from station 
  where city like "[aeiou]%" and city like "%[aeiou]";
```
<HR>
  
#### Weather Observation Station 9
### Query the list of CITY names from STATION that do not start with vowels. Your result cannot contain duplicates.
```
  select distinct(city) from station 
  where city not like "[aeiou]%";
```
<HR>

#### Weather Observation Station 10
### Query the list of CITY names from STATION that do not start with vowels. Your result cannot contain duplicates.
```
  select distinct(city) from station 
  where city not like "%[aeiou]";
```
<HR>
  
#### Weather Observation Station 11
### Query the list of CITY names from STATION that either do not start with vowels or do not end with vowels. Your result cannot contain duplicates.
```
  select distinct(city) from station 
  where city not like "[aeiou]%" or city not like "%[aeiou]";
```
<HR>
  
#### Weather Observation Station 12
### Query the list of CITY names from STATION that do not start with vowels and do not end with vowels. Your result cannot contain duplicates.
```
  select distinct(city) from station 
  where city not like "[aeiou]%" and city not like "%[aeiou]";
```
<HR>
  
#### Higher Than 75 Marks
### Query the Name of any student in STUDENTS who scored higher than 75 Marks. Order your output by the last three characters of each name. If two or more students both have names ending in the same last three characters (i.e.: Bobby, Robby, etc.), secondary sort them by ascending ID.
```
  select name from students
  where marks > 75
  order by right(name,3),id
```
