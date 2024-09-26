# World-Cup-Database

### Approach for the World Cup Database Project

1. **Understanding the Requirements:**
   - First, I took a close look at the project requirements to figure out the necessary tables and how they would relate to each other. The `games.csv` file provided valuable data on teams and matches that I needed to organize.

2. **Designing the Database:**
   - I planned two main tables:
     - **Teams Table:** This table includes a unique `team_id` (which automatically increments) and a `name` column to store each team's name.
     - **Games Table:** Here, I included columns like `game_id`, `year`, `round`, `winner_id`, `opponent_id`, `winner_goals`, and `opponent_goals`, making sure the foreign keys correctly reference the teams.

3. **Setting Up the Database:**
   - After logging into PostgreSQL, I created a new database called `worldcup`. Then, I ran SQL commands to create the `teams` and `games` tables, applying the right data types and constraints like NOT NULL and UNIQUE to maintain data integrity.

4. **Inserting Data:**
   - I wrote a script (`insert_data.sh`) to read the `games.csv` file. This script first adds unique team names to the `teams` table and then fills in the `games` table with match details. I made sure to use efficient queries to minimize database interactions.

5. **Querying the Database:**
   - To analyze the data, I created a `queries.sh` script that runs various SQL queries, such as counting total games and finding teams with the most wins. Before finalizing the script, I tested each query in the PostgreSQL terminal to ensure accuracy.

6. **Ensuring Data Integrity and Performance:**
   - Throughout the project, I made it a point to check that all constraints were enforced. This helped maintain data integrity. I also focused on optimizing performance by reducing the number of queries during data insertion.

7. **Finalizing Everything:**
   - Once the database was set up and the data was inserted, I used the `pg_dump` command to create a backup of the database in a `.sql` file. I organized all the relevant files, including scripts and the database dump, into a GitHub repository, adding a `.gitignore` file to filter out unnecessary files.

8. **Documentation:**
   - Finally, I put together a README file that explains the project, how to set it up, and how to run the scripts. This way, anyone looking at my work can easily understand my approach and the purpose behind the database.

This approach helped me stay organized and ensured I met all the project requirements effectively.
