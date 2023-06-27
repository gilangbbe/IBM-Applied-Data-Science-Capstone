# 🚀 Project Background
SpaceX advertises Falcon 9 rocket launches on its website with a cost of 62 million dollars; other providers cost upward of 165 million dollars each, much of the savings is because SpaceX can reuse the first stage. Therefore if we can determine if the first stage will land, we can determine the cost of a launch. This information can be used for another company to bid against SpaceX for a rocket launch.

The aim of this project is to predict if the Falcon 9 first stage will successfully land.

Datasest is from SpaceX REST API  : _api.spacexdata.com/v4/_

Web scraping from Wikipedia       : _https://en.wikipedia.org/w/index.php?title=List_of_Falcon_9_and_Falcon_Heavy_launches&oldid=1027686922_

# 📄 Problems to be Answered
* What variables affect the success of the first stage landing?
* What are the conditions which will allow SpaceX to achieve the best landing success rate? 
* What is the best algorithm that can be used for predicting the successfull of a rocket launch? 

# 📄 Methodology
* Data collection methodology : 
  * SpaceX REST API 
  * Web Scraping from Wikipedia
* Data wrangling : 
  * Dropping unnecessary variables
  * One Hot Encoding for classification models
* Perform exploratory data analysis (EDA) using visualization and SQL
* Build an Interactive Map with Folium 
* Build a Dashboard with Plotly Dash

# 📄 Conclusion
* The success of a mission can be explained by several factors such as the launch site, the orbit and especially the number of previous launches. Indeed, we can assume that there has been a gain in knowledge between launches that allowed to go from a launch failure to a success.
* Depending on the orbits, the payload mass can be a criterion to take into account for the success of a mission. Some orbits require a light or heavy payload mass. But generally low weighted payloads perform better than the heavy weighted payloads
* Depending on the launch sites, CCAFS SLC 40 and KSC LC 9A has higher rate of success when payload mass is higher than 10000kg, in contrast where KSC LC 39A has 100% success rate when payload mass is less than 5000kg
* For this dataset, we choose the Decision Tree Algorithm as the best model even if the test accuracy between all the models used is identical. We choose Decision Tree Algorithm because it has a better train accuracy. 
