# Sample Projects

## Coronavirus Data Analysis and Commentary  
This [notebook](https://www.kaggle.com/robjm16/covid-19-data-prep-and-analysis) contains extensive exploratory data analysis related to the coronavirus pandemic from a variety of sources (including Johns Hopkins University and the Centers for Disease Control).  Included are global and country-level analyses, as well as state-by-state drill downs for US data.  Also included are commentary on dealing with highly ambiguous data and an article by me entitled "Subways, Social Networks and the Coronavirus" that views New York's coronavirus situation through the lens of "small world networks" and subways as super spreaders.    


## 5-Minute ETF Stock Price Prediction  
VNQ is a popular exchange-traded fund (ETF) sponsored by Vanguard that seeks to track the value of an index comprised of real estate trusts (REITs) and other stocks related to real property (e.g., builders, property managers). This [notebook](https://github.com/robjm16/samples/blob/master/VNQ_v7_Copy1.ipynb) is designed to guide short-term investing in VNQ by seeking to predict the price of VNQ five minutes into the future based on the current and past prices of a basket of related stocks and index funds. The basket includes a portion of the ETF's underlying REITs and other stocks, interest rates and other asset classes (e.g., a gold ETF is included).
The investment thesis is that VNQ is unusually dependent on these related stocks, that the dependencies are extremely complex and that short-term pricing anomolies can be exploited.
To predict the VNQ price, a long short-term memory (LSTM) neural network is used, using sequences comprised of the VNQ stock price and approximately 20 other stock prices in five-minute intervals over five periods. Thus the inputs to the model can be described as a series of 5 x 20 matrixes that seek to predict the next price (five minutes hence) of VNQ.
The data was sourced from Yahoo Finance via its free API, which limits 5-minute backward-looking data to 60 days. After the initial 60 days were drawn, the data was continually updated on a daily basis. The model was re-trained on the most up-to-date dataset each day, with parameters reassessed on a weekly basis.
Each day, an economic ROI assessment was also conducted, to estimate how well the model performed (hypothetically) each day of the model were followed strictly.



## 10-Day Stock Price Predictions 
This [notebook](https://github.com/robjm16/samples/blob/master/Stock_Predictions_Final_Github.ipynb) generates stock price predictions for a machine learning competition sponsored by Kaggle and Two Sigma, a hedge fund that leverages artificial intelligence in its trading strategies. The aim of the competition was to use financial and news data to predict how roughly 1,800 stocks would perform relative to their benchmarks 10 days out.

Scoring was based on confidence values (0 to 1) assigned to each prediction multiplied by the actual returns against benchmarks.  There was also a Sharpe ratio-like component to the scoring, which provided a risk-adjusted final score.  

I generated dozens of features based largely on moving and exponential moving averages of financial data and news sentiment.  In the end, I used a neural network that correctly predicted the direction of 10-day-out returns about 53% of the time, not bad given the notoriously difficult task of stock price prediction (but, as mentioned above, the actual contest scoring was based on a more complicated formula).  

At the end of the first phase of the competition, based on historical data, my model ranked in the top 10% of over 2,900 teams/participants. Final standings will be based on prediction success against actual stock returns in early 2019.
Complete information about the contest can be found [here](https://www.kaggle.com/c/two-sigma-financial-news).



## 2018 NCAA Basketball Tournament Predictions
This [notebook](https://github.com/robjm16/samples/blob/master/NCAA_2018_vGF.ipynb) was developed for a Kaggle/Google Cloud competition on predicting the 2018 NCAA Men's Basketball Tournament. 

Contest participants were given historical team and game data and asked to predict every possible match-up among 68 teams in the annual basketball tournament. The contest was based on predicted probabilities, not simple win/loss accuracy.  It used log loss as its evaluation metric, harshly penalizing incorrect predictions made with high confidence.

My approach included extensive data pre-processing to combine multiple files and develop numerous features.  These included, for example, winning percentages for away/neutral site games and an end-of-season "momentum" measure, for each team as well as for their opponents.  

I explored the predictive power of six classifiers (Naive Bayes, Random Forest, lightGBM, KNN, Linear Regression and Neural Network), as well as a stacked model.  The Neural Network and Linear Regression models scored the best on my validation datasets, and I submitted predictions from both (the contest allowed two submissions, ultimately using whichever scored the highest).

In the end, based on actual results of the 2018 tournament, my predictions ranked in the top 5% of all submissions. 

Here is the [link](https://www.kaggle.com/c/mens-machine-learning-competition-2018) to the Kaggle competition, with complete details on the competition and the core datasets. 



## Safe Driver Identification 
This [notebook](https://github.com/robjm16/samples/blob/master/Safe_Driver_Prediction_vGF.ipynb) was developed for a Kaggle competition on predicting safe drivers for Brazilian insurer Porto Seguro. 

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



## Time-Series Financial Data Analysis 
This [notebook](https://github.com/robjm16/samples/blob/master/Time_Series_Financial_Data_vGF.ipynb) demonstrates time-series analysis of stock price information.  The analyis looks at how well a group of companies heavily focused on artifical intelligence (AI) performed relative to other companies in the tech-heavy NASDAQ index and the S&P 500 over the past year, in daily, quarterly and annual increments. 
