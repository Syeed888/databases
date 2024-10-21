## Week 7  Update Queries

### Question 1
UPDATE game 
SET co2_consumed = co2_consumed + 500, location = (
    SELECT ident 
    FROM airport 
    WHERE name = 'Nottingham Airport'
) 
WHERE screen_name = 'Vesa';

![Screenshot 2024-10-21 100245](https://github.com/user-attachments/assets/2a2c8cad-8439-44b5-bc23-041224392824)

### Question 2
goal_reached

### Question 3
delete from goal_reached;
select * from goal_reached

![Screenshot 2024-10-21 100647](https://github.com/user-attachments/assets/7c020996-663d-4899-a8cd-25ca25403d87)

### Question 4
delete from game;
select * from game;

![Screenshot 2024-10-21 100905](https://github.com/user-attachments/assets/86bae8e3-64c3-4ede-b615-a8156cead629)
