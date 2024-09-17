#Multiple Table Queries # Week3
Q.NO.1
SELECT country.name AS "country name", airport.name AS "airport name"
FROM country, airport
where country.iso_country=airport.iso_country and
country.name='Iceland';

<img width="671" alt="Screenshot 2024-09-14 at 4 13 21 PM" src="https://github.com/user-attachments/assets/5784278c-d086-4e20-854d-f9b0b6ae72ae"> 

Q.No.2
select airport.name as 'airport name' from airport
join country
where airport.iso_country=country.iso_country and
country.name='France' and airport.type="large_airport" ;

<img width="527" alt="Screenshot 2024-09-14 at 9 15 44 PM" src="https://github.com/user-attachments/assets/6e807ae5-fe9b-4c11-8f9a-d88cec39a653">



Q.NO.3
select country.name as country_name,airport.name airport_name
from airport, country
where country.iso_country=airport.iso_country and
country.continent="AN";
<img width="718" alt="Screenshot 2024-09-14 at 9 23 12 PM" src="https://github.com/user-attachments/assets/cb9b7fa7-6b2b-4da6-9432-c42be312f778">



Q.NO.4

select elevation_ft
from airport, game
where location = ident and screen_name = "Heini";
<img width="402" alt="Screenshot 2024-09-14 at 9 32 16 PM" src="https://github.com/user-attachments/assets/cf8ec905-21e9-473b-af91-f7b3edba9c92">





Q.NO.5!

select elevation_ft* 0.3048 as elevation_m
from airport, game
where location = ident and screen_name = "Heini";

<img width="461" alt="Screenshot 2024-09-14 at 9 36 12 PM" src="https://github.com/user-attachments/assets/c56aa7c7-18b3-4991-ad86-9160440e85c6">



Q.NO.6
select name
from airport, game
where location = ident and screen_name = "Ilkka";
<img width="405" alt="Screenshot 2024-09-14 at 9 39 29 PM" src="https://github.com/user-attachments/assets/8547e76f-f9dc-44ab-9858-013b2d9ed2c9">





Q.no.7
select country.name
from airport, game, country
where location = ident and airport.iso_country = country.iso_country  and 
screen_name = "Ilkka";

<img width="728" alt="Screenshot 2024-09-14 at 9 43 16 PM" src="https://github.com/user-attachments/assets/4bdbe797-02ca-4d12-9f1e-a7d82670df47">




Q.NO.8
select name
from goal, goal_reached, game
where game.id = game_id and goal.id = goal_id and screen_name = "Heini";
<img width="564" alt="Screenshot 2024-09-14 at 9 47 41 PM" src="https://github.com/user-attachments/assets/9aec1f0c-0548-46fe-af45-221c037ca641">





Q.NO.9
select airport.name
from airport, game, goal, goal_reached
where ident = location and game.id = game_id and goal.id = goal_id and 
screen_name = "Ilkka" and goal.name = "CLOUDS";
<img width="892" alt="Screenshot 2024-09-14 at 9 52 44 PM" src="https://github.com/user-attachments/assets/0a58d625-102f-4e47-a82d-ac954eb05adc">




Q.No.10
select country.name
from country, airport, game, goal, goal_reached
where airport.iso_country = country.iso_country and 
ident = location and 
game.id = game_id and 
goal.id = goal_id and 
screen_name = "Ilkka" and goal.name = "CLOUDS";



<img width="431" alt="Screenshot 2024-09-14 at 9 59 00 PM" src="https://github.com/user-attachments/assets/246723c3-d881-4b55-ab11-1bf926378e39">



