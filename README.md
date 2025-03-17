# World Cup Database

*This project consists of creating a Bash script that enters information from World Cup games into PostgreSQL, then querying the database for useful statistics.*

## Problem Statement

You start with several files, one of them is *games.csv* . It contains a comma-separated list of all games of the final three rounds of the World Cup tournament since 2014; the titles are at the top. It includes the year of each game, the round of the game, the winner, their opponent, and the number of goals each team scored. 

You need to do three things for this project:

- Part 1: Create the database 

  Create your database structure according to the user stories below. Don't forget to connect to the database after you create it. 
  - Create a database named **worldcup** and then create **teams** and **games** tables.
  - The *teams* table should have a **team_id** column that is a type of **SERIAL** and is the primary key, and a **name** column that has to be **UNIQUE**.
  - The *games* table should have a **game_id** column that is a type of **SERIAL** and is the primary key, a **year** column of type **INT**, and a **round** column of type **VARCHAR**.
  - The *games* table should have **winner_id** and **opponent_id** foreign key columns that each reference **team_id** from the *teams* table.
  - The *games* table should have **winner_goals** and **opponent_goals** columns that are type **INT**.
  - All the columns should have the **NOT NULL** constraint.
  

- Part 2: Insert the data 

  Complete the *insert_data.sh* script to correctly insert all the data from *games.csv* into the database.
  - When you run your **insert_data.sh** script, it should add each unique team to the *teams* table. There should be 24 rows.
  - When you run your **insert_data.sh** script, it should insert a row for each line in the games.csv file (other than the top line of the file). There should be 32 rows.
  - Each row should have every column filled in with the appropriate info. Make sure to add the correct ID's from the *teams* table (you cannot hard-code the values).

- Part 3: Query the database 

  Complete the empty echo commands in the *queries.sh* file to produce output that matches the *expected_output.txt* file.
  - Correctly complete the *queries* in the **queries.sh** file.
  - Fill in each empty **echo** command to get the output of what is suggested with the command above it.
  - The output should match what is in the **expected_output.txt** file *exactly*, take note of the number of decimal places in some of the query results.


![Image](https://github.com/user-attachments/assets/c7cd8d03-3c40-42ee-a6ec-00036fddcb96)

![Image](https://github.com/user-attachments/assets/8eb6a1ea-fdbd-450f-949f-db1cc5a3e333)

![Image](https://github.com/user-attachments/assets/cc2b7bdf-8dc8-42de-bfdd-2a3dd081209d)

![Image](https://github.com/user-attachments/assets/7a5f3e3a-717b-4800-aa99-acf582204244)
