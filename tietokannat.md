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