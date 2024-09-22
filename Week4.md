#Week4
#ex4 Qno.1
select country.name as "country name ", airport.name as "airport name" from country
inner join airport on country.iso_country = airport.iso_country
where country.name = "Finland";

<img width="727" alt="Screenshot Exercise4 - Question1" src="https://github.com/user-attachments/assets/b0935b7c-b788-4a23-8865-9aeb46632985">


#ex4 Qno.2
select screen_name, name from game
inner join airport on game.location = airport.ident;

<img width="415" alt="Screenshot Exercise4 - Question2" src="https://github.com/user-attachments/assets/0a6a468d-d426-49b7-ad8a-855f83728d55">



#ex4 Qno.3
select game.screen_name, country.name from game
inner join airport on game.location = airport.ident
inner join country on airport.iso_country = country.iso_country;

<img width="502" alt="Screenshot Exercise4 - Question3" src="https://github.com/user-attachments/assets/d54f5a7a-e42a-4b58-86e0-f4ae09f95c1f">


#ex4 Qno.4
select name, screen_name from airport
left join game on game.location = airport.ident
where name like "%Hels%" order by screen_name desc;

<img width="422" alt="Screenshot Exercise4 - Question4" src="https://github.com/user-attachments/assets/67e797e9-cfab-4b85-995b-06bcdb76b64b">


#ex4 Qno.5
select name, screen_name from goal
left join goal_reached on goal.id = goal_id
left join game on game.id = game_id;

<img width="401" alt="Screenshot Exercise4 - Question5" src="https://github.com/user-attachments/assets/a7a79ea3-96b8-4706-8c22-6e681a4c6044">


#ex5 Qno.1
select name from country
where iso_country in (select iso_country from airport
where name like "Satsuma%");

<img width="434" alt="Screenshot Exercise5 - Question1" src="https://github.com/user-attachments/assets/2db8ede0-cdc6-4fbf-aa48-5437f16e92bd">


#ex5 Qno.2
select name from airport
where iso_country in (
select iso_country from country
where name = "Monaco");

<img width="335" alt="Screenshot Exercise5 - Question2" src="https://github.com/user-attachments/assets/900b7b61-9f62-4539-a6cc-e19c78e276cc">


#ex5 Qno.3
select screen_name from game
where id in (select game_id from goal_reached
where goal_id in (select id from goal
where name = "clouds"));

<img width="367" alt="Screenshot Exercise5 - Question3" src="https://github.com/user-attachments/assets/6bfc66b4-ef34-4374-8fc0-454da1e2834e">


#ex5 Qno.4
select name from country
where iso_country not in (
select iso_country from airport);

<img width="335" alt="Screenshot Exercise5 - Question4" src="https://github.com/user-attachments/assets/4b24ff78-2b6f-4550-8108-465d4839dc35">


#ex5 Qno.5
select name from goal
where id not in (select goal_id from goal_reached
where game_id not in (select id from game
where name = "Heini"));

<img width="398" alt="Screenshot Exercise5 - Question5" src="https://github.com/user-attachments/assets/bfeeae8e-b4c2-42ea-bd2c-5292d50cc8f0">
