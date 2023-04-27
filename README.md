# Cryptocurrencies
#### Module 19 Challenge


## Project Overview
### Purpose
The purpose of this anlaysis is to use unsupervised machine learning to analyze a dataset of cryptocurrencies to help uncover trends in order to pitch and convince Accountability Accounting to invest in cryptocurrencies.  The cryptocurrencies will be clustered in groups according to their features, and a report will be generated for use in the sales pitch.

The technical analysis will consist of 4 parts:
+ Preprocessing the data for Principal Component Analysis **(PCA)**,
+ Reducing the data dimension using PCA,
+ Clustering Cryptocurrencies using K-Means,
+ Visualizing classification results with 2D and 3D scatter plots.

### Resouces
+ Data Source: crypto_data.csv from [CryptoCompare](https://min-api.cryptocompare.com/data/all/coinlist)
+ Software: Python 3.10.11, Anaconda Navigator 1.11.2, Jupyter Notebook 6.5.4

## Results
#### Preprocessing Data for PCA
+ Keep only cryptocurrencies being traded:

<img width="549" alt="image" src="https://user-images.githubusercontent.com/113741694/234964644-0f947041-ea13-4ea7-9228-557b1d6c6e0b.png">

+ Drop "IsTrading" Column

<img width="488" alt="image" src="https://user-images.githubusercontent.com/113741694/234964790-005ac4f4-4677-4c40-80a4-67a6651915d3.png">

+ Remove rows with at least 1 null value

<img width="458" alt="image" src="https://user-images.githubusercontent.com/113741694/234964907-5e817d5a-aef0-4999-a1c6-c55d9cb8c567.png">

+ Keep only rows where coins were mined

<img width="454" alt="image" src="https://user-images.githubusercontent.com/113741694/234965024-748f0a3f-8204-4210-87c9-bab40cce0a46.png">

+ Drop "CoinName" column

<img width="311" alt="image" src="https://user-images.githubusercontent.com/113741694/234969909-9d9d3e5d-e63e-471b-a5aa-dc70a45ace9e.png">

+ Create new DataFrame with the Coin Names column

<img width="400" alt="image" src="https://user-images.githubusercontent.com/113741694/234970145-e3aa68a7-5d10-450e-8a6b-fc0b4a73fffe.png">

+ Use get_dummies() to create variables for text features

<img width="751" alt="image" src="https://user-images.githubusercontent.com/113741694/234970481-85df1d0f-f68b-47b5-9d0a-8f966e9c7085.png">

+ Standardize data with StandardScaler()

<img width="447" alt="image" src="https://user-images.githubusercontent.com/113741694/234970637-3f5f56d4-73d1-43fe-b686-a256d5700835.png">

#### Reducing Data Dimensions Using PCA
+ Reduce dimensions with PCA 

<img width="274" alt="image" src="https://user-images.githubusercontent.com/113741694/234975486-b6fe23f0-e1a0-46a0-bc8f-df97a5194c1e.png">

+ Create a new DataFrame with the principal components

<img width="433" alt="image" src="https://user-images.githubusercontent.com/113741694/234975676-e19b03da-db1b-4c98-95a9-6367b230206f.png">

#### Clustering Cryptocurrencies Using K-Means
+ Find the best value for "k" using the elbow curve

<img width="466" alt="image" src="https://user-images.githubusercontent.com/113741694/234975748-3854b9cb-4f7f-49bd-975c-9299cd96c493.png">

<img width="532" alt="image" src="https://user-images.githubusercontent.com/113741694/234967040-3254a088-1182-45c1-9477-a633a8984e4a.png">

+ Initialize and fit the K-Means model, and predict clusters

<img width="266" alt="image" src="https://user-images.githubusercontent.com/113741694/234967329-731c247e-bdcc-4c85-a1b9-0a7ce552108d.png">

<img width="455" alt="image" src="https://user-images.githubusercontent.com/113741694/234967397-66c6bd39-9efa-4ae6-a039-b9733c3635d9.png">

+ Create new DataFrame with the same index as crypto_df DataFrame

<img width="649" alt="image" src="https://user-images.githubusercontent.com/113741694/234975943-1e54fcb2-3e2b-4427-9733-36c7c402a016.png">


#### Visualizing Cryptocurrencies Results
+ 3D-Scatter plot with PCA data and the clusters

<img width="347" alt="image" src="https://user-images.githubusercontent.com/113741694/234967875-576e96c0-edf2-4fcd-be4a-ca8a4318810c.png">

<img width="559" alt="image" src="https://user-images.githubusercontent.com/113741694/234968038-731290f0-18dc-4005-bda0-433950964840.png">

+ New table of tradable cryptocurrencies

<img width="653" alt="image" src="https://user-images.githubusercontent.com/113741694/234976180-5d607a99-1012-41b7-b0f2-44c3a596945e.png">

+ Total number of tradable cryptocurrencies

<img width="453" alt="image" src="https://user-images.githubusercontent.com/113741694/234976254-dc9dde7e-542d-4d1f-929b-0cf68ba99f54.png">

+ New DataFrame with the index from clustered_df

<img width="710" alt="image" src="https://user-images.githubusercontent.com/113741694/234976354-a181e010-ea93-432d-bab3-6d307cb913b4.png">

+ 2D Scatter Plot using hvplot

<img width="604" alt="image" src="https://user-images.githubusercontent.com/113741694/234976410-2a203454-5338-4157-8726-2a3769a75fcb.png">












