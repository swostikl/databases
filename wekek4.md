week4
Exercises 1
Q.No.1

select country.name as 'country name' , airport.name as 'airport name'
from country
inner join airport on airport.iso_country=country.iso_country
where country.name='Finland' and scheduled_service='yes';
<img width="654" alt="Screenshot 2024-09-15 at 8 29 16 AM" src="https://github.com/user-attachments/assets/5a7c4e3c-d1fd-4480-b1fb-3d675565016a">



Q.No. 2

select screen_name, airport.name
from game 
inner join airport on location = ident;


<img width="399" alt="Screenshot 2024-09-15 at 8 33 55 AM" src="https://github.com/user-attachments/assets/1f232682-31be-4420-936f-8c66460b9ae6">




Q.No.3
select screen_name, country.name
from game
inner join airport on location=ident
inner join country on airport.iso_country=country.iso_country;

<img width="513" alt="Screenshot 2024-09-15 at 8 37 50 AM" src="https://github.com/user-attachments/assets/7273823a-2934-4dd3-813c-f4955b40d707">



Q.no.4

select airport.name, screen_name
from airport left join game on ident = location 
where name like "%Hels%";

<img width="457" alt="Screenshot 2024-09-15 at 8 49 10 AM" src="https://github.com/user-attachments/assets/4a978317-06da-4efb-ad95-cc66726fc51f">


Q.NO.5
select name, screen_name 
from goal
left join goal_reached on goal.id=goal_reached.goal_id
left join game on goal_reached.game_id=game.id;

<img width="436" alt="Screenshot 2024-09-15 at 8 57 28 AM" src="https://github.com/user-attachments/assets/1f2ef598-1bd4-4078-9ac9-192f84a7d304">




Exercises2
Q.no.1
select name
from country
where iso_country in(
select iso_country
from airport
where name like "Satsuma%"
);
<img width="297" alt="Screenshot 2024-09-15 at 9 40 15 AM" src="https://github.com/user-attachments/assets/09afaa77-f988-4d0e-96dc-3297a8920dd8">




Q.no.2
select name
from airport where
iso_country in(
select iso_country
from country
where name = "Monaco"
);
<img width="328" alt="Screenshot 2024-09-15 at 9 44 21 AM" src="https://github.com/user-attachments/assets/c330b994-046d-44ad-9e9c-1e81fbaecae8">




Q.No.3
select screen_name
from game
where id in (
select game_id
from goal_reached
where goal_id in(
select id
from goal
where name = "CLOUDS"
)
);



<img width="389" alt="Screenshot 2024-09-15 at 9 51 59 AM" src="https://github.com/user-attachments/assets/11e9ad16-ea59-4aba-aef0-db94f1c89bc0">




Q.No.4
select country.name
from country
where iso_country not in
(select airport.iso_country
from airport);

<img width="313" alt="Screenshot 2024-09-15 at 9 55 55 AM" src="https://github.com/user-attachments/assets/730e9fef-7e0a-4dea-b0f0-b701e5166491">



Q.No.5

select name
from goal
where id not in(
select goal.id
from goal, goal_reached, game
where game.id = game_id and goal.id = goal_id and screen_name = "Heini"
);



<img width="564" alt="Screenshot 2024-09-15 at 10 04 50 AM" src="https://github.com/user-attachments/assets/5738303c-9a64-4a45-8ded-2a3fe16a0b68">





