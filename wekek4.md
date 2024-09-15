week4
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



