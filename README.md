# SQL
CREATE TABLE creates a new table.
INSERT INTO adds a new row to a table.
SELECT queries data from a table.
UPDATE edits a row in a table.
ALTER TABLE changes an existing table.
DELETE FROM deletes rows from a table.
#Examples:
/1/
INSERT INTO celebs (id, name, age) VALUES (1, 'Justin Bieber', 21);
/2/
UPDATE celebs 
SET age = 22 
WHERE id = 1; 

SELECT * FROM celebs;
/3/
UPDATE celebs 
SET twitter_handle = '@taylorswift13' 
WHERE id = 4; 

DELETE FROM celebs WHERE twitter_handle IS NULL; 

SELECT * FROM celebs;
/4/
CREATE TABLE awards (
  id INTEGER PRIMARY KEY,
  recipient TEXT NOT NULL,
  award_name TEXT DEFAULT "Grammy");
/5/
CREATE TABLE celebs (
    id INTEGER PRIMARY KEY, 
    name TEXT UNIQUE,
    date_of_birth TEXT NOT NULL,
    date_of_death TEXT DEFAULT 'Not Applicable',
    );
/6/
INSERT INTO celebs (id, name, age) VALUES (2, 'Beyonce Knowles', 33); 

INSERT INTO celebs (id, name, age) VALUES (3, 'Jeremy Lin', 26); 

INSERT INTO celebs (id, name, age) VALUES (4, 'Taylor Swift', 26);
