# Stevie-s-Portfolio
Data Analytics Portfolio. Project's 1-3 were created in Khan Academy's Intro to SQL course.
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

# Project 3: Joining tables in an athlete database
CREATE TABLE athletes(
    id INTEGER PRIMARY KEY AUTOINCREMENT,
    fullname TEXT,
    age INTEGER,
    sport TEXT);
    
INSERT INTO athletes (fullname, age, sport) VALUES ("Lebron James", 38, "Basketball");
INSERT INTO athletes (fullname, age, sport) VALUES ("Tiger Woods", 47, "Golf");
INSERT INTO athletes (fullname, age, sport) VALUES ("Lionel Messi", 35, "Soccer");
INSERT INTO athletes (fullname, age, sport) VALUES ("Tom Brady", 69, "Football");
INSERT INTO athletes (fullname, age, sport) VALUES ("Kevin Durant", 45, "Basketball");

CREATE table career(
    id INTEGER PRIMARY KEY AUTOINCREMENT,
    athlete_id INTEGER,
    years_pro INTEGER,
    team TEXT);
    
INSERT INTO career (athlete_id, years_pro, team) VALUES (1, "20", "Lakers");
INSERT INTO career (athlete_id, years_pro, team) VALUES (2, "26", "PGA");
INSERT INTO career (athlete_id, years_pro, team) VALUES (3, "18", "Argentina");
INSERT INTO career (athlete_id, years_pro, team) VALUES (4, "22", "Buccaneers");
INSERT INTO career (athlete_id, years_pro, team) VALUES (5, "15", "Nets");


/*Return years pro for each athlete*/
SELECT athletes.fullname, career.years_pro
FROM athletes
JOIN career
ON athletes.id = career.athlete_id;
SELECT * FROM athletes;


# Project 4: Bike Sales project in Google Sheets
In this project I clean the data, create a few pivot tables, and create a simple dashboard.
https://docs.google.com/spreadsheets/d/1qmelkhFcNu170HMH0cWzOtiqoB2k4nuMKaaPdy7H14E/edit?usp=sharing

# Project 5: Bellabeat Case Study from Google Data Analysis course
Informational doc: https://docs.google.com/document/d/1fqSi0C1abOZ0qufkJyoKJB5XOG4_cbzIhUJhBoGjE3k/edit
Rstudio code: https://posit.cloud/content/4668477
# Project 6: Tableau Netflix Project:
Dataset: (https://www.kaggle.com/code/chirag907...)
Project: (https://public.tableau.com/app/profile/stevie.becker/viz/Netflixportfolioproject/Netflix)
