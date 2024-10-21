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


