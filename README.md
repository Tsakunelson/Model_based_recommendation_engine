# Model_based_recommendation_engine
Model_based Recommendation Engine
## Installation
- Anaconda 4.5.11 distribution 
- Python 3.6 
- Numpy and Pandas
- Matplotlib
- Scipy

## Project Motivation
In this notebook, we implement a model based recommendation engine to address two major issues faced by most recommendation systems: 
- The cold start problem
- Providing an offline testing environment, to prevent customer churn.

Funk Singular Value Decomposition is adopted as matrix factorization model, to which a content and knowledge based recommendation strategy is adopted. Consider a user-item matrix that looks like the folowing matrix, to which we want to update both U and V matrices based on the 4 highlighted.

![User-movier ratings](./Figure5.png)

We also have the following U (left) and V (right) matrices:

![U and V matrices](./Figure6.png)

To identify what the current prediction would be for the rating 4 (highlighted in the first image above) based on the current values in the U and V matrices, we perform a linear combination of the corrsponding row and column, resulting to -1.8. This is quite far from the expected rating value, and would produce a large error with respect to the original value. With the help of gradient descent and a loss function, we would be able to make accurate predictions for values in the U and V matrices. These results would enable acurate rating predictions for missing values, hence a solution to test our model in an ofline setting, to prevent client churn.  

## File Descrition 
This repository consists of:
- Cleaned movies dataset (movies_clean.svs)
- Cleaned reviews dataset (reviews_clean.svs)

## Authors, Licensing, Acknowledgements
- Nelson Zange Tsaku 
- Licensing Code and documentation copyright 2018 the Author's Code released under Udacity License 
- Thanks to the Udacity Community for related support
