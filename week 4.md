## Week 4 Join

### Question 1
SELECT country.name AS "country name", airport.name AS "airport name" 
FROM country 
JOIN airport ON country.iso_country = airport.iso_country 
WHERE country.name = "Finland";

![Screenshot 2024-10-21 085027](https://github.com/user-attachments/assets/c9ddd9f7-1608-4b8a-919b-88c28b928202)

### Question 2
SELECT screen_name, airport.name 
FROM game 
INNER JOIN airport ON location = ident;

![Screenshot 2024-10-21 085512](https://github.com/user-attachments/assets/651117d7-c665-4bb6-ac7a-f85ebd553ba2)

### Question 3
SELECT screen_name, country.name 
FROM game 
INNER JOIN airport ON location = ident 
INNER JOIN country ON airport.iso_country = country.iso_country;

![Screenshot 2024-10-21 085812](https://github.com/user-attachments/assets/4fd8a36f-e447-4f7d-be23-1c404689e48b)

### Question 4
SELECT airport.name AS "airport name", game.screen_name AS "screen_name"
FROM airport
LEFT JOIN game ON airport.ident = game.location
WHERE airport.name LIKE '%Hels%';

![Screenshot 2024-10-21 090222](https://github.com/user-attachments/assets/5cc8d0e3-edc8-484b-a7d6-b29145de5ff0)

### Question 5
SELECT name, screen_name 
FROM goal 
LEFT JOIN goal_reached ON goal.id = goal_id 
LEFT JOIN game ON game.id = game_id;

![Screenshot 2024-10-21 090542](https://github.com/user-attachments/assets/9f82de54-fa07-4409-b2fe-1b6a541cfcfb)
