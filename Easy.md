#### Reversing the select query I
## Query all columns for all American cities in the CITY table with populations larger than 100000. The CountryCode for America is USA.
- Select * from city 
  where population > 100000 and countrycode = "USA"

--------------------------------------------------------------------------------------------------------------------------------------------------------------------
#### Reversing the select query II
## Query the NAME field for all American cities in the CITY table with populations larger than 120000. The CountryCode for America is USA.
- select Name from city
  where population > 120000 and countrycode = "USA";
--------------------------------------------------------------------------------------------------------------------------------------------------------------------

## Query all columns (attributes) for every row in the CITY table.
- Select * from City
--------------------------------------------------------------------------------------------------------------------------------------------------------------------

## Query all columns for a city in CITY with the ID 1661.
- select * from city 
  where id = 1661
  
## Query all attributes of every Japanese city in the CITY table. The COUNTRYCODE for Japan is JPN.
- select * from city 
  where countrycode = "JPN"
