#Week 5
#ex 6 
#Qno.1
select max(elevation_ft) from airport;

<img width="431" alt="Screenshot Ex6 - Qno 1" src="https://github.com/user-attachments/assets/eb8ed068-f131-4ccd-8177-56d73d434aac">



#ex 6 #Qno.2
select continent, count(*)
from country
group by continent;

<img width="350" alt="Screenshot Ex6 - Qno 2" src="https://github.com/user-attachments/assets/b5a4291c-c7c9-4ecf-8e79-4ed5aa3dfbf0">


#ex6 #Qno.3
select screen_name, count(*)
from game, goal_reached
where id = game_id
group by screen_name;

<img width="362" alt="Screenshot Ex6 - Qno 3" src="https://github.com/user-attachments/assets/15b51efb-88b6-4083-922b-b4feee012182">


#ex6 #Qno.4
select screen_name from game
where co2_consumed in (select min(co2_consumed) from game);

<img width="464" alt="Screenshot Ex6 - Qno 4" src="https://github.com/user-attachments/assets/c4851eda-de4f-420b-8b63-646ecd2ca145">


#ex6 #Qno.5
select country.name, count(*) from country
inner join airport on airport.iso_country = country.iso_country
group by country.name
order by count(airport.id) desc limit 50;

<img width="500" alt="Screenshot Ex6 - Qno 5" src="https://github.com/user-attachments/assets/26c1afd8-4eb2-4d3f-a485-372401d2d001">


#ex6 #Qno.6
select country.name from country
inner join airport on airport.iso_country = country.iso_country
group by country.name
having count(airport.id) > 1000;

<img width="494" alt="Screenshot Ex6 - Qno 6" src="https://github.com/user-attachments/assets/1d0ccf19-9b94-4c5c-88dd-dd23ba653e62">



#ex6 Qno.7
select name from airport
where elevation_ft in (select max(elevation_ft) from airport);

<img width="488" alt="Screenshot Ex6 - Qno 7" src="https://github.com/user-attachments/assets/73ac35de-f55f-482b-9497-054227223a5f">


#ex6 # Qno.8
select country.name from country
inner join airport on airport.iso_country = country.iso_country
where elevation_ft in (select max(elevation_ft) from airport);

<img width="497" alt="Screenshot Ex6 - Qno 8" src="https://github.com/user-attachments/assets/dde8bc0e-3444-45b4-90a0-b46822648bd3">


#ex6 #Qno.9
select count(*) from goal_reached, game
where id = game_id and screen_name = "Vesa";

<img width="440" alt="Screenshot Ex6 - Qno 9" src="https://github.com/user-attachments/assets/94cc6c3c-0158-4bdc-9745-f127587caa72">


#ex6 #Qno.10
select name from airport
where latitude_deg in (select min(latitude_deg) from airport);

<img width="489" alt="Screenshot Ex6 - Qno 10" src="https://github.com/user-attachments/assets/86cf5070-48b9-45c8-adf5-f91f22e058df">



#ex 7 #Qno.1
update game
set co2_consumed = co2_consumed + 500,
location = (select ident from airport where name = "Nottingham Airport")
where screen_name = "Vesa";

<img width="563" alt="Screenshot Ex7 - Qno 1" src="https://github.com/user-attachments/assets/6878e1a0-5ced-45f3-962b-c3929723b4ff">



#ex7 #Qno.2

![Screenshot Ex7 - Qno 2](https://github.com/user-attachments/assets/214bb1a5-e676-4796-b1d3-9b3a9a4b72e8)

#ex7 #Qno.3
delete from goal_reached;
select * from goal_reached;

<img width="353" alt="Screenshot Ex7 - Qno 3" src="https://github.com/user-attachments/assets/b83b2dce-5fcd-47fb-ab6f-b0a6117a8ee6">



#ex7 #Qno.4
delete from game;
select * from game;

<img width="307" alt="Screenshot Ex7 - Qno 4" src="https://github.com/user-attachments/assets/34b3318e-a287-4eec-841f-ab9ae0368e2e">




