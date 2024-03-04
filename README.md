# nosql-challenge
## Overview
The purpose of this project is to implement the skills learned and tools introduced in Module 12 to evaluate some of the food hygiene ratings data for establishments across the United Kingdom in order to help journalists and food critics decide where to focus future articles for a food magazine, Eat Safe, Love.

## Tools
- Jupyter Notebook
- Pandas
- Pretty Print
- PyMongo
- Python

## Project Structure
### Part 1: Database and Jupyter Notebook Set Up
1. Import the data provided in the establishments.json file from the Terminal. Name the database uk_food and the collection establishments. Text used to import data can be found in the markdown cell in the notebook.
1. Within notebook, import the libraries needed: PyMongo and Pretty Print.
1. Create an instance of the Mongo Client.
1. Confirm that the database has been created and loaded the data properly:
	- List the databases in MongoDB to confirm that uk_food is listed.
	- List the collection(s) in the database to ensure that establishments is there.
	- Find and display one document in the establishments collection using find_one and display with pprint.
1. Assign the establishments collection to a variable to prepare the collection for use.


### Part 2: Update the Database
Make the following changes to the establishments collection:
1. A new halal restaurant just opened in Greenwich, but hasn't been rated yet and should be included in the analysis.
1. Find the BusinessTypeID for "Restaurant/Cafe/Canteen" and return only the BusinessTypeID and BusinessType fields.
1. Update the new restaurant with the BusinessTypeID found.
1. Establishments in Dover should be excluded. Perform a check to see how many documents contain the Dover Local Authority. Then, remove any establishments within the Dover Local Authority from the database, and check the number of documents to ensure they were deleted.
1. Some of the number values are stored as strings, when they should be stored as numbers.
	- Use update_many to convert latitude and longitude to decimal numbers.
	- Use update_many to convert RatingValue to integer numbers.

### Part 3: Exploratory Analysis
Eat Safe, Love has specific questions they want answered, which will help them find the locations they wish to visit and avoid.
1. Which establishments have a hygiene score equal to 20?
1. Which establishments in London have a RatingValue greater than or equal to 4?
1. What are the top 5 establishments with a RatingValue of 5, sorted by lowest hygiene score, nearest to the new restaurant added, "Penang Flavours"?
1. How many establishments in each Local Authority area have a hygiene score of 0? Sort the results from highest to lowest, and print out the top ten local authority areas.

----
## Sources
I referenced several class actvities and applicable documentation to complete this challenge.