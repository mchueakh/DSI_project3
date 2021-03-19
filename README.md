# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Project 3 - Classification Model in Reddit posts -


## Objectives:
- Find is the best model that can classifiy between the booksuggestion and basketball posts.
- Find a list of main key words which are can identify the post is booksuggestion or basketball post

### Data Source

- the two sub-reddit post are https://www.reddit.com/r/Basketball/ and https://www.reddit.com/r/booksuggestions/

## The Workflow Process

### 0. Define problem
- Find is the best model that can classifiy between the booksuggestion and basketball posts.
- Find a list of main key words which are can identify the post is booksuggestion or basketball post

### 1. Data Preparation
- the two sub-reddit post are https://www.reddit.com/r/Basketball/ and https://www.reddit.com/r/booksuggestions/
- run reddit-api_P3.ipynb to get Basketball_posts.csv and booksuggestions_posts.csv
- load two files in pandas Dataframes

### 2. EDA 
- calulate the number of charactor in each posts (book & basketball)
- plot histogram for the number of charactor in each posts (book & basketball)
- plot Proportion of part of speech in posts (book & basketball)
- combine two dataframes (book & basketball) to single df_posts_train dataframe
- set target = 1 in book posts and target = 0 in basketball posts

### 3. Data preprocessing (text in the posts)
- Split data to X,y Train and Test
- Step 1. Remove non-letters. (such number, #!/()[]&$~`+= )
- Step 2. Convert to lower case.
- Step 3. Remove stopwords. (such as a, an, the, in, on, at, has, have)
- Step 4. Lemmatization, grouping words. (such as “cats” and “cat”)


### 4. Bernoulli Naive Bayes Model
- GridSearch & Pipeline to select the best estimator
- Run the model by using the best estimator
- Evaluate the model

### 5. Logistic Regression Model
- GridSearch & Pipeline to select the best estimator
- Run the model by using the best estimator
- Evaluate the model

### 6. Voting Classifier Model
- Classify by using 5 model to vote the final target
- 1. LogisticRegression()
- 2. BernoulliNB()
- 3. DecisionTreeClassifier()
- 4. AdaBoostClassifier()
- 5. GradientBoostingClassifier()
- Evaluate the model




## Conclusion 

The Bernoulli Naive Bayes model is best performance and good perform in unseen and testing data when compare with Logistic Regression Model which is slightly over fit with the training data.

### Here are the list of main keyword which can use to identify the booksuggestion post 
- read
- like
- looking
- would
- suggestion
- good
- love
- really
- something
- novel
- reading
- similar
- recommendation
- life

### Here are the list of main keyword which can use to identify the Basketball post 
- basketball
- Play
- team
- game
- ball
- kg
- nba
- player
- poll
- shot
- aau
- able dunk
- able jump 
- able play 
- access 
- adidas 
- advantage
- aggressive
- airball 
- anger
