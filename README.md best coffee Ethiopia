create database coffee_quality;
use coffee_quality;

## loading the table
select*
from coffee;

## to find number of duplicate in the table
select
species,
count(Species),
Owner,
Country_of_Origin,
Region,
Processing_Method,
Flavor,
Aftertaste
from coffee;

## changing the column name Processing_Method to creation
alter table coffee2 change Processing_Method creation varchar (25);

select*
from coffee2;

## best quality coffee in Ethiopia
select
species,
Owner,
Country_of_Origin,
Region,
creation,
Flavor,
Aftertaste,
best_quality
from coffee4
where best_quality > 17
## best quality coffee in ethiopia is specie Arabica, owner metad plc, region Oromiya, best quality number 17.25

create temporary table coffee4
select
species,
Owner,
Country_of_Origin,
Region,
creation,
Flavor,
Aftertaste,
Flavor + Aftertaste as best_quality
from coffee3;

create temporary table coffee3
select
species,
Owner,
Country_of_Origin,
Region,
creation,
Flavor,
Aftertaste
from coffee2
where
Country_of_Origin = 'Ethiopia';

## removing all duplicate found
create temporary table coffee2
select
distinct(Species),
Owner,
Country_of_Origin,
Region,
Processing_Method,
Flavor,
Aftertaste
from coffee;
