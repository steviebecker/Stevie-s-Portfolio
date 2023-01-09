# Stevie-s-Portfolio
Data Analytics Portfolio. Project's 1 and 2 were creating Khan Academy's Intro to SQL course.
# Project 1: Creating a store database
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

# Project 2: Creating an App's SQL Database
/* What does the app's SQL look like? */
CREATE TABLE bleacher_report(
    id INTEGER PRIMARY KEY AUTOINCREMENT,
    name TEXT,
    points INTEGER,
    minutes INTEGER);

INSERT INTO bleacher_report (name, points, minutes) VALUES ("Lebron", 30, 50);
INSERT INTO bleacher_report (name, points, minutes) VALUES ("Giannis", 34, 33);
INSERT INTO bleacher_report (name, points, minutes) VALUES ("Nicola", 32, 30);
INSERT INTO bleacher_report (name, points, minutes) VALUES ("Kevin", 24, 34);

UPDATE bleacher_report set name = "Nikola"
WHERE id = 3;

DELETE FROM bleacher_report
WHERE id = 2;
SELECT * FROM bleacher_report;

# Project 3: Bike Sales project in Google Sheets
In this project I clean the data, create a few pivot tables, and create a simple dashboard.
https://docs.google.com/spreadsheets/d/1qmelkhFcNu170HMH0cWzOtiqoB2k4nuMKaaPdy7H14E/edit?usp=sharing

