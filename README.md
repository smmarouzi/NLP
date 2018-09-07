# NLP
Price prediction

In this project I am going to predict the price from different features including item_description.

table description:

Size of the DF: (118948, 8)

train_id               int64

name                  object

item_condition_id      int64

category_name         object

brand_name            object

price                float64

shipping               int64

item_description      object

dtype: object


I used NLTK library to edit the texts in a way can be used for extracting valuable words.
I used TFIDF technique (term frequency–inverse document frequency) to find the importance of words, then choosed the most important words as the features.

After finding the valuable words in item_description, and making dummie variables from other object columns, a linear regression model is trained.
category_name is splited to 3 different columns and then dummy variables is created for all of them.

Correlation between the target and features is used to find the most valuable features.
One of each two features with high correlation is removed.

At the end the result are shown...


(I had to work with a sample of 1000 rows)
(In next steps I will solve the problem of workin with the whole data)
