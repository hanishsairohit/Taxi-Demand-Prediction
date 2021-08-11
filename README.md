# Taxi-Demand-Prediction


* The main objective of this problem is to predict the the number of pickups for a given location.
* Analysed the data and extracted basic features like speed,time for each trip in the dataset.
* Clustered all the locations in the dataset using k-means, as k-means algorithm creates clusters of same size.
* Divided the whole timeframe (i.e, from january 2016 to march 2016) into 10 min interval bins and assigned each datapoint with a pickup_bin based on the pickup time of the trip. Calculated number of pickups that happened at each 10 min interval time of every cluster (location).
* Visualized the timeseries of number of pickups for every cluster. 
* Featurized Train and test data with:
         - Top 4 important frequencies and amplitudes from the fourier transform of the last 24hr pickups
         - Number of pickups that happpened in the last 5 time intervals of a cluster (location).
         - Relative number of pickups at a cluster with the sum of total number of pickups happened across all the clusters in the last
        5 time intervals.
         - latitude and longitude of the cluster centroid.
         - Exponential weighted moving average.
* Applied SGD Regressor, Linear Regression, Random Forest Decision Trees Regressor and XGBoost Regressor on top of the extracted features. 
* Compared all the models using PrettyTable.
