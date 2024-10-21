## Week 5 Subqueries

### Question 1
SELECT country.name 
FROM country 
JOIN airport ON country.iso_country = airport.iso_country 
WHERE airport.name LIKE 'Satsuma%';

![Screenshot 2024-10-21 091103](https://github.com/user-attachments/assets/74f806c9-73ef-45cf-876f-6d8b5ef9fc2c)

### Question 2
SELECT airport.name 
FROM airport 
WHERE airport.iso_country = 'MC';

![Screenshot 2024-10-21 091311](https://github.com/user-attachments/assets/a26f2a4a-1825-4f83-8f95-11471ac4baa8)

### Question 3
SELECT game.screen_name 
FROM game 
JOIN goal_reached ON game.id = goal_reached.game_id 
JOIN goal ON goal_reached.goal_id = goal.id 
WHERE goal.name = 'CLOUDS';

![Screenshot 2024-10-21 091507](https://github.com/user-attachments/assets/62510c68-653a-473c-b5f6-3b2fe4622e92)

### Question 4
SELECT country.name 
FROM country 
WHERE country.iso_country NOT IN (SELECT airport.iso_country FROM airport);

![Screenshot 2024-10-21 091656](https://github.com/user-attachments/assets/86dc6e8c-bbf4-4140-8f00-588d4cd1efa7)

### Question 5
SELECT name 
FROM goal 
WHERE id NOT IN (
    SELECT goal.id 
    FROM goal, goal_reached, game 
    WHERE game.id = game_id AND goal.id = goal_id AND screen_name = "Heini"
);

![Screenshot 2024-10-21 092014](https://github.com/user-attachments/assets/f8583eac-9dbd-480d-92d2-82c359f2dac9)
