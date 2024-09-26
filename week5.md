# week  5 exercises
# Excercise 6

Q.NO.1
select max(elevation_ft)
from airport;

<img width="372" alt="1" src="https://github.com/user-attachments/assets/8fb820e2-0dd5-4ef0-ab90-b66e93dd59cc">



Q.no.2

select continent, count(*)
from country
group by continent;

<img width="392" alt="2" src="https://github.com/user-attachments/assets/7839d296-970c-4a98-b8a2-94298c7a5dc0">


Q.no.3

select screen_name, count(*)
from game, goal_reached
where id = game_id
group by screen_name;


<img width="374" alt="3" src="https://github.com/user-attachments/assets/3165aeee-09cc-404c-ab0d-149ae03ec483">



Q.no.4
select screen_name
from game
where co2_consumed in(
select min(co2_consumed)
from game
);


<img width="303" alt="4" src="https://github.com/user-attachments/assets/18469db7-30a4-4a6e-b604-0127bf4a7bc4">




Q.no.5

select country.name, count(*)
from airport, country
where airport.iso_country=country.iso_country
group by country.iso_country
order by count(*) desc
limit 50;



<img width="464" alt="5" src="https://github.com/user-attachments/assets/17da7ca6-94c7-4b86-8fc0-d6bbde0792f2">




Q.no. 6
select country.name
from airport, country
where airport.iso_country = country.iso_country
group by country.iso_country
having count(*) > 1000;


<img width="391" alt="6" src="https://github.com/user-attachments/assets/bb03987f-5592-4aeb-baa0-1247ad939b83">




Q.no. 7
select name
from airport
where elevation_ft in (
select max(elevation_ft)
from airport
);


<img width="276" alt="7" src="https://github.com/user-attachments/assets/4e865c1b-92a7-4559-996d-989e8a91d1c0">



Q.no 8
select name
from country
where iso_country in (
select iso_country
from airport
where elevation_ft in(
select max(elevation_ft)
from airport
)
);


<img width="293" alt="8" src="https://github.com/user-attachments/assets/1b10aff9-0583-4c3e-ab5e-1f2ba6320380">


Q.no.9
select count(*)
from game, goal_reached
where id = game_id and screen_name = "Vesa"
group by screen_name;

<img width="372" alt="9" src="https://github.com/user-attachments/assets/5ef0f138-ae4a-4d44-9ce3-9a48c739e72e">



Q.no.10
select name
from airport
where latitude_deg in(
select min(latitude_deg)
from airport
);

<img width="259" alt="10" src="https://github.com/user-attachments/assets/55d82cfb-3572-4fb1-9bd9-e7323fa8daf9">




# Exercise 7

Q.no 1

update game
set location=(select ident from airport where name="Nottingham Airport"), 
co2_consumed=co2_consumed + 500
where screen_name="Vesa";


select * from goal;


<img width="610" alt="7 1" src="https://github.com/user-attachments/assets/b7cfbbb8-72f1-4ead-adfd-4c441c140bbe">



Q.no 2
Prepare your own database for the project by deleting all dummy data relating to the game state. To maintain referential integrity, you have to delete the data in a specific order.
Do you have to delete data first from the game table or from the goal_reached table?
Question 2Answer

a.game   b.goal_reached

My answer is b. goal reached.


Q.no.3
Delete the dummy data from the goal_reached table.

delete from goal_reached;
select * from goal_reached;

Q.no.4
Delete the data from the game table.

delete from game;

select * from game;












