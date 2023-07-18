# Mood-Based-Restaurant-Recommendation-System
In this project, we build a recommendation system depending on the user's mood. The system will require the data for different restaurants with their rating. The data analysis was done using various libraries for data cleaning and visualization. The data was visualized using map, box, and scatter plots which helped find the insights in data. The comfort food was found from another dataset and used to plot the recommended restaurant on the map.
# I.	INTRODUCTION

This project is based on the analysis of data of the restaurants and recommending the restaurants based on the user's mood. We analyzed and built a recommendation system using the two datasets based on restaurant and comfort foods.
# II.	DATASET

We have used two datasets in this project. The first dataset includes Zomato API data (zomato.csv) collected from Kaggle; it consists of 3879 rows and 25 columns. The restaurant data from different countries with the following columns/details are:
•	Restaurant Id: Unique id of every restaurant across various cities of the world
•	Restaurant Name: Name of the restaurant
•	 Country Code: Country in which restaurant is located
•	City: City in which restaurant is located
•	Address: Address of the restaurant
•	Locality: Location in the city
•	Locality Verbose: Detailed description of the locality
•	Longitude: Longitude coordinate of the restaurant's location
•	Latitude: Latitude coordinate of the restaurant's location
•	Cuisines: Cuisines offered by the restaurant
•	Average Cost for two: Cost for two people in different currencies
•	Currency: Currency of the country
•	Has Table booking: yes/no
•	Has Online delivery: yes/ no
•	Is delivering: yes/ no
•	Switch to order menu: yes/no
•	Price range: range of price of food
•	Aggregate Rating: Average rating out of 5
•	Rating colour: depending upon the average rating colour
•	Rating text: text-based on the rating of rating
•	Votes: Number of ratings cast by people

      The second dataset includes the details of various food choices and various information on the different types of food. It has 125 rows and 61 columns. Some of the valuable attributes of the 'food_choices.csv' are:
•	comfort_food_reasons: It contains different moods and emotions.
•	comfort_food: It has different types of foods for different moods.
     There are more columns in this dataset, but we only need these two columns to build our recommendation model.

# III.	RECOMMENDATION SYSTEM
 
Importing Libraries: The first step for this will be importing the required libraries that can be used to clean, analyze, and visualize the data. Following libraries are used in the project:
•	Pandas
•	Numpy
•	Seaborn
•	Matplotlib
•	Plotly
•	Collections
•	NLTK

Read the Data: After importing the library, we first need to read the CSV file on Jupyter notebook.
