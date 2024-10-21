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
