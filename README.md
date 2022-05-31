# Education-and-Census-Data-Project

Based on project from Codecademy and completed in DB Browser for SQLite. - https://discuss.codecademy.com/t/data-science-independent-project-3-education-census-data/419947

# Project: Analyzing Education & Census Data
This project will take you off-platform and get you started in your own developer environment! Never done that before? Not to worry - we’ve shared some resources to help you down below. This project can be completed entirely on your own - or, you can join our Community Discord 47 and find someone to work with! Jump to the community support section to hear more about this.

This project is broken down into key questions that your client or company is looking to answer. As a data scientist, you’ll often become a resource to help businesses answer the key questions about the efficacy of existing or potential strategies & projects.

# Overview
# Objective
Your advice is needed by a team of policymakers seeking to make more informed decisions on education. Help them investigate how external factors may influence performance in state assessment exams for public high school students.

# Pre-requisites
In order to complete this project, we suggest that you have familiarity with the content in the following courses or lessons on the Codecademy platform:

- Manipulation 
- Queries 
- Aggregate Functions 
- Multiple Tables 

# Suggested Technologies
First, get the data. Depending on where you are on your Path, there may be multiple technology options you can use to complete this project - we suggest the following:

- DB Browser for SQLite 

Get started - hosting your project
DB Browser for SQLite 243 is a visual tool for working with SQLite databases. Follow the link to download the application for your computer.

SQLite can store an entire database in a single file, which usually has a .sqlite or .db extension. To open a database, select Open Database at the top of the window and browse for the file. Alternatively, you can choose to create a New Database by saving a file with the .sqlite or .db extension.
To import data from a CSV file into a table, select “File > Import > Table from CSV file…” and browse for the CSV file. (Note: All fields imported from the CSV file will have a data type of TEXT. Be sure to convert fields to numeric type as needed. See here 68 for how to do that.)


There are several tabs near the top of the window for working with the data:

Database Structure: View the tables in your database and the columns they contain.
Browse Data: Browse the data for each table.
Execute SQL: Write and execute SQL queries.
Project Tasks
You can download the data you’ll be using for this specific project here 22 and here 10.

# Basic Requirements
Let’s break this project down into a couple different parts.

# Explore tables: Start off by exploring each table separately.

How many public high schools are in each zip code? in each state?
The locale_code column in the high school data corresponds to various levels of urbanization as listed below. Use the CASE statement to display the corresponding locale_text and locale_size in your query result.
Hint: Try taking a look at using the substr() function to help look at each part of the locale_code for determining locale_text and locale_size.

locale_text	locale_code (locale_size)
City	11 (Large), 12 (Midsize), 13 (Small)
Suburb	21 (Large), 22 (Midsize), 23 (Small)
Town	31 (Fringe), 32 (Distant), 33 (Remote)
Rural	41 (Fringe), 42 (Distant), 43 (Remote)

What is the minimum, maximum, and average median_household_income of the nation? for each state?

Joint analysis: Join the tables together for even more analysis.

Do characteristics of the zip-code area, such as median household income, influence students’ performance in high school?
Hint: One option would be to use the CASE statement to divide the median_household_income into income ranges (e.g., <$50k, $50k-$100k, $100k+) and find the average exam scores for each.
Additional Challenges
Intermediate Challenge

On average, do students perform better on the math or reading exam? Find the number of states where students do better on the math exam, and vice versa.
Hint: We can use the WITH clause to create a temporary table of average exam scores for each state, with an additional column for whether the average for math or reading is higher. (Note: Some states may not have standardized assessments, so be sure to also include an option for No Exam Data) Then, in your final SELECT statement, find the number of states fitting each condition.
Advanced Challenge

What is the average proficiency on state assessment exams for each zip code, and how do they compare to other zip codes in the same state?
Note: Exam standards may vary by state, so limit comparison within states. Some states may not have exams. We can use the WITH clause to create a temporary table of exam score statistic for each state (e.g., min/max/avg) - then join it to each zip-code level data to compare.
Resources & Support
Project-specific resources
SQLite Documentation 17 &
SQLite Tutorial 24
SQLite substr() Function 15
US Census Data 32
Public HS Data 20
State Assessment Data 13
General Resources
How to get set-up for coding on your computer 20
What is a Relational Database Management System? 5
What you need to know about Git, GitHub & Coding in Teams
How developer teams work 1
First steps in tackling a group project
Resource on writing pseudocode 2 to get started with off-platform projects
