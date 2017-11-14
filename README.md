# Sample Work



## Safe Driver Identification 
This [notebook](https://github.com/robjm16/samples/blob/master/Safe_Driver_Prediction_GF.ipynb) was developed for a Kaggle competition on predicting safe drivers for a Brazilian insurance company named Porto Seguro. 

The notebook includes extensive data exploration and preprocessing, including the use of predictive models to interpolate key missing values. 

LightGBM is the primary model used, with several rounds of parameter tuning.  In addition, the notebook shows model stacking and prediction averaging using various base models (e.g., KNN, Random Forests).  

Here is the [link](https://www.kaggle.com/c/zillow-prize-1#description) to the Kaggle competition, with complete details on the competition and the core datasets.                        



## Zillow Home Value Estimates 
This [notebook](https://github.com/robjm16/samples/blob/master/Zillow_Competition_vGF.ipynb) was developed for a Kaggle competition related to Zillow's estimates of home values.  

In the first phase of the competition (submissions were due Oct 16, 2017), the aim was to predict the residual error in Zillow's home value estimates based on a subset of real estate transactions in California in 2016 and 2017.  Please note that residual errors -- not the home values themselves -- were being predicted.  

Only the datasets provided by Zillow could be used in the first round (i.e., no supplemental data could be incorporated).   A second phase, allowing for the use of outside data and aimed at building a better model for predicting actual home values, will take place in 2018.   

Here is the [link](https://www.kaggle.com/c/zillow-prize-1#description) to the Kaggle competition, with complete details on the competition and the core datasets.                         



## Instacart Repeat Grocery Purchases  
This [notebook](https://github.com/robjm16/samples/blob/master/Instacart_Competition_vGF.ipynb) was developed for a Kaggle competition on predicting repeat product purchases on Instacart, an online grocery ordering site.

The datasets included information on 3.4M orders and 49.7K unique products. The orders were further broken down into “prior”, “train” and “test” sets. The prior orders covered the five (or more, as available) most recent orders leading up to the final order in the dataset. The train set covered the final order. The test set included user IDs and a few temporal attributes for the final order (but not the ordered products, which is what we were predicting).

I first conducted exploratory data analysis(EDA), using code posted by other Kaggle competitors as well as my own code. I engineered additional features based on products (e.g., how often the item was reordered), users (e.g., how many items he/she typically ordered) and product/user combination characteristics (e.g., how often a user bought a specific product). I then added those features to the train dataset, and in turn used the trained classifier on the test dataset.

I tested a variety of classifiers and regression models, ultimately using a Random Forest classifier for my final submission.  

Here is the [link](https://www.kaggle.com/c/instacart-market-basket-analysis) to details on the Instacart competition, including core datasets.                                         



## Twitter Sentiment Analysis
This [notebook](https://github.com/robjm16/samples/blob/master/Tweet_Analysis_vGF.ipynb) demonstrates sentiment analysis and topic modeling on a selection of tweets from Twitter. The tweets were pulled on October 16, 2017, via the Twitter API, using the search term "Tesla" (the car company). The tweets were tokenized, evaluated for positive/negative sentiment and broken down by topics and further analyzed (e.g., for hashtags).


