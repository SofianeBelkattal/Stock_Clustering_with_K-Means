**Stock Clustering with K-Means**

This project applies the K-Means clustering algorithm to a set of U.S. stocks using two features: annualized return and annualized return variance. The goal is to group stocks based on their risk–return profile and visualize how they cluster.

Data is downloaded from Yahoo Finance using the yfinance library. The best number of clusters is evaluated using both the Elbow Method and the Silhouette Score.

**Overview**

Steps performed in this project:

Download historical stock data.

Compute daily returns.

Calculate annualized return and annualized variance.

Prepare the dataset for clustering.

Evaluate different values of k using:

the Elbow Method

the Silhouette Score

Visualize the selected clustering with centroids.

**Stock List**

The analysis uses the following tickers:

NVDA, OPEN, NIO, ONDS, PLUG,
BBAI, GOOGL, ABEV, BBWI, VICI,
HL, RXRX, ORCL, NOK, CMG,
CRWV, PSNYW, TIGR, NTR, HALO,
SENEB, CFFI


Data is collected from January 1, 2023 to November 26, 2025.

**Method
Return and Variance**

Daily percentage changes are computed from closing prices.
Annualized values are obtained by multiplying:

mean daily return × 252

daily return variance × 252

These two values form the input features for clustering.

**Clustering**

K-Means is applied for k values ranging from 2 to 9.
For each value of k, the code records:

inertia (Elbow Method)

silhouette score

These help select a reasonable number of clusters.

**Scaling**

Because variance and return may be on different scales, scaling with StandardScaler can be applied to improve clustering results.



**How to Run it**

Open the notebook or Python script.

Ensure internet access (needed for yfinance).

Run all cells or execute the script.

The code will generate:

a table with each stock’s return and variance

the Elbow and Silhouette plots

a scatter plot showing clusters and centroids (if included)

**Notes and Limitations**

Only two features are used; adding more could improve the quality of clustering.

Outliers may influence centroid locations.

K-Means assumes spherical clusters, which may not always match financial data.

Results depend on the time window and stock selection.

**Possible Improvements**

Add more financial features (beta, sector, volume, Sharpe ratio)

Try other clustering algorithms

Visualize clusters more clearly with labels

Use rolling windows to compare clusters over time