# Cryptocurrencies

# Credit_Risk_Analysis

## Resources
- Anaconda 4.11.0
- Jupyter Notebook 6.0.3
- Python 3.7.6
- Pandas
- Plotly
- scikit-learn
- Data:  crypto_data.csv

## Project Overview

With an understanding of what unsupervised learning is used for, how to process data, how to cluster, how to reduce dimensions, and how to reduce the principal components using PCA - it’s time to put all these skills to use by creating an analysis for clients who are preparing to get into the cryptocurrency market.

A company is interested in offering a new cryptocurrency investment portfolio for its customers. The company, however, is lost in the vast universe of cryptocurrencies. I was asked to create a report that includes details of what cryptocurrencies are on the trading market and how they could be grouped to create a classification system for this new investment.

The I worked with was not ideal, so it needed to be processed to fit the machine learning models. Since there is no known output for what the client is looking for, I have decided to use unsupervised learning. To group the cryptocurrencies, I decided on a clustering algorithm. I used data visualizations to share the findings.

Project consisted of four technical analysis deliverables. as follows:

Deliverable 1: Preprocessing the Data for PCA
Deliverable 2: Reducing Data Dimensions Using PCA
Deliverable 3: Clustering Cryptocurrencies Using K-means
Deliverable 4: Visualizing Cryptocurrencies Results

## Preprocessing the Data for PCA 

Preprocessed the dataset in order to perform PCA.  Used understanding of Pandas to perform the following steps:

The following six preprocessing objectives have been met:

- All cryptocurrencies that are not being traded are removed 
- All cryptocurrencies that do not have a defined algorithm are removed 
- The IsTrading column is dropped 
- All the rows that have at least one null value are removed 
- All the rows that do not have coins being mined are removed 
- The CoinName column is dropped 
- A new DataFrame is created that stores all cryptocurrency names from the CoinName column and retains the index from the crypto_df DataFrame 
- The get_dummies() method is used to create variables for the text features, which are then stored in a new DataFrame
The features from the DataFrame have been standardized using the StandardScaler fit_transform() function 

![Crypto Deliverable 1](https://github.com/PatriciaCB1/Credit_Risk_Analysis/blob/main/Images/Naive%20Random%20Oversampler.png) 

## Reducing Data Dimensions Using PCA

Using knowledge of how to apply the Principal Component Analysis (PCA) algorithm, I reduced the dimensions of the X DataFrame to three principal components and placed these dimensions in a new DataFrame.

The following objectives were acheived:

- The PCA algorithm reduced the dimensions of the X DataFrame down to three principal components 
- The pcs_df DataFrame was created and has the following three columns, PC 1, PC 2, and PC 3, and has the index from the crypto_df DataFrame 

![Crypto Deliverable 2](https://github.com/PatriciaCB1/Credit_Risk_Analysis/blob/main/Images/Naive%20Random%20Oversampler.png) 

## Clustering Cryptocurrencies Using K-means

Using knowledge of the K-means algorithm, I created an elbow curve using hvPlot to find the best value for K from the pcs_df DataFrame created. I then ran the K-means algorithm to predict the K clusters for the cryptocurrencies’ data.

The followig clustering objectives were met:

- The K-means algorithm is used to cluster the cryptocurrencies using the PCA data, where the following steps have been completed:
    - An elbow curve is created using hvPlot to find the best value for K 
    - Predictions are made on the K clusters of the cryptocurrencies’ data 
    - A new DataFrame is created with the same index as the crypto_df DataFrame and has the following columns: Algorithm, ProofType, TotalCoinsMined, TotalCoinSupply, PC 1, PC 2, PC 3, CoinName, and Class 

![Crypto Deliverable 3](https://github.com/PatriciaCB1/Credit_Risk_Analysis/blob/main/ImagesNaive%20Random%20Oversampler.png) 

![Elbow Curve](https://github.com/PatriciaCB1/Credit_Risk_Analysis/blob/main/Images/Naive%20Random%20Oversampler.png) 

## Visualizing Cryptocurrencies Results

Using knowledge of creating scatter plots with Plotly Express and hvplot, I visualized the distinct groups that correspond to the three principal components you created in the prior step, then created a table with all the currently tradable cryptocurrencies using the hvplot.table() function.

The following visualization goals were met:

- The clusters are plotted using a 3D scatter plot, and each data point shows the CoinName and Algorithm on hover 
- A table with tradable cryptocurrencies is created using the hvplot.table() function 
- The total number of tradable cryptocurrencies is printed 
- A DataFrame is created that contains the clustered_df DataFrame index, the scaled data, and the CoinName and Class columns 
- A hvplot scatter plot is created where the X-axis is "TotalCoinsMined", the Y-axis is "TotalCoinSupply", the data is ordered by "Class", and it shows the CoinName when you hover over the data point 

![Crypto Deliverable 4](https://github.com/PatriciaCB1/Credit_Risk_Analysis/blob/main/Images/Naive%20Random%20Oversampler.png) 

![Crypto Scatterplot](https://github.com/PatriciaCB1/Credit_Risk_Analysis/blob/main/Images/Naive%20Random%20Oversampler.png) 

![Crypto Table 4](https://github.com/PatriciaCB1/Credit_Risk_Analysis/blob/main/Images/Naive%20Random%20Oversampler.png) 

![Crypto 3D](https://github.com/PatriciaCB1/Credit_Risk_Analysis/blob/main/Images/Naive%20Random%20Oversampler.png)