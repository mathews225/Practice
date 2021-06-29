# SELECT from WORLD Tutorial
### https://sqlzoo.net/wiki/SELECT_from_WORLD_Tutorial

| name        | continent |    area | population |          gdp |
| ----------- | --------- | ------: | ---------: | -----------: |
| Afghanistan | Asia      |  652230 |   25500100 |  20343000000 |
| Albania     | Europe    |   28748 |    2831741 |  12960000000 |
| Algeria     | Africa    | 2381741 |   37100000 | 188681000000 |
| Andorra     | Europe    |     468 |      78115 |   3712000000 |
| Angola      | Africa    | 1246700 |   20609294 | 100990000000 |

> In this tutorial you will use the SELECT command on the table world:

## Introduction
_Observe the result of running this SQL command to show the name, continent and population of all countries._

``` sql
SELECT
    name
    , continent
    , population
  FROM world;
```
| name                          | continent     | population |
| ----------------------------- | ------------- | ---------: |
| Afghanistan                   | Asia          |   25500100 |
| Albania                       | Europe        |    2821977 |
| Algeria                       | Africa        |   38700000 |
| Andorra                       | Europe        |      76098 |
| Angola                        | Africa        |   19183590 |
| Antigua and Barbuda           | Caribbean     |      86295 |
| Argentina                     | South America |   42669500 |
| Armenia                       | Eurasia       |    3017400 |
| Australia                     | Oceania       |   23545500 |
| Austria                       | Europe        |    8504850 |
| Azerbaijan                    | Asia          |    9477100 |
| Bahamas                       | Caribbean     |     351461 |
| Bahrain                       | Asia          |    1234571 |
| Bangladesh                    | Asia          |  156557000 |
| Barbados                      | Caribbean     |     285000 |
| Belarus                       | Europe        |    9467000 |
| Belgium                       | Europe        |   11198638 |
| Belize                        | North America |     349728 |
| Benin                         | Africa        |    9988068 |
| Bhutan                        | Asia          |     749090 |
| Bolivia                       | South America |   10027254 |
| Bosnia and Herzegovina        | Europe        |    3791622 |
| Botswana                      | Africa        |    2024904 |
| Brazil                        | South America |  202794000 |
| Brunei                        | Asia          |     393162 |
| Bulgaria                      | Europe        |    7245677 |
| Burkina Faso                  | Africa        |   17322796 |
| Burundi                       | Africa        |    9420248 |
| Cambodia                      | Asia          |   15184116 |
| Cameroon                      | Africa        |   20386799 |
| Canada                        | North America |   35427524 |
| Cape Verde                    | Africa        |     491875 |
| Central African Republic      | Africa        |    4709000 |
| Chad                          | Africa        |   13211000 |
| Chile                         | South America |   17773000 |
| China                         | Asia          | 1365370000 |
| Colombia                      | South America |   47662000 |
| Comoros                       | Africa        |     743798 |
| Congo, Democratic Republic of | Africa        |   69360000 |
| Congo, Republic of            | Africa        |    4559000 |
| Costa Rica                    | North America |    4667096 |
| Côte d'Ivoire                 | Africa        |   23919000 |
| Croatia                       | Europe        |    4290612 |
| Cuba                          | Caribbean     |   11167325 |
| Cyprus                        | Asia          |     865878 |
| Czech Republic                | Europe        |   10517400 |
| Denmark                       | Europe        |    5634437 |
| Djibouti                      | Africa        |     886000 |
| Dominica                      | Caribbean     |      71293 |
| Dominican Republic            | Caribbean     |    9445281 |


## Large Countries
_Show the name for the countries that have a population of at least 200 million. 200 million is 200000000, there are eight zeros._

``` sql
SELECT name
FROM world
WHERE
    population > 200000000;
```

| name          |
| ------------- |
| Brazil        |
| China         |
| India         |
| Indonesia     |
| United States |

## Per capita GDP
_Give the name and the per capita GDP for those countries with a population of at least 200 million._

```SQL
SELECT
    name
    , gdp/population as 'per capita GDP'
FROM world
WHERE
    population _200000000
```

| name          | per capita GDP     |
| ------------- | ------------------ |
| Brazil        | 11115.264751422625 |
| China         | 6121.710598592322  |
| India         | 1504.793124478397  |
| Indonesia     | 3482.020488188676  |
| United States | 51032.29454636844  |


## South America In millions
_Show the name and population in millions for the countries of the continent 'South America'. Divide the population by 1000000 to get population in millions._

``` sql
SELECT
    name
    , population/1000000 as population
FROM world
WHERE
    continent = 'South America';
```
<table class="sqlmine"><tr><th>name</th><th>population</th></tr><tr><td>Argentina</td><td class="r">42.6695</td></tr><tr><td>Bolivia</td><td class="r">10.027254</td></tr><tr><td>Brazil</td><td class="r">202.794</td></tr><tr><td>Chile</td><td class="r">17.773</td></tr><tr><td>Colombia</td><td class="r">47.662</td></tr><tr><td>Ecuador</td><td class="r">15.7742</td></tr><tr><td>Guyana</td><td class="r">0.784894</td></tr><tr><td>Paraguay</td><td class="r">6.783374</td></tr><tr><td>Peru</td><td class="r">30.475144</td></tr><tr><td>Saint Vincent and the Grenadines</td><td class="r">0.109</td></tr><tr><td>Suriname</td><td class="r">0.534189</td></tr><tr><td>Uruguay</td><td class="r">3.286314</td></tr><tr><td>Venezuela</td><td class="r">28.946101</td></tr></table>

## France, Germany, Italy
_Show the name and population for France, Germany, Italy_

``` sql
SELECT
    name
    , population
FROM world
WHERE
    name IN ('France', 'Germany', 'Italy');
```
| name    | population |
| ------- | ---------: |
| France  |   65906000 |
| Germany |   80716000 |
| Italy   |   60782668 |

## United
_Show the countries which have a name that includes the word 'United'_


``` sql
SELECT name
FROM world
WHERE
    name LIKE '%United%';
```
| name                 |
| -------------------- |
| United Arab Emirates |
| United Kingdom       |
| United States        |


## Two ways to be big
_Two ways to be big: A country is big if it has an area of more than 3 million sq km or it has a population of more than 250 million._

_Show the countries that are big by area or big by population. Show name, population and area._

``` sql
SELECT
    name
    , population
    , area
FROM world
WHERE
    population > 250000000
      OR
    area > 3000000;
```
| name          | population |     area |
| ------------- | ---------: | -------: |
| Australia     |   23545500 |  7692024 |
| Brazil        |  202794000 |  8515767 |
| Canada        |   35427524 |  9984670 |
| China         | 1365370000 |  9596961 |
| India         | 1246160000 |  3166414 |
| Indonesia     |  252164800 |  1904569 |
| Russia        |  146000000 | 17125242 |
| United States |  318320000 |  9826675 |

## One or the other (but not both)
_Exclusive OR (XOR). Show the countries that are big by area (more than 3 million) or big by population (more than 250 million) but not both. Show name, population and area._

- _Australia has a big area but a small population, it should be included._
- Indonesia has a big population but a small area, it should be included._
- China has a big population and big area, it should be excluded._
- United Kingdom has a small population and a small area, it should be excluded._

``` sql
SELECT
    name
    , population
    , area
FROM world
WHERE
    (population > 250000000
      OR
    area > 3000000) 
      AND NOT
    (population > 250000000
         AND
        area > 3000000 );
```
| name      | population |     area |
| --------- | ---------: | -------: |
| Australia |   23545500 |  7692024 |
| Brazil    |  202794000 |  8515767 |
| Canada    |   35427524 |  9984670 |
| Indonesia |  252164800 |  1904569 |
| Russia    |  146000000 | 17125242 |

## Rounding
_Show the name and population in millions and the GDP in billions for the countries of the continent 'South America'. Use the ROUND function to show the values to two decimal places._

_For South America show population in millions and GDP in billions both to 2 decimal places._

``` sql
SELECT 
    name
    , ROUND(population/1000000,2) as 'pop.'
    , ROUND(gdp/1000000000,2) as gdp
FROM world
WHERE
    continent = 'South America';
```
| name                             |   pop. |     gdp |
| -------------------------------- | -----: | ------: |
| Argentina                        |  42.67 |  477.03 |
| Bolivia                          |  10.03 |   27.04 |
| Brazil                           | 202.79 | 2254.11 |
| Chile                            |  17.77 |  268.31 |
| Colombia                         |  47.66 |  369.81 |
| Ecuador                          |  15.77 |    87.5 |
| Guyana                           |   0.78 |    2.85 |
| Paraguay                         |   6.78 |   25.94 |
| Peru                             |  30.48 |  204.68 |
| Saint Vincent and the Grenadines |   0.11 |    0.69 |
| Suriname                         |   0.53 |    5.01 |
| Uruguay                          |   3.29 |   49.92 |
| Venezuela                        |  28.95 |  382.42 |

## Trillion dollar economies
_Show the name and per-capita GDP for those countries with a GDP of at least one trillion (1000000000000; that is 12 zeros). Round this value to the nearest 1000._

_Show per-capita GDP for the trillion dollar countries to the nearest $1000._

``` sql
SELECT
    name
    , ROUND(gdp/population,-3) AS 'gdp per cap.'
FROM world
WHERE
    gdp > 1000000000000;
```
| name           | gdp per cap. |
| -------------- | -----------: |
| Australia      |        66000 |
| Brazil         |        11000 |
| Canada         |        45000 |
| China          |         6000 |
| France         |        40000 |
| Germany        |        42000 |
| India          |         2000 |
| Italy          |        33000 |
| Japan          |        47000 |
| Mexico         |        10000 |
| Russia         |        14000 |
| South Korea    |        22000 |
| Spain          |        28000 |
| United Kingdom |        39000 |
| United States  |        51000 |

## Name and capital have the same length
_Greece has capital Athens._

_Each of the strings 'Greece', and 'Athens' has 6 characters._

_Show the name and capital where the name and the capital have the same number of characters._

``` sql
SELECT 
    name
    , capital
FROM world
WHERE 
    LEN(name) = LEN(capital);
```
| name       | capital    |
| ---------- | ---------- |
| Algeria    | Algiers    |
| Angola     | Luanda     |
| Armenia    | Yerevan    |
| Botswana   | Gaborone   |
| Canada     | Ottowa     |
| Djibouti   | Djibouti   |
| Egypt      | Cairo      |
| Estonia    | Tallinn    |
| Fiji       | Suva       |
| Gambia     | Banjul     |
| Georgia    | Tbilisi    |
| Ghana      | Accra      |
| Greece     | Athens     |
| Luxembourg | Luxembourg |
| Mauritania | Nouakchott |
| Paraguay   | Asunción   |
| Peru       | Lima       |
| Poland     | Warsaw     |
| Russia     | Moscow     |
| Rwanda     | Kigali     |
| San Marino | San Marino |
| Singapore  | Singapore  |
| Taiwan     | Taipei     |
| Togo       | Lomé       |
| Turkey     | Ankara     |
| Zambia     | Lusaka     |


## Matching name and capital

_The capital of Sweden is Stockholm. Both words start with the letter 'S'._

_Show the name and the capital where the first letters of each match. Don't include countries where the name and the capital are the same word._

``` sql
SELECT 
    name
    , capital
FROM
    world
    WHERE LEFT(capital,1) LIKE LEFT(name,1)
      AND
    name <> capital;
```
<table><tr><th>name</th><th>capital</th></tr><tr><td>Algeria</td><td>Algiers</td></tr><tr><td>Andorra</td><td>Andorra la Vella</td></tr><tr><td>Barbados</td><td>Bridgetown</td></tr><tr><td>Belize</td><td>Belmopan</td></tr><tr><td>Brazil</td><td>Brasília</td></tr><tr><td>Brunei</td><td>Bandar Seri Begawan</td></tr><tr><td>Burundi</td><td>Bujumbura</td></tr><tr><td>Guatemala</td><td>Guatemala City</td></tr><tr><td>Guyana</td><td>Georgetown</td></tr><tr><td>Kuwait</td><td>Kuwait City</td></tr><tr><td>Maldives</td><td>Malé</td></tr><tr><td>Marshall Islands</td><td>Majuro</td></tr><tr><td>Mexico</td><td>Mexico City</td></tr><tr><td>Monaco</td><td>Monaco-Ville</td></tr><tr><td>Mozambique</td><td>Maputo</td></tr><tr><td>Niger</td><td>Niamey</td></tr><tr><td>Panama</td><td>Panama City</td></tr><tr><td>Papua New Guinea</td><td>Port Moresby</td></tr><tr><td>Sao Tomé and Príncipe</td><td>São Tomé</td></tr><tr><td>South Korea</td><td>Seoul</td></tr><tr><td>Sri Lanka</td><td>Sri Jayawardenepura Kotte</td></tr><tr><td>Sweden</td><td>Stockholm</td></tr><tr><td>Taiwan</td><td>Taipei</td></tr><tr><td>Tunisia</td><td>Tunis</td></tr></table>

## All the vowels

_Equatorial Guinea and Dominican Republic have all of the vowels (a e i o u) in the name. They don't count because they have more than one word in the name._

_Find the country that has all the vowels and no spaces in its name._


``` sql
SELECT name
FROM world
WHERE 
    name LIKE '%a%'
      AND 
    name LIKE '%e%'
      AND 
    name LIKE '%i%'
      AND 
    name LIKE '%o%'
      AND 
    name LIKE '%u%'
      AND 
    name NOT LIKE '% %'
```
<table class="sqlmine"><tr><th>name</th></tr><tr><td>Mozambique</td></tr></table>