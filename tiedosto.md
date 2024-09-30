# Viikko 2 

### Tehtävä 1 Yhteen tauluun kohdistuvien kyselyiden harjoitukset
select * from goal;
![image](https://github.com/user-attachments/assets/7473ab71-c689-4cf7-a03b-fac2af4eb88f)

select name from airport where iso_country = "FI";
![image](https://github.com/user-attachments/assets/1660f6c0-3201-48db-82c8-f2a6ab8420c4)

select name from airport where iso_country = "FI" order by name asc;
![image](https://github.com/user-attachments/assets/00a1e3cc-0baa-4830-9345-768ced7433a7)

select name, type from airport where iso_country  = "FI" order by type asc, name asc;
![image](https://github.com/user-attachments/assets/d2652ac1-9a1e-4207-8514-9113625e9cea)

select name from country WHERE name LIKE "F%";
![image](https://github.com/user-attachments/assets/bb52c5c9-24a2-427a-915c-05e7a8f2b87b)

select name from country WHERE name LIKE "%F%";
![image](https://github.com/user-attachments/assets/f9959560-9365-4694-b769-2586490192c7)

select location from game where screen_name = "Vesa";
![image](https://github.com/user-attachments/assets/6f3c32dd-ea48-438e-b002-eef01a739b81)

select co2_consumed from game WHERE screen_name = "Ilkka";
![image](https://github.com/user-attachments/assets/c3c772fb-8a99-4792-b08e-f3045eb6f9e8)

select co2_budget from game limit 1;
![image](https://github.com/user-attachments/assets/cbfbf838-9087-4c47-ac2a-a4820d92dc96)

### tehtävä 2 Where-osan liitosehto harjoitukset

select country.name as "country name", airport.name as "airport name" from airport, country where airport.iso_country = country.iso_country and country.name = "Iceland";
![image](https://github.com/user-attachments/assets/e79d14b8-9524-4f58-a8fb-6ca9c680361c)

select airport.name as "airport name" from airport, country where airport.iso_country = country.iso_country and country.name = "France" and airport.type = "large_airport";
![image](https://github.com/user-attachments/assets/12446c6b-c153-4b5f-962f-420a2424e8e7)

select country.name as country_name, airport.name as airport_name from airport, country where airport.iso_country = country.iso_country and country.continent = "AN";
![image](https://github.com/user-attachments/assets/ead0c65c-25c2-493d-a342-f77f94b11cfe)

select elevation_ft from airport, game where location = ident and screen_name = "Heini";
![image](https://github.com/user-attachments/assets/7bfa76d7-afb7-4b41-96f5-00962055ab95)

select elevation_ft * 0.3048 as elevation_m from airport, game where location = ident and screen_name = "Heini";
![image](https://github.com/user-attachments/assets/fb22c739-34e7-46c3-99be-fea9eed092ad)

select name from airport, game where location = ident and screen_name = "Ilkka";
![image](https://github.com/user-attachments/assets/afd4bb90-5815-49b8-806f-24c9f2f9fbe8)

select country.name from airport,game, country where location = ident and airport.iso_country = country.iso_country and screen_name = "Ilkka";
![image](https://github.com/user-attachments/assets/d8e4659e-c1d9-4ee4-84f5-507e93a2ba9c)

select name from goal, goal_reached, game where game.id = game_id and goal.id = goal_id and screen_name = "Heini";
![image](https://github.com/user-attachments/assets/32991598-b7ed-4e7d-bb70-aafb1c5e0571)







