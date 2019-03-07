# Marketing-Segmentation

# Project Overview
This project was done as part of my Data Science Practicum I.  I work in the Marketing industry and thought this would be a good project to improve my skills in text mining, clustering and Python.

In marketing, customer segmentation is the process of dividing customers into groups that contain similar characteristics such as age, gender, interests and, in the case of my project, buying behaviors.

Retailers strive to use their marketing budgets efficiently by identifying customers with a higher probability to purchase a product by identifying the group or segment that best fit their marketing offers.

For this project I used online retail data https://archive.ics.uci.edu/ml/datasets/online+retail.  This data consisted of UK-based transactional data for the period between 1/12/2010 and 9/12/2011 for registered non-store online retailers.

# Data Observations

* The dataset contained 541,909 online retail transactions with 8 variables.
* The data contained multiple transactions for invoices.
* The data contained null data values for some variables.
* The data contained cancelled and bad debt transactions.

# Data Cleaning Approach

* Transactional data needs to be summarized by Customer Id when identifying customer segments.
* My approach was to remove the cancelled and bad debt transactions that did not have an associated parent transaction since that only consisted of 2% of the data.
* Most of the null values were in the Customer ID (~25%) and, with this value missing, wound not be helpful when summarizing the data for customer segmentation.

# Data Composition

After the data cleaning was complete, the data consisted of the following:

![composition of data](https://user-images.githubusercontent.com/34171862/53852261-a77e1d00-3f7e-11e9-949f-26c1ce0ca976.PNG)


# Text Mining and Cluster Analysis of Description of items purchased

Text mining the description variables consisted of the following steps:

  1. Getting a list of all the unique descriptions from the items purchased.
  2. Tokenizing the descriptions into meaningful words (nltk.word_tokenize).
  3. Utilizing SnowballStemmer to extract the base form of the extracted word (nltk.stem.SnowballStemmer("english")).
  4. Utilizeing the parts of speech on words to identify only nouns (pos_tag).
  5. Further cleaning words.
  6. Counting the number of times each words occurs
  
 
Text Mining of Top 100 Words found in the Description variable:

![top 100 words](https://user-images.githubusercontent.com/34171862/53711898-bee3cb80-3e01-11e9-900b-bc5725e6e0f6.png)

Clustering of Words in the Description variable to create product categories:

I used a silhouette analysis for selecting the number of clusters for K-means clustering.  Silhouette analysis is used to identify the seperation distance between the resulting clusters.

I settled on five clusters for product categories there was not much differentiation with the average silhouette scores after cluster five.
   
![silhouette cluster - 5 product categories](https://user-images.githubusercontent.com/34171862/53759129-d744fc00-3e7c-11e9-95c6-922de57a0b2a.PNG)

# Cluster Analysis of Customer Similarities

Clustering of Customer Segmentation to identify customer behaviors:

I used a silhouette analysis for selecting the number of clusters for K-means clustering.

I settled on eleven clusters for customer behavior categories since there was not much differentiation with the average silhouette scores after cluster eleven.

![silhouette cluster - 11 customer categories](https://user-images.githubusercontent.com/34171862/53780821-3a598180-3ec3-11e9-9887-1040dce17487.PNG)


# Modeling Analysis

The four models used to classify these clusters:
1. Support Vector Machine (SVM) - classification accuracy was 94.5.
2. Logistic Regression - classification accuracy was 89.49.
3. K-Nearest Neighbor - classification accuracy was 81.87.
4. Decision Tree - classification accuracy was 72.63.

Of the four models used, SVM model had the best accuracy at 94.5 with the Logistic Regression model following closely behind with 80.49.

Confusion matrix for the best performing model (SVM):

![svm confusion matrix](https://user-images.githubusercontent.com/34171862/53780881-902e2980-3ec3-11e9-9960-e4bf53e9dc29.png)

# Conclusions

* Overall, this cluster classification did very well.  I believe using more features such as demographic data would be helpful in further distinguishing customer buying behaviors.
* This project demonstrated many aspects that emerge in the marketing industries from the data cleansing to the modeling.



# References


<link to video >
