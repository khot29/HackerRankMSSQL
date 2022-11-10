## Query all columns for all American cities in the CITY table with populations larger than 100000. The CountryCode for America is USA.
- Select * from city 
  where population > 100000 and countrycode = "USA"


## Query the NAME field for all American cities in the CITY table with populations larger than 120000. The CountryCode for America is USA.
- select Name from city
  where population > 120000 and countrycode = "USA";
