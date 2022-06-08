# Analysis of different Currencies

## Purpose
The task was to create a report that includes what cryptocurrencies are on the trading market and how they could be grouped for classification for potential investing. 

Since the data isn't of the best quality it needs to be processed so it can fit into machine-learning models of the unsupervised variety as well as the implementation of clustering algorithms

## Summary

What was done initially to the dataset was cleaning:
* Making sure the Crypto is trading.
* Dropping that column becuase it is no longer needed.
* Dropping columns with missing data.
* Making sure coins have been mined from this Crypto.
* Splitting "CoinName" column from the main DataFrame to its own.

![Cleaned_Dataframe](https://github.com/Cyber-Wolfe/Crypto_Analysis/blob/main/Captures/Cleaned_Dataframe.PNG)

Next was setting "ProofType" and "Algorithm" to dummy data for the sake of using the data for machine-learning.

The data was set to a scaler, fit_transformed and then reduced with Principal-Component-Analysis to three components and then renamed for the ease of reading as such:

Next was acquiring the Kmeans so we can have the dataset placed into an Elbow curve:

Then the CoinName and PC data were placed back into the cleaned set for clustering:

The Clustered_Df was then used for a 3D scatter plot:

Lastly, the TotalCoinSupply and TotalCoinsMined columns were scaled and fit transformed to fit a new DataFrame to be used for our final Hvplot:

## Conclusion

Essentially from what the data had given us, is that all of the coins in that cluster that aren't at 0 mined are worthwhile investments.  As long as the coins mined is equal to or more than coins in supply it is a worthwhile investment. 
