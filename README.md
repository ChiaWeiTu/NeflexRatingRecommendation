# NeflexRatingRecommendation
Netflix Rating Recommendation Analysis-Python

     Introduction and discovery 

•	Background

 Netflix canceled user film review system and use artificial intelligence algorithms to recommend movies in these years. For getting more viewers, Netflix try to obtain viewer’s flavor of movie and recommend more feature of movie which match with user’s taste. Also, use the most popular result for increasing Netflix’s movie variety. 

•	Problem  

Does the rating score really indicate how well Netflix system feel the recommended content fits the specific user? Does the recommendation score really help user find their love shows and movies?

•	Developing initial hypotheses 

If the Netflix rating recommendation is higher than scores 80, The result is yes (highly recommend).
If the Netflix rating recommendation is lower than scores 80, The result is No (not recommend).


  Data Preparation 

The Dataset is form Data World  https://data.world/chasewillden/netflix-shows
 
The dataset is about Netflix each title (movie name)'s rating information, including the rating category for different ages(rating), the description of rating, the release year, user rating size (only more than 80 sizes can be record on the user score standard) and the rating score. 



    Model Planning and Implementation 
#!pip install yellowbrick
# import yellowbrick library
from yellowbrick.cluster import KElbowVisualizer

The original data have overlapping the same ages but different TV rating names, it can be categorized to 5 different age levels. And the user rating score is from the lowest score 55 to highest score 99 excluding the 0 (unrated movie). So, I planned to divide the score to two results-Not Recommend and Highly Recommend. Over 80 are yes for recommend, others are no for recommend. For the Not Recommend and Highly Recommend target, it can change it to the binary category.
 Base on the data transform, I create two series of machine learning pipeline. One is for the clustering analysis which can find the related group in different rating.
The clustering can be analyzed into more detail in each rating group. For example, the teenager can be divided by 7 classes (k=7). So, this can observe the relationship between each specific user’s reaction and in different flavor of movies (like release year).

Second is for Logistic regression and classifications algorithms to make predictions for the recommend result. Logistic regression is mostly used to solve binary classification. 
 After through the classification pipeline model, it can use the best model to predict the release year, different user group or rating description whether will have a good effect on the result of recommendation.

I use list to store every machine learning models and best parameter. And then zip all the list into for loop to use GridSearchCV finding the optimal parameter and pipeline predicting the X test and then append to the result list.



   Concluding Remarks 

As the number of people subscribing and watching Netflix grew, the task became a big data project. Netflix rating recommendation system can help viewers by choosing among numerous options available to them through the streaming service. It also can filter the program rated group and remove unnecessary information from the data stream before it reaches to them. 
Moreover, through the highly recommendation system, it can increase the viewer’s trust of selecting the films from recommendation which they like a lot and then giving a nice feedback.
If Netflix rating recommendation system obtain more updated and enough size of data, it seems to be a ideally cycle between user and business strategy. 





