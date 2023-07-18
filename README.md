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
Handling Null values: The two mentioned above did not contain any null value. It was checked using IsNull().
 Moreover, as there were no null values in the two datasets, we continued with further data analysis.
In this project, we will only use the data from restaurants in Delhi. We need to get data only for Delhi from the dataset. The country code '1' and city 'Delhi' are selected to get the data for the restaurant in Delhi.
We also got the number of cuisines a particular restaurant has from the Cuisines column. The num_cuisine column will be the new column in the data frame, which shows the number of cuisines. It is done by using the splitting the string.
The dataset after this operation will have an additional column name num_cuisines.
The following bar graph can visualize the number of aggregate ratings:
It can be seen from the graph that most of the restaurant has ratings between 3.0- 3.5. 
 One more plot was made to get the restaurant details on the map for that we used Plotly library. The plotly scatter_mapbox plot is used to get the scatter points according to the restaurant's longitude and latitude as mentioned in the dataset. In addition, when we bring the cursor to one of the points, we can see the restaurant name, rating, and location.
The above plot shows the Delhi map with each restaurant's location in the dataset. As it can be seen from the range scale the darker, the green colour gets, the more is the restaurant's rating.
 To find out how many top cuisines a restaurant serves, we used Counter(). To perform this operation, we split the cooking from the Cuisines column and then used Counter() to get the count of every cuisine.
The graph below shows the ten cuisines and how many restaurants serve those cuisines. It can also be said that these are the top 10 cuisines in Delhi. Also, we can see that there are 78 types of cuisines available in Delhi.
 Furthermore, similarly, from the column num_cuisines, we can visualize how many cuisines are served in the restaurant. 

K-Means clustering: K-means clustering is used in this project to determine where the high-rated restaurant is located in Delhi. These clusters are formed using the res_data's Longitude, Latitude and Aggregate rating from the res_data. We set the number of clusters to 7.

The 7 clusters displayed in the plot show the different zones of Delhi, with the labels showing the average rating of all restaurants in the particular zone.  We found that the cluster in the middle indicates that the central part of Delhi has a higher rating restaurant.
       
After analyzing the first dataset, we then worked on our second dataset. We found the types of comfort food for different moods from this dataset. As stated previously, we will only use two columns from this data frame.

 
# IV.	OUTCOMES 
To get the three comfort food from the above dataset, we made a search_comfort() which holds the parameter mood and searches for the foods for that particular food. We used the comfort food reasons column to split the value in this function and converted all the text in lowercase. These texts are stored in the temp variable. If the user specifies the mood, it will find the comfort food by splitting the text from comfort_food columns and making a dictionary for a particular mood.
Another function was created find_my_comfort, which takes the user's mood and will display the comfort foods. The comfort foods for happy are:

 Based on the one food from the comfort food, we found the restaurant which serves that particular food. This was done by selecting the rows from comfort_food that contains pizza. We sort the data frame by the Aggregate rating to get the highest rating. The output contains only the top rating restaurant having pizza in their menu and details.


 Using the above data, we plotted the location of these restaurants on the map using Plotly scatter_mapbox. This map shows the location of 3 restaurants, their cuisines, and their rating.

 
# V.	REFERENCES
•	Plotlygraphs, "Builtin colorscales," Builtin Colorscales, 03-Jul-2019. [Online]. Available: https://plotly.com/python/builtin-colorscales/.
•	S. Mehta, "Zomato Restaurants Data," Kaggle, 13-Mar-2018. [Online]. Available: https://www.kaggle.com/shrutimehta/zomato-restaurants-data 
•	D. Ong, "Yelp restaurant recommendation system - capstone project," Medium, 25-Oct-2020. [Online]. Available: https://towardsdatascience.com/yelp-restaurant-recommendation-system-capstone-project-264fe7a7dea1
•	NLTK. [Online]. Available: https://www.nltk.org/_modules/nltk/stem/wordnet.html
•	BoraPajo, "Food choices," Kaggle, 23-Apr-2017. [Online]. Available: https://www.kaggle.com/borapajo/food-choices 


