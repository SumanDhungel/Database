# Database
#week 3 ex2
#Qno.1
select * from goal ;

 <img width="806" alt="Screenshot Exercise 2- Question1" src="https://github.com/user-attachments/assets/f78413eb-502b-4fca-b51d-f9ae76211163">

#Qno.2
select name from airport where iso_country = "FI";

<img width="515" alt="Screenshot Exercise2 - Question 2" src="https://github.com/user-attachments/assets/d0e8a038-a758-464a-baa1-23f6449aaf03">

#Qno.3
select name from airport where iso_country = "FI" order by name asc;

<img width="638" alt="Screenshot Exercise 2 - Question3" src="https://github.com/user-attachments/assets/91026488-b5c0-4dba-9233-da5344ed09d0">

#Qno.4
select name, type from airport where iso_country = "FI" order by type, name;

<img width="688" alt="Screenshot Exercise 2 - Question 4" src="https://github.com/user-attachments/assets/31a5c6d2-08ad-415e-a2b5-49405ef0bf8e">

#Qno.5
select name from country where name like "F%";

<img width="482" alt="Screenshot Exercise 2 Question5" src="https://github.com/user-attachments/assets/5e25b48c-e654-4a65-9e8e-7e45798893bc">

#Qno.6
select name from country where name like "%F%";

<img width="490" alt="Screenshot Exercise 2- Question6" src="https://github.com/user-attachments/assets/17d59342-c060-4102-87c3-4ed486843ee5">

#Qno.7
select location from game where screen_name = "Vesa";

<img width="536" alt="Screenshot Exercise 2- Question7" src="https://github.com/user-attachments/assets/814215be-7a48-4bde-8118-a2fe31c5e10e">

#Qno.8
select co2_consumed from game where screen_name = "Ilkka";

<img width="572" alt="Screenshot Exercise2- Question8" src="https://github.com/user-attachments/assets/24ad5a50-403a-46bb-9dcd-85187bcaabe1">

#Qno.9
select distinct co2_budget from game;

<img width="419" alt="Screenshot Exercise2- Question9" src="https://github.com/user-attachments/assets/8ad1f420-3765-4be0-b31b-08b6d7416b82">

#Qno.10
set @co2_left := 0;
select screen_name, co2_budget, co2_consumed, (co2_budget - co2_consumed) as co2_left from game where screen_name = "Ilkka";

<img width="950" alt="Screenshot Exercise2 - Question10" src="https://github.com/user-attachments/assets/ae9ec797-de9a-4ba9-922b-e5e826091963">






 
