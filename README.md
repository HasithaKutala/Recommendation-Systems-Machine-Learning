# Recommendation-Systems-Machine-Learning

There are two types of recommendation systems they are: Content-based filtering, based on the content of movies like action, and comedy and Collaborative filtering  here we check user behaviour and recommend based on their behaviour ex: Netflix.  

1. Weighted hybrid technique for Recommender system

<img width="423" alt="Screenshot 2024-03-19 at 22 44 36" src="https://github.com/HasithaKutala/Recommendation-Systems-Machine-Learning/assets/118222826/0e5bcd06-4902-4b51-be9d-79d4f5502b07">

2. Nearest Neighbours 

Using the corrwith() method, you calculated the pairwise correlation of user ratings for "Star Wars (1977)" and "Liar Liar (1997)" against all other movies in the dataset this method computes the Pearson correlation coefficient, which measures the linear correlation between two variables, giving a value between -1 and 1. A value close to 1 implies a strong positive correlation, meaning if a user likes "Star Wars", they are likely to like the movie it's being compared with (and vice versa). A value close to -1 indicates a strong negative correlation and a value around 0 implies no linear correlation.
You then converted the series of correlations into a DataFrame and dropped any rows with NaN values to clean up the data. When you sort corr_starwars by the 'Correlation' column in descending order, theoretically, you should see the movies most similar to "Star Wars (1977)" based on user ratings. 

common issues:

High leverage of outliers: If a movie was rated by only one user, and that user also rated "Star Wars" highly, the correlation between that movie and "Star Wars" could appear unjustifiably high.
Lack of robustness: Correlations based on small sample sizes (few ratings) are not statistically robust and can lead to misleading conclusions.
Improving the Recommendation
To mitigate this issue and improve the quality of your recommendations, you can set a threshold for the minimum number of ratings that a movie must have to be considered in your similarity calculations
