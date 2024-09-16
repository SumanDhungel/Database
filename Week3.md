# Database
#week 3 
#ex2 Qno.1
select * from goal ;

 <img width="806" alt="Screenshot Exercise 2- Question1" src="https://github.com/user-attachments/assets/f78413eb-502b-4fca-b51d-f9ae76211163">

#ex2 Qno.2
select name from airport where iso_country = "FI";

<img width="515" alt="Screenshot Exercise2 - Question 2" src="https://github.com/user-attachments/assets/d0e8a038-a758-464a-baa1-23f6449aaf03">

#ex2 Qno.3
select name from airport where iso_country = "FI" order by name asc;

<img width="638" alt="Screenshot Exercise 2 - Question3" src="https://github.com/user-attachments/assets/91026488-b5c0-4dba-9233-da5344ed09d0">

#ex2 Qno.4
select name, type from airport where iso_country = "FI" order by type, name;

<img width="688" alt="Screenshot Exercise 2 - Question 4" src="https://github.com/user-attachments/assets/31a5c6d2-08ad-415e-a2b5-49405ef0bf8e">

#ex2 Qno.5
select name from country where name like "F%";

<img width="482" alt="Screenshot Exercise 2 Question5" src="https://github.com/user-attachments/assets/5e25b48c-e654-4a65-9e8e-7e45798893bc">

#ex2 Qno.6
select name from country where name like "%F%";

<img width="490" alt="Screenshot Exercise 2- Question6" src="https://github.com/user-attachments/assets/17d59342-c060-4102-87c3-4ed486843ee5">

#ex2 Qno.7
select location from game where screen_name = "Vesa";

<img width="536" alt="Screenshot Exercise 2- Question7" src="https://github.com/user-attachments/assets/814215be-7a48-4bde-8118-a2fe31c5e10e">

#ex2 Qno.8
select co2_consumed from game where screen_name = "Ilkka";

<img width="572" alt="Screenshot Exercise2- Question8" src="https://github.com/user-attachments/assets/24ad5a50-403a-46bb-9dcd-85187bcaabe1">

#ex2 Qno.9
select distinct co2_budget from game;

<img width="419" alt="Screenshot Exercise2- Question9" src="https://github.com/user-attachments/assets/8ad1f420-3765-4be0-b31b-08b6d7416b82">

#ex2 Qno.10
set @co2_left := 0;
select screen_name, co2_budget, co2_consumed, (co2_budget - co2_consumed) as co2_left from game where screen_name = "Ilkka";

<img width="950" alt="Screenshot Exercise2 - Question10" src="https://github.com/user-attachments/assets/ae9ec797-de9a-4ba9-922b-e5e826091963">



#ex3 Qno.1
select country.name as "country name", airport.name as "airport name"
-> from country, airport
-> where airport.iso_country = country.iso_country and country.name = "Iceland";

<img width="644" alt="Screenshot Exercise 3 - Question1" src="https://github.com/user-attachments/assets/ac3426cf-8934-455c-895e-229c060ae0de">


#ex3 Qno.2
select airport.name as "airport name" from airport
-> join country on airport.iso_country = country.iso_country
-> where country.name = "France" and airport.type = "large_airport";

<img width="519" alt="Screenshot Exercise3 - Question2" src="https://github.com/user-attachments/assets/e507c0c0-9e12-4ab9-8435-36fb8c8342d1">

#ex3 Qno.3
select country.name as "country_name", airport.name as "airport_name" from country, airport
-> where airport.iso_country = country.iso_country and country.continent = "AN";

<img width="800" alt="Screenshot Exercise3 - Question3" src="https://github.com/user-attachments/assets/4e277d0c-67d6-4b18-a9bb-2a7f8570a4d4">

#ex3 Qno.4
select elevation_ft from airport
-> join game on airport.ident = game.location 
-> where screen_name = "Heini";

<img width="386" alt="Screenshot Exercise3 - Question4" src="https://github.com/user-attachments/assets/5b066f03-cd97-44e2-b39f-84f7e98794aa">

#ex3 Qno.5
set @elevation_m = 0;
select (elevation_ft * 0.3048) as elevation_m from airport
-> join game on airport.ident = game.location 
-> where screen_name = "Heini";

<img width="569" alt="Screenshot Exercise3 - Question5" src="https://github.com/user-attachments/assets/542b5172-f656-43b4-8c47-9cd5c923c4cb">

#ex3 Qno.6
select name from airport
-> join game on airport.ident = game.location
-> where screen_name = "Ilkka";

<img width="344" alt="Screenshot Exercise3 - Question6" src="https://github.com/user-attachments/assets/be9386f7-d919-4c7e-9875-a6f34a04d525">

#ex3 Qno.7
select country.name from country, airport, game
-> where game.location = airport.ident and airport.iso_country = country.iso_country
-> and game.screen_name = "Ilkka";


<img width="641" alt="Screenshot Exercise3 - Question7" src="https://github.com/user-attachments/assets/c54b4582-3a58-41e8-b2c7-801a3d14f82c">

#ex3 Qno.8
select goal.name from goal, goal_reached, game
-> where goal.id = goal_id and game.id = game_id and screen_name = "Heini";

<img width="555" alt="Screenshot Exercise3 - Question8" src="https://github.com/user-attachments/assets/9d63bdca-71fc-45ad-8a37-13bf14941ac7">


#ex3 Qno.9
select airport.name from airport, game, goal_reached, goal
-> where airport.ident = game.location and game.id = game_id and goal.id = goal_id
-> and game.screen_name = "Ilkka" and goal.name = "clouds";

<img width="608" alt="Screenshot Exercise3 - Question9" src="https://github.com/user-attachments/assets/4be5a5fe-ba82-4f56-a601-7b62155c75fb">


#ex3 Qno.10
select country.name from country, airport, game, goal_reached, goal
-> where game.location = airport.ident and game.id = game_id 
-> and goal.id = goal_id and airport.iso_country = country.iso_country
-> and game.screen_name = "Ilkka" and goal.name = "clouds";

<img width="640" alt="Screenshot Exercise3 - Question10" src="https://github.com/user-attachments/assets/f4292721-fc56-444e-81f4-fee5d4471cb6">









 
