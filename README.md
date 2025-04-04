<h1><b>Video Game Sales Analysis</b></h1>

<h2>Short Description</h2>
This project analyzes video game sales data stored in a MySQL database using Python. It includes scripts to connect to the database, retrieve data, and perform basic analysis such as comparing average global sales before and after 2005 and labeling records based on their release year. The code leverages libraries like pandas, pymysql, and sqlalchemy to interact with the database and process the data.

<h2>Getting Started</h2>

<h2>Prerequisites</h2>
To run this project, ensure you have the following installed:

Python 3.x: The code is written in Python (tested with version 3.12.7).
MySQL: A running MySQL server with a database named ap containing a video_games table.
Python Libraries:
pandas: For data manipulation and analysis.
pymysql: For MySQL database connectivity.
sqlalchemy: For creating a database engine.
os: For environment variable handling (included in Python standard library).

**Install the required libraries using pip:**
<i>pip install pandas pymysql sqlalchemy</i>

**Installing**
Clone or Download the Code: Save the provided Jupyter Notebook (or Python script) to your local machine.
Set Up MySQL Database:
Create a database named ap in your MySQL server.
Create a table named video_games with the following schema (based on the columns in the code):

**sql**
<i>CREATE TABLE video_games (
    Name VARCHAR(255),
    Platform VARCHAR(50),
    Year_of_Release FLOAT,
    Genre VARCHAR(50),
    Publisher VARCHAR(100),
    NA_Sales FLOAT,
    EU_Sales FLOAT,
    JP_Sales FLOAT,
    Other_Sales FLOAT,
    Global_Sales FLOAT,
    Critic_Score FLOAT,
    Critic_Count FLOAT,
    User_Score VARCHAR(10),
    User_Count FLOAT,
    Developer VARCHAR(100),
    Rating VARCHAR(10)
);</i>

Populate the table with video game sales data (e.g., from a CSV file or manually).

**Configure Environment Variables:**
Set the following environment variables for database access:
DB_USERNAME: Your MySQL username.
DB_PWD: Your MySQL password.

Example (Linux/Mac):
<i>export DB_USERNAME="your_username"
export DB_PWD="your_password"</i>

Example (Windows):
<i>set DB_USERNAME=your_username
set DB_PWD=your_password</i>

Run the Code: Open the Jupyter Notebook or execute the Python script in your preferred environment.

<h2>Running the Tests</h2>

**Breakdown of Tests**
The code includes two main problems/tests:

**Problem 1: Average Global Sales Before vs. After 2005**
Objective: Determine whether the average global sales of video games were higher before or after 2005.
Method: Executes SQL queries to calculate the average Global_Sales for games released before 2005 and after 2005, then compares the results.
Output: Prints the average sales values and a conclusion (e.g., "Average of global sales was higher before 2005").

**Problem 2: Labeling Records Pre-2005 and Post-2005**
Objective: Add a new column to the dataset labeling games as "pre_2005" or "post_2005" based on their Year_of_Release.
Method: Uses a SQL CASE statement to create the label column and retrieves the updated dataset.
Output: Displays the first few rows of the updated DataFrame with the new label column.
To run these tests:

Open the Jupyter Notebook in an environment like Jupyter Lab or VS Code.
Execute each cell sequentially to see the outputs.
Ensure the MySQL connection is active (conn) before running the SQL queries.

**Deployment**
This project is designed for local execution and analysis. To deploy it in a production environment:

**Containerization:** Use Docker to containerize the Python environment and MySQL database.
Web Application: Integrate the code into a Flask or Django app to serve results via a web interface.
Cloud Hosting: Deploy the database on a cloud service like AWS RDS and the Python code on a service like AWS Lambda or Heroku.

**Author**
Name: Oluwatomiwa Oladele
Contact: github.com/ladhenrytom

**License**
This project is licensed under the MIT License - see the  file for details. 

**Acknowledgement**
pandas: For powerful data manipulation capabilities.
sqlalchemy & pymysql: For seamless database connectivity.
Video Game Sales Dataset: The original dataset creators (if known) for providing the data used in this analysis.
