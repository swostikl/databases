# week  5 exercises
# Excercise 

Q.NO.1
select max(elevation_ft)
from airport;



Q.no.2

select continent, count(*)
from country
group by continent;





Q.no.3

select screen_name, count(*)
from game, goal_reached
where id = game_id
group by screen_name;


Q.no.4
select screen_name
from game
where co2_consumed in(
select min(co2_consumed)
from game
);



Q.no.5

select country.name, count(*)
from airport, country
where airport.iso_country = country.iso_country
group by country.iso_country
order by count(*) desc
limit 50;


Q.no. 6
select country.name
from airport, country
where airport.iso_country = country.iso_country
group by country.iso_country
having count(*) > 1000;


Q.no. 7
select name
from airport
where elevation_ft in (
select max(elevation_ft)
from airport
);


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

Q.no.9
select count(*)
from game, goal_reached
where id = game_id and screen_name = "Vesa"
group by screen_name;


Q.no.10
select name
from airport
where latitude_deg in(
select min(latitude_deg)
from airport
);














