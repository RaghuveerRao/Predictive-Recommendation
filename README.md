# What You’ll Buy Next & When You’ll Buy It

Trend Marketplace Fall Project for Team 9

In this project, we approached a recommendation business problem as a predictive challenge and enhanced the traditional collaborative recommendation system. By this, I mean we took a recommendation system using past choices of individuals to inform future decisions and factored in time. This adjusted the traditional recommendation system from one that could be considered annoying into one that sends welcome reminders when they are wanted. We use intacart's grocery sales data for the past two years two build our model on the data set is available on Kaggle.com, more details on this at the end of this page. 

For example. Let's say I go to the grocery store and on the first week, I purchase milk, designated by the orange circle, and toothpaste, designated by the red circle. If I go to the store once a week, it is reasonable to think that I will buy milk each week, but I will be unlikely to buy toothpaste as often. Perhaps I buy toothpaste once every three weeks. The traditional recommendation system will not realize this time difference. It will recommend that I buy milk and toothpaste every time I go to the store. However, our predictive recommendation system will give a high probability to purchase toothpaste only at the times that make sense, based on my frequency of past purchases over time. For more datils on our approach please refer to our presentation and handout. 

![Recommendation differences](https://github.com/RaghuveerRao/Predictive-Recommendation/raw/master/image/recc.JPG)


### Feature Engineering
Our recommender system is different from traditional ones in the aspect of capturing time-based features. Hence, four kinds of features are taken into consideration before implementing our machine learning models: user related features, item related features, user x item related features and time-related features. Feature engineering code is available in Data Preparation.ipynb

### Architecture
![Architecture diagram](https://raw.githubusercontent.com/RaghuveerRao/Predictive-Recommendation/master/image/archi.JPG)


### AWS Spark ML implementation
Spark ML - AWS.ipynb - contains the PySpark code to read the feature engineered files process them into Spark data frame's and run Spark ML's Random Forest algorithm and predict probabilities for test data set. 

### Random Forest Algorithm
Random forest in an ensemble of decision trees, an Ensemble model is the one in which the classifier is constructed by combining several different Independent base classifiers (decision trees in this case). The ensemble classifier then aggregates the individual predictions to combine them into a final prediction. 

### Advantage of using Random forest through Spark ML on AWS's EMR clusters
An advantage of running Random forest on AWS configuration of 10 node cluster is that each of the decision trees can be trained parallelly by leveraging the distributed in-memory computing of spark across our AWS clusters. Enabling faster and cost-effective training, as we can scale down our cluster configuration once we are done with training. 

### Visualisation through Tableau
The prediction of what a specific user will buy and at what time has been visualized through Tableau dashboard (Tableau Dashboard.twb). The dashboard lets you pick UserId and time & day of the week when the user is visiting and then visualize the probability distribution of what the algorithm will recommend for that user. 

### Data files
Raw data files can be obtained from Kaggle at the following link
https://www.kaggle.com/c/instacart-market-basket-analysis/data 
