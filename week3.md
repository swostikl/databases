#week 3
Q.no. 1
select * 
from goal;

<img width="1225" alt="Screenshot 2024-09-10 at 9 06 40 PM" src="https://github.com/user-attachments/assets/a3878e4c-19d2-43c7-a1ea-c3b5cd084ec8">

Q. No. 2
select name 
from airport 
where iso_country = "FI";
<img width="540" alt="Screenshot 2024-09-14 at 10 16 39 PM" src="https://github.com/user-attachments/assets/292f0134-3143-43eb-b24f-fc0c3ca3e814">



Q. No. 3.
select name 
from airport 
where iso_country="FI" order by name;

<img width="1440" alt="Screenshot 2024-09-11 at 10 23 35 PM" src="https://github.com/user-attachments/assets/55fec96f-0f59-4d1c-b19b-0f883ef8ff66">

Q. No. 4
select name, type 
from airport 
where iso_country="FI" 
order by type, name; 

<img width="1440" alt="Screenshot 2024-09-11 at 4 29 46 PM" src="https://github.com/user-attachments/assets/103b273d-51e6-4a4e-9a00-5b9870b0199a">

Q.No.5
select name 
from country 
where name like "F%";

<img width="499" alt="Screenshot 2024-09-11 at 4 40 34 PM" src="https://github.com/user-attachments/assets/bf1127ba-2e24-4865-87ae-c869e244399e">



Q.No.6
select name 
from country 
where name like "%F%";

<img width="539" alt="Screenshot 2024-09-11 at 4 42 46 PM" src="https://github.com/user-attachments/assets/3833d6db-0509-4e82-8c67-0a03269101a0">

Q.No.7
select location 
from game where 
screen_name = "Vesa";
<img width="566" alt="Screenshot 2024-09-14 at 10 26 57 PM" src="https://github.com/user-attachments/assets/7d03444d-ffeb-4edc-bc2d-ac8a3c0e1210">





Q.NO.8
select co2_consumed 
from game
where screen_name = "Ilkka";
<img width="575" alt="Screenshot 2024-09-14 at 10 29 36 PM" src="https://github.com/user-attachments/assets/8d59e3c1-4c02-480f-b7c1-aa8d53b2a610">





Q.No.9
select distinct co2_budget from game;

<img width="442" alt="Screenshot 2024-09-14 at 10 31 20 PM" src="https://github.com/user-attachments/assets/dea6b994-1fb5-4cbc-8915-d3175f59ea55">





Q.No.10
select screen_name , co2_budget, co2_consumed from game where screen_name='Ilkka';

<img width="736" alt="Screenshot 2024-09-14 at 10 38 15 PM" src="https://github.com/user-attachments/assets/cf3ee5b4-84fe-4a85-a1f5-40786dc9f2d6">

















