# Crypto-Clustering

Module 10 Challenge: Crypto Clustering


Background
In this Challenge, you’ll assume the role of an advisor at one of the top five financial advisory firms in the world. Competitors are fierce, so you want to propose a novel approach to assembling investment portfolios that are based on cryptocurrencies. Instead of basing your proposal on only returns and volatility, you want to include other factors that might impact the crypto market—leading to better performance for your portfolio.
When you present the idea, your manager loves it! So, you’re asked to create a prototype for submitting your crypto portfolio proposal to the company board of directors.

What You're Creating
In this Challenge, you’ll combine your financial Python programming skills with the new unsupervised learning skills that you acquired in this module.
You’ll create a Jupyter notebook that clusters cryptocurrencies by their performance in different time periods. You’ll then plot the results so that you can visually show the performance to the board.
The CSV file that’s provided for this Homework contains the price change data of cryptocurrencies in different periods.

Files
Download the following files to help you get started:
Module 10 Challenge files

Instructions
Use the starter code file to complete the tasks outlined in the Instructions. The steps for this assignment are divided into the following sections:


Import the Data (provided in the starter code)


Prepare the Data (provided in the starter code)


Find the Best Value for k Using the Original Data


Cluster Cryptocurrencies with K-means Using the Original Data


Optimise Clusters with Principal Component Analysis


Find the Best Value for k Using the PCA Data


Cluster the Cryptocurrencies with K-means Using the PCA Data


Visualise and Compare the Results



Note: For the purpose of this assignment, assume that k refers to lowercase k. The instructions will specify "uppercase K" where necessary.


Find the Best Value for k Using the Original Data
In this section, you will use the elbow method to find the best value for k.


Code the elbow method algorithm to find the best value for k. Use a range from 1 to 11.


Plot a line chart with all the inertia values computed with the different values of k to visually identify the optimal value for k.


Answer the following question: What is the best value for k?



Cluster Cryptocurrencies with K-means Using the Original Data
In this section, you will use the K-means algorithm with the best value for k (found in the previous section) in order to cluster the cryptocurrencies according to the price changes of cryptocurrencies provided.


Initialize the K-means model with four clusters by using the best value for k.


Fit the K-means model using the original data.


Predict the clusters to group the cryptocurrencies using the original data. View the resulting array of cluster values.


Create a copy of the original data and add a new column with the predicted clusters.


Using hvPlot, create a scatter plot by setting x="price_change_percentage_24h" and y="price_change_percentage_7d". Colour the graph points with the labels found using K-means. Then, add the crypto name in the hover_cols parameter to identify the cryptocurrency represented by each data point.



Optimise Clusters with Principal Component Analysis
In this section, you will perform a principal component analysis (PCA) and reduce the features to three principal components.


Create a PCA model instance and set n_components=3.


Use the PCA model to reduce to three principal components. View the first five rows of the DataFrame.


Retrieve the explained variance to determine how much information can be attributed to each principal component.


Answer the following question: What is the total explained variance of the three principal components?


Create a new DataFrame with the PCA data. Be sure to set the coin_id index from the original DataFrame as the index for the new DataFrame. Review the resulting DataFrame.



Find the Best Value for k Using the PCA Data
In this section, you will use the elbow method to find the best value for k by using the PCA data.


Code the elbow method algorithm and use the PCA data to find the best value for k. Use a range from 1 to 11.


Plot a line chart with all the inertia values computed with the different values of k to visually identify the optimal value for k.


Answer the following questions: What is the best value for k when using the PCA data? Does it differ from the best k value found using the original data?



Cluster Cryptocurrencies with K-means Using the PCA Data
In this section, you will use the PCA data and the K-means algorithm with the best value for k (found in the previous section) in order to cluster the cryptocurrencies according to the principal components.


Initialize the K-means model with four clusters by using the best value for k.


Fit the K-means model by using the PCA data.


Predict the clusters to group the cryptocurrencies by using the PCA data. View the resulting array of cluster values.


Create a copy of the DataFrame with the PCA data and add a new column to store the predicted clusters.


Using hvPlot, create a scatter plot by setting x="PC1" and y="PC2". Colour the graph points with the labels found using K-means. Then, add the crypto name in the hover_cols parameter to identify the cryptocurrency represented by each data point.



Visualise and Compare the Results
In this section, you will visually analyse the cluster analysis results by observing the outcome with and without using the optimisation techniques.


Create a composite plot using hvPlot and the plus (+) operator to compare the elbow curve that you created to find the best value for k with the original data and the PCA data.


Create a composite plot using hvPlot and the plus (+) operator to compare the cryptocurrencies clusters using the original data and the PCA data.


Answer the following question: After visually analysing the cluster analysis results, what is the impact of using fewer features to cluster the data by using K-means?
