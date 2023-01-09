# Stevie-s-Portfolio
Data Analytics Portfolio
# Project 1: Creating a fake clothing store database and running some Select statements on it in SQL.
CREATE TABLE clothing (id INTEGER PRIMARY KEY, name TEXT, quantity INTEGER, price INTEGER, gender INTEGER);
INSERT INTO clothing VALUES (1, "t shirt", 18, 7, 1);
INSERT INTO clothing VALUES (2, "long sleeve", 12, 8, 1);
INSERT INTO clothing VALUES (3, "jeans",10, 4, 2);
INSERT INTO clothing VALUES (4, "sweats", 9, 3, 1);
INSERT INTO clothing VALUES (5, "coats", 1, 22, 2);
INSERT INTO clothing VALUES (6, "shoes", 7, 2, 2);
INSERT INTO clothing VALUES (7, "socks", 7, 4, 2);
INSERT INTO clothing VALUES (8, "sportswear", 8, 8, 1);
INSERT INTO clothing VALUES (9, "underwear", 7, 6, 1);
INSERT INTO clothing VALUES (10, "belts", 10, 3, 1);
INSERT INTO clothing VALUES (11, "hats", 7, 4, 2);
INSERT INTO clothing VALUES (12, "swimwear", 7, 4, 2);
INSERT INTO clothing VALUES (13, "dresses", 15, 7, 2);
INSERT INTO clothing VALUES (14, "clearance", 12 ,6, 1);
INSERT INTO clothing VALUES (15, "other", 4, 10, 1);
SELECT * FROM clothing ORDER BY price;
SELECT SUM(quantity) FROM clothing GROUP BY gender;
