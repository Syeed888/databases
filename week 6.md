## Week 6 Aggregate Queries

### Question 1
SELECT max(elevation_ft)
FROM airport;

![Screenshot 2024-10-21 092445](https://github.com/user-attachments/assets/ccfbdc26-5979-4755-9197-c30d4307b8f8)

### Question 2
SELECT continent, count(*)
FROM country
GROUP BY continent;

![Screenshot 2024-10-21 092827](https://github.com/user-attachments/assets/afba89a3-68d2-4642-ba72-3fcbc2846935)

### Question 3
SELECT screen_name, count(*) 
FROM game, goal_reached 
WHERE id = game_id 
GROUP BY screen_name;

![Screenshot 2024-10-21 093115](https://github.com/user-attachments/assets/80d4dcb4-8f7a-43d7-9708-d3077f6d93a0)

### Question 4
SELECT screen_name 
FROM game 
WHERE co2_consumed IN (SELECT MIN(co2_consumed) FROM game);

![Screenshot 2024-10-21 093534](https://github.com/user-attachments/assets/348c3166-3907-44eb-be4e-5a2c78213eda)

### Question 5
SELECT country.name, count(*) 
FROM airport, country 
WHERE airport.iso_country = country.iso_country 
GROUP BY country.iso_country 
ORDER BY COUNT() DESC 
LIMIT 50;

![Screenshot 2024-10-21 094115](https://github.com/user-attachments/assets/c2890521-1e14-4d55-a92c-7ca9a0d3bdb3)

### Question 6
SELECT country.name 
FROM airport, country 
WHERE airport.iso_country = country.iso_country 
GROUP BY country.iso_country 
HAVING COUNT(*) > 1000;

![Screenshot 2024-10-21 094428](https://github.com/user-attachments/assets/4068fb09-1cae-47a3-96d5-a2a91012df36)

### Question 7
SELECT name 
FROM airport 
WHERE elevation_ft = (
    SELECT MAX(elevation_ft) 
    FROM airport
);

![Screenshot 2024-10-21 094620](https://github.com/user-attachments/assets/c4ae6325-2eeb-4549-a59c-1efe088f943e)

### Question 8
SELECT country.name 
FROM country 
WHERE iso_country = (
    SELECT iso_country 
    FROM airport 
    WHERE elevation_ft = (
        SELECT MAX(elevation_ft) 
        FROM airport
    )
);

![Screenshot 2024-10-21 094815](https://github.com/user-attachments/assets/4ff0c19b-3931-4cfa-84cc-079525bb9de6)

### Question 9
SELECT count(*) 
FROM game, goal_reached 
WHERE id = game_id AND screen_name = "Vesa" 
GROUP BY screen_name;

![Screenshot 2024-10-21 095128](https://github.com/user-attachments/assets/f9d2283b-c7d4-46db-b5e8-dd1c1bf50cf7)

### Question 10
SELECT name 
FROM airport 
WHERE latitude_deg IN (SELECT MIN(latitude_deg) FROM airport);

![Screenshot 2024-10-21 095502](https://github.com/user-attachments/assets/c4d54d0c-4fc2-41c6-bbd3-7c9ecf8bf8d1)
