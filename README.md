In this project I'm analyzing a dataset, that contains different videos and trying to make predictictions whether video will get any likes based on different criterias. I think nowadays with popularity of such platforms as YouTube, Instagram and others, relevance of video could be really important and exploring effect of different factors on number of likes could give better picture for content creators, sponsors and statistic in general.

My Project contains data cleaning and analyzing, visualizations of different aspects of data and using machine learning models to see which one is doing better predictions. 

Data Dictionary for this dataset:

![image](https://user-images.githubusercontent.com/66798944/144357382-6af14450-0988-4b94-8dfa-6ee8b21caf6c.png)

First, let’s take a look on our target. We can see, that there’s a bigger amount of videos with no likes comparing to the ones, that  have any likes, therefore I’m going to group Number of likes into 0 likes and the ones with any likes all together:

![image](https://user-images.githubusercontent.com/66798944/144357515-ca562a71-eeca-4810-8cdb-b5014c686462.png)


Next, I’m showing how video time posting could affect number of likes. Based on this visualization, we see that video has more chances on getting 0 likes at 1 am and between 5 & 7 pm. The highest amount of likes video gets between 3 and 4 pm.

![image](https://user-images.githubusercontent.com/66798944/144357571-176a42f3-4520-48c6-8784-02b6a6b2876e.png)

Then I am looking on Day of week affection on Likes. Based on this heatmap, videos have more chances on receiving 0 likes on 1st day of the week (Sunday) and 6th day (Friday), however there's high chance on getting likes on 6th day as well.

![image](https://user-images.githubusercontent.com/66798944/144357647-327492da-1963-45c7-a4ad-4a11c3e6cb20.png)

Then I am binarizing other column in my data set, so I can see correlations between all the values. This heatmap shows that number of tags and day of the week has the most impact on number of likes.

![image](https://user-images.githubusercontent.com/66798944/144357733-211cd0c5-9ab0-40ea-b5ec-9dbcd26b0fe1.png)

My target is a classification problem, so I’ve used couple classification models, such as LogisticRegression, KNeighborsClassifier, BaggingClassifier and RandomForestClassifier. 
I tried hypertune some parameters. Based on models scores, I would say Logistic Regression is the best option, since scores are pretty good and overfitting is minimal. Also it can be used with default parameters, because tyning didn’t really change the score, so we can use less steps in evaluating this model. Below there are the accuracy results:


Training accuracy: 93.3%
Test accuracy: 93.5%


So based on my observations, in order to receive bigger amount of likes, video should be posted between 3 and 4 pm on Friday. Looks like videos less than 9 minutes have higher chances on getting likes and amount of tags should be less than 10. 








