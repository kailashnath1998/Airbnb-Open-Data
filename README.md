## AirBnB

### Installations

The project has been done in the Anaconda enviroment with python 3.7. Moreover I have used the following python libraries:

- Matplotlib
- NumPy
- Pandas
- Seaborn
- Sklearn

### Motivation

I was interested in exploring the AirBnB dataset for Seattle. Some of the questions that I have analyzed are:

- How to get the best price?
- How to get better reviews?
- Can a machine learning algorithm predict listing prices?

### Files

The Ipynb notebook showcases the analysis done in order to explore the dataset, the data prepartion and wrangling as well as the building of prediction models in order to answer the questions above. The notebook contains markdown cells to help with documentation of the steps as well as to communicate findings based on each analysis.

For reference an HTML version of the notebook is also available.

Lastly, the data folder contains the dataset from Kaggle (https://www.kaggle.com/airbnb/seattle). It contains 3 files:

- calendar.csv: calendar availability of listings and price
- listings.csv: information about all the available listings
- reviews.csv: listing reviews by the users

### Summary Of The Results

- Question 1: How to achieve the best price?

    From the correlation matrix below we can immediately see which parameters correlate most with the price. The number of people that the list can include is the most significant factor, but amenities are also key.

    ![Correlation](images\correlation.png)

    In fact, the relationship between housing and pricing is linear , showing how important it is to manage more people if you want a good price.

    Location is also important when it comes to pricing. According to Seattle statistics, the most expensive area (Magnolia) was twice as expensive as the lowest cost area (Dellridge).

- Question 2 :How to achieve good reviews?

    From the heat map above we can see that the most important factor in getting good reviews is to respond to all the guests' requests, which is not too surprising.

    ![Review Score](images\review-score.PNG)

    There is a small correlation between bathrooms, price and review score. This might be due to standard. Higher standard listings gets better reviews. limitations on maximum nights are bad for review score and availablity is also relevant.

- Question 3 : Can a machine learning algorithm predict listing prices?

    I experimented with three different machine learning algorithms for this analysis: Support vector machines, AdaBoost and RandomForest.

    In the end, Random forest turned ut to be the most accurate machine learning algorithm for this task with an R2-score of 0.53, meaning that the model can explain 53% of the price. The dataset contained little information about standard besides amenities, and I belive that a substantial amount of the remaining unexplained variance of price is related to standard.

### Acknowledgements, etc.

Credit to the AirBnB dataset published by AirBnB and Kaggle for hosting it, the dataset here: https://www.kaggle.com/airbnb/seattle

Heatmap reference: https://stackoverflow.com/questions/12286607/making-heatmap-from-pandas-dataframe