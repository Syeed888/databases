# Week 3

### Assignment: Multiple Table Queries

### Question 1
SELECT country.name AS "country name", airport.name AS "airport name"
FROM country
JOIN airport ON country.iso_country = airport.iso_country
WHERE country.name = 'Iceland';

![Screenshot (2)](https://github.com/user-attachments/assets/e25c1493-39fa-4baa-a75c-11fcfee67faf)

### Question 2
SELECT name AS "airport name"
FROM airport
WHERE iso_country = 'FR' AND type = 'large_airport';
![Screenshot 2024-10-21 073810](https://github.com/user-attachments/assets/a7aabbc2-4841-42ed-9832-026a1b5b1eb8)

### Question 3
SELECT country.name AS country_name, airport.name AS airport_name
FROM airport
JOIN country ON airport.iso_country = country.iso_country
WHERE country.continent = 'AN';
![Screenshot 2024-10-21 075025](https://github.com/user-attachments/assets/9e1b91e8-582e-403f-81d0-1a8958f84782)

### Question 4
SELECT airport.elevation_ft
FROM airport
JOIN game ON game.location = airport.ident
WHERE game.screen_name = 'Heini';
![Screenshot 2024-10-21 075702](https://github.com/user-attachments/assets/b3506d19-7cf6-4281-801f-779abb04299f)

### Question 5
SELECT airport.elevation_ft * 0.3048 AS elevation_m
FROM airport
JOIN game ON game.location = airport.ident
WHERE game.screen_name = 'Heini';
![Screenshot 2024-10-21 080029](https://github.com/user-attachments/assets/fcce0fcd-6606-41e0-94fb-1264012cee81)

### Question 6
SELECT airport.name
FROM airport
JOIN game ON game.location = airport.ident
WHERE game.screen_name = 'Ilkka';
![Screenshot 2024-10-21 080322](https://github.com/user-attachments/assets/29638281-eac8-4a9c-9983-9c3a9d6aee94)

### Question 7
SELECT country.name
FROM airport
JOIN game ON game.location = airport.ident
JOIN country ON airport.iso_country = country.iso_country
WHERE game.screen_name = 'Ilkka';

![Screenshot 2024-10-21 080543](https://github.com/user-attachments/assets/85778762-0a37-4597-b432-50f4b3d62e2b)

### Question 8
SELECT goal.name
FROM goal
JOIN goal_reached ON goal.id = goal_reached.goal_id
JOIN game ON goal_reached.game_id = game.id
WHERE game.screen_name = 'Heini';
![Screenshot 2024-10-21 080954](https://github.com/user-attachments/assets/ce27087b-525c-4a7f-a5db-9d1942e29894)

### Question 9
SELECT airport.name 
FROM game, goal_reached, goal, airport 
WHERE ident = location 
AND game.id = game_id 
AND goal.id = goal_id 
AND screen_name = "Ilkka" 
AND goal.name = "CLOUDS";
![Screenshot 2024-10-21 082910](https://github.com/user-attachments/assets/6f25fdbe-5506-4b12-b1fb-609fd29e7d8f)

### Question 10
SELECT country.name 
FROM game, goal_reached, goal, country, airport 
WHERE airport.iso_country = country.iso_country 
AND ident = location 
AND game.id = game_id 
AND goal.id = goal_id 
AND screen_name = "Ilkka" 
AND goal.name = "CLOUDS";
![Screenshot 2024-10-21 083437](https://github.com/user-attachments/assets/7a2f0663-2bae-4d44-9df8-da957e537a1c)

