# Yhteen tauluun kohdistuvat kyselyt


### Tehtävä 1
select * from goal;
![screenshot](https://github.com/TazzaLakuKahvi/Tietokannat/blob/main/MariaDB_Screenshots/osio1kuva1.png)
### Tehtävä 2
select name, type from airport where iso_country = "FI";
![screenshot](https://github.com/TazzaLakuKahvi/Tietokannat/blob/main/MariaDB_Screenshots/osio1kuva2.png)
### Tehtävä 3
select name from airport where iso_country = "FI" order by name asc;
![screenshot](https://github.com/TazzaLakuKahvi/Tietokannat/blob/main/MariaDB_Screenshots/osio1kuva3.png)
### Tehtävä 4
select name, type from airport where iso_country = "FI" order by type asc, name asc;
![screenshot](https://github.com/TazzaLakuKahvi/Tietokannat/blob/main/MariaDB_Screenshots/osio1kuva4.png)
### Tehtävä 5
select name from country where name like "f%";
![screenshot](https://github.com/TazzaLakuKahvi/Tietokannat/blob/main/MariaDB_Screenshots/osio1kuva5.png)
### Tehtävä 6
select name from country where name like "%f%";
![screenshot](https://github.com/TazzaLakuKahvi/Tietokannat/blob/main/MariaDB_Screenshots/osio1kuva6.png)
### Tehtävä 7
select location from game where screen_name = "Vesa";
![screenshot](https://github.com/TazzaLakuKahvi/Tietokannat/blob/main/MariaDB_Screenshots/osio1kuva7.png)
### Tehtävä 8
select co2_consumed from game where screen_name = "Ilkka";
![screenshot](https://github.com/TazzaLakuKahvi/Tietokannat/blob/main/MariaDB_Screenshots/osio1kuva8.png)
### Tehtävä 9
select co2_budget from game where id = "1";
![screenshot](https://github.com/TazzaLakuKahvi/Tietokannat/blob/main/MariaDB_Screenshots/osio1kuva9.png)


# Where osan liitosehto


### Tehtävä 1
select country.name as "country name", airport.name "airport name"
from country, airport
where country.iso_country = airport.iso_country
and airport.iso_country = "IS";
![screenshot](https://github.com/TazzaLakuKahvi/Tietokannat/blob/main/MariaDB_Screenshots/osio2kuva1.png)
### Tehtävä 2
select name as "airport name"
from airport
where iso_country = "FR"
and type = "large_airport";
![screenshot](https://github.com/TazzaLakuKahvi/Tietokannat/blob/main/MariaDB_Screenshots/osio2kuva2.png)
### Tehtävä 3
select country.name as "country_name", airport.name as "airport_name"
from country, airport
where country.iso_country = airport.iso_country
and airport.iso_country = "AN";
![screenshot](https://github.com/TazzaLakuKahvi/Tietokannat/blob/main/MariaDB_Screenshots/osio2kuva3.png)
### Tehtävä 4
select elevation_ft
from airport, game
where game.location = airport.ident
and game.screen_name = "Heini";
![screenshot](https://github.com/TazzaLakuKahvi/Tietokannat/blob/main/MariaDB_Screenshots/osio2kuva4.png)
### Tehtävä 5
select elevation_ft*0.3048 as "elevation_m"
from game, airport
where game.location = airport.ident
and game.screen_name = "Heini";
![screenshot](https://github.com/TazzaLakuKahvi/Tietokannat/blob/main/MariaDB_Screenshots/osio2kuva5.png)
### Tehtävä 6
select airport.name
from airport, game
where airport.ident = game.location
and game.screen_name = "Ilkka";
![screenshot](https://github.com/TazzaLakuKahvi/Tietokannat/blob/main/MariaDB_Screenshots/osio2kuva6.png)
### Tehtävä 7
select country.name
from country, game, airport
where game.location = airport.ident
and game.screen_name = "Ilkka"
and country.iso_country = airport.iso_country;
![screenshot](https://github.com/TazzaLakuKahvi/Tietokannat/blob/main/MariaDB_Screenshots/osio2kuva7.png)
### Tehtävä 8
select goal.name
from goal, goal_reached, game
where goal.id = goal_reached.goal_id
and goal_reached.game_id = game.id
and game.screen_name = "Heini";
![screenshot](https://github.com/TazzaLakuKahvi/Tietokannat/blob/main/MariaDB_Screenshots/osio2kuva8.png)
### Tehtävä 9
select airport.name
from airport, goal, game
where goal.name = "ClOUDS"
and game.location = airport.ident
and game.screen_name = "Ilkka";
![screenshot](https://github.com/TazzaLakuKahvi/Tietokannat/blob/main/MariaDB_Screenshots/osio2kuva9.png)
### Tehtävä 10
select country.name
from country, airport, goal, game
where goal.name = "ClOUDS"
and game.location = airport.ident
and country.iso_country = airport.iso_country
and game.screen_name = "Ilkka";
![screenshot](https://github.com/TazzaLakuKahvi/Tietokannat/blob/main/MariaDB_Screenshots/osio2kuva10.png)
