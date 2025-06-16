# IBM-Applied-Data-Science-Capstone

In this hands-on project, we are tasked with predicting if the first stage of the SpaceX Falcon 9 rocket will land successfully. SpaceX advertises Falcon 9 rocket launches on its website with a cost of 62 million dollars; other providers cost upward of 165 million dollars each, much of the savings is due to the fact that SpaceX can reuse the first stage. Therefore if we can determine if the first stage will land, we can determine the cost of a launch. With the help of data science findings and models, a competing startup can make more informed bids against SpaceX for a rocket launch.
![](https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBM-DS0321EN-SkillsNetwork/labs/module_1_L2/images/Falcon9_rocket_family.svg)
![](https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBMDeveloperSkillsNetwork-DS0701EN-SkillsNetwork/lab_v2/images/landing_1.gif)

The project develops through different steps:
### Part 1 - Data Collection using API
SpaceX launch data was gathered from SpaceX REST API (https://github.com/r-spacex/SpaceX-API), which has different endpoints. Specifically, we worked with the endpoint: api.spacexdata.com/v4/launches/past.

### Part 2 - Data Scraping
Web scraping of Falcon 9 historical launch records from the Wikipedia page titled “List of Falcon 9 and Falcon Heavy launches” (https://en.wikipedia.org/wiki/List_of_Falcon_9_and_Falcon_Heavy_launches) was performed using the BeautifulSoup library.

### Part 3 - Data Wrangling
We used the API again targeting different endpoints to gather specific missing data, such as Booster Version, Launch Site and Payload Data. The ‘mission outcome’ column in the raw data was also converted into Training Labels with 1 (the booster successfully landed) or 0 (unsuccessful).

### Part 4 - Exploratory Data Analysis using Pandas
Categorical plots, scatter plots and bar plots were generated to visualize the relationship between different variables.

### Part 5 - Exploratory Data Analysis using SQL
We performed SQL queries to further interrogate the dataset and gain insights into which features influence the mission outcome.

### Part 6 - Interactive Maps and Dashboards
We built an interactive map using Folium to visualize the launch sites as well as a Plotly Dashboard.
The Plotly Dashboard has been deployed to Render.com using the free hosting plan and is available at the following URL: https://ibm-applied-data-science-capstone-0esu.onrender.com.

### Part 7 - Predictive Analysis using Classification Models
In this phase, we standardized the data and split it into training and test sets. We created machine learning models using: 
- Logistic Regression,
- Support Vector Machine (SVM),
- Decision Tree Classifier, and
- K-Nearest Neighbors (KNN).
 
Finally, we performed a Grid Search to identify the optimal hyperparameters for each classification model.
