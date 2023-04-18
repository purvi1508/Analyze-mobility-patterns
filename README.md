# Analyze-mobility-patterns
The dataset (link) contains location data of users collected from GPS-enabled mobile devices over a period of time. It includes latitude, longitude, altitude, and time-stamp information for each location point. The data is organized by individual users, with each user having multiple trajectories.

PART 1: WRITE A FUNCTION TO CALCULATE THE TOTAL DISTANCE TRAVELED BY EACH USER IN THE DATASET.

The Haversine formula is used to determine the distance between two places based on 
the information of latitude, longitude and Altitude.

The length of the dataset is 24876978 thus for the ease of calculation new_df has been 
created which gets the top 500 rows with each unique 'individual_id' and use 
multiprocessing library to calculates the total distance traveled by each individual in the 
DataFrame.

New_df contains 87248 rows.
The result is as follows: 

https://docs.google.com/document/d/1A7SajI0_VCj3CCCaWRN9sqFksS8TPF-6DLTHYaF7bSg/edit

PART 2:  WRITE A FUNCTION TO EXTRACT AND VISUALIZE THE SPATIAL AND TEMPORAL HOTSPOTS OF BEJING CITY.

In order to extract and visualize the spatial and temporal hotspots i have used 2 
methods:

 I have used DBSCAN because it can discover clusters that are both 
geographically and Since the dataset is quite large to visualize it had been 
grouped according to individual_id and randomly 7000 dataset has been 
selected by the provided groups. So that it could shows the trajectory of 
individual_id 1 over time, with latitude, longitude, altitude, date, and time 
information for each location. It also includes trajectory_id, which may be used 
to distinguish different trajectories for the same individual. The individual_id's 
Silhouette score here quantifies how similar an object is to its own cluster in 
comparison to other clusters. 

A score of 1 indicates that the object is highly 
similar to its own cluster and quite different from other clusters, whereas a 
score of -1 suggests the reverse. The scale goes from -1 to 1.

Silhouette score: 
https://docs.google.com/document/d/1BNmDfNzFQO9sX4o60XSj7ti8TIIvCz
Qoe_RZD1M6-LA/edit
