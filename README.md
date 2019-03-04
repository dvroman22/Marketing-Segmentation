# Marketing-Segmentation
Marketing Cluster Segmentation

# Project Overview
This project was done as part of my Data Science Practicum I.  I currently work in a Marketing industry and thought this would be a good project to improve my skills in text mining, clustering and Python.

In many industries specifically marketing, customer segmentation is the process of dividing customers into groups that contain similar characteristics such as age, gender, interests and, in the case of my project, buying behaviors.

Retailers strive to use their marketing budgets efficiently and want to identify customers with a higher probability to purchase a product by identifying the group or segment that best fit their marketing offers.

For this project I used online retail data https://archive.ics.uci.edu/ml/datasets/online+retail.  This data consists of UK-based transactional data for the period between 1/12/2010 and 9/12/2011 for registered non-store online retailers.

# Data Observations

* The dataset contains 541,909 online retail transactions with 8 variables.
* There are multiple transactions for invoices
* There are null data values for some variables
* There are cancelled and bad debt transactions since there contains negative quanties and unit prices

# Data Cleaning Approach

* The transactional data will need to be summarized by Customer Id when identifying customer segments.
* My approach was to remove the cancelled and bad debt transactions that did not have a associated parent transaction since that only consisted of 2% of the data.
* Most of the null values were in the Customer ID (~25%) and with this value missing this won't be helpful when summarizing the data for customer segmentation.
# Text Mining and Cluster Analysis of Description of items purchased94.5

Text Mining of Top 100 Words found in the Description variable:

![alt text](https://github.com/adam-p/markdown-here/raw/master/src/common/images/icon48.png "Logo Title Text 1")

Clustering of Words in the Description variable to create product categories:

![alt text](https://github.com/adam-p/markdown-here/raw/master/src/common/images/icon48.png "Logo Title Text 1")

# Cluster Analysis of Customer Similarities

Clustering of Customer Segmentation to identify customer behaviors:

![alt text](https://github.com/adam-p/markdown-here/raw/master/src/common/images/icon48.png "Logo Title Text 1")


# Modeling Analysis

The four models used to classify this clusters:
1. Support Vector Machine (SVM)
2. Logistic Regression
3. K-Nearest Neighbor
4. Decision Tree

The best performing model was the Support Vector Machine with a classification accuracy of 94.5.

![alt text](https://github.com/adam-p/markdown-here/raw/master/src/common/images/icon48.png "Logo Title Text 1")

# Conclusions

* Overall, this cluster classificaton was good.  I believe using more features such as demographic data would be more helpful in furthing identifying customer buying behaviors.
* This project demonstrated many aspects that emerge in the marketing industries from the data cleansing to the modeling.



# References

<link to video >
