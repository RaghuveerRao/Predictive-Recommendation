# What You’ll Buy Next & When You’ll Buy It

Trend Marketplace Fall Project for Team 9

### AWS Spark ML implementation
Spark ML - AWS.ipynb - contains the PySpark code to read the feature engineered files process them into Spark data frame's and run Spark ML's Random Forest algorithm and predict probabilities for test data set. 

### Visualisation through Tableu
The prediction of what a specific user will buy and at what time has been visualized through Tableau dashboard (Tableau Dashboard.twb). The dashboard let's you pick UserId and time & day of the week when the user is visiting and then visualize the probability distribution of what the algorithm will recommend for that user. 


### Random Forest Algorithm
Random forest in an ensemble of decision trees, an Ensemble model is the one in which the classifier is constructed by combining several different Independent base classifiers (decision trees in this case). The ensemble classifier then aggregates the individual predictions to combine them into a final prediction. 

### Advantage of using Random forest through Spark ML on AWS's EMR clusters
Advantage of running Random forest on AWS configuration of 10 node cluster is that, each of the decision tree can be trained parallelly by leveraging the distributed in-memory computing of spark across our AWS clusters. Enabling faster and cost effective training, as we can scale down our cluster configuration once we are done with training. 

### Raw data files
Raw data files can be obtained from Kaggle at the following link
https://www.kaggle.com/c/instacart-market-basket-analysis/data 
