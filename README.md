# AI Productivity Analytics System
This is a MySQL database project where I built a system to track study sessions, sleep hours, and test scores.
The main goal of this project is to organize productivity-related data and perform basic analysis using SQL queries.

## What This Project Does
- Stores student information
- Tracks daily study sessions
- Logs sleep hours
- Records test scores
- Performs simple analysis using JOIN and aggregate functions

## Technologies Used
- MySQL
- SQL
- ER Diagram
  
## Database Tables
- Students
- Study_Sessions
- Sleep_Data
- Test_Scores

Each table is connected using foreign keys.

## Example Queries

### Average Focus Rating
SELECT AVG(FOCUS_RATING)
FROM STUDY_SESSIONS;

### Sleep vs Test Score
SELECT S.SLEEP_HOURS, T.SCORE
FROM SLEEP_DATA AS S
INNER JOIN TEST_SCORES AS T
ON S.STUDENT_ID = T.STUDENT_ID
AND S.SLEEP_DATE = T.TEST_DATE;


## Why I Built This
I wanted to practice database design and understand how structured data can be used later for analysis and machine learning.

## How to Use
1. Run database_schema.sql
2. Insert data using sample_data.sql
3. Run queries from queries.sql
