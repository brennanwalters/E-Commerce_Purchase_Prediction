![Screen Shot 2021-07-02 at 4 04 48 PM](https://user-images.githubusercontent.com/54850909/124328448-43b88e80-db4f-11eb-8302-88b0cd298b35.png)


# Table of Contents
* Introduction
* Data Description
* Analysis Results
* Logistic Regression
* Model Evaluation
* Conclusion

# Introduction

Retail e-commerce has seen rapid growth for many years now, evolving from its beginning in the 1990s and becoming a major component of many businesses. More recently, e-commerce has increased significantly as many more people rely heavily on online shopping. With the increase in demand for online retail, many businesses have moved their inventory to the internet in order to stay open. In short, e-commerce is probably more important now than ever before, for both consumers and retailers. By analyzing e-commerce data, I hope to gain some experience dealing with real questions that data analysts working in the industry are facing regarding consumer behavior. For example:

* How many customers visited the site in a certain time period?
* What kind of activity went on during that time (viewing, buying, etc.)?
* What products are most frequently purchased?
* What might be some factors that contribute to purchases?

# Data Description

Source: [Kaggle](https://www.kaggle.com/mkechinov/ecommerce-behavior-data-from-multi-category-store)

The full data contains online shopping information from October 2019 to April 2020. For my analysis, I used the November 2019 data. The data defines an 'event' as one of three shopper actions:
* **view** - a user viewed a product
* **cart** - a user added a product to their shopping cart
* **purchase** - a user purchased a product

The data contains over 67 million events. Other variables include: the date of the event, the product id, the category id, the category code, the brand, the price, the user’s unique id, and user session id.

![Screen Shot 2021-05-28 at 1 46 56 PM](https://user-images.githubusercontent.com/54850909/120029064-33931980-bfbb-11eb-94c3-1d7248d1684d.png)

# Analysis Results

## Shoppers
### Number of Unique Shopper IDs
![Screen Shot 2021-05-28 at 1 42 13 PM](https://user-images.githubusercontent.com/54850909/120028946-06df0200-bfbb-11eb-930b-6fc56b355666.png)

### Number of Shoppers Over Time
![image](https://user-images.githubusercontent.com/54850909/120032716-36443d80-bfc0-11eb-8b72-f93e4d8c7dea.png)

* There were 3,696,117 shoppers on the site during November
* Activity increased dramatically towards the middle of the month and then decreased

## Events
![Screen Shot 2021-05-28 at 2 11 56 PM](https://user-images.githubusercontent.com/54850909/120031684-bcf81b00-bfbe-11eb-9708-d6164b888566.png)


![Screen Shot 2021-05-25 at 6 24 02 PM](https://user-images.githubusercontent.com/54850909/119580644-686a5b00-bd86-11eb-86ae-f27c070d2277.png)

* The majority of events were views. There were also more views than shoppers, implying that customers viwed multiple items
* There were fewer purchases than items added to shopping carts
* A very small number of events were actual purchases


## Purchases
### Added Variables

* Binary variable to indicate a purchase
* Day of the week the event occurred
* Separated category_code into two different columns

![Screen Shot 2021-05-25 at 6 53 21 PM](https://user-images.githubusercontent.com/54850909/119582650-8a65dc80-bd8a-11eb-81bf-16cee0e339e5.png)

### Most Frequently Purchased Brands and Categories

<p float="left">
  <img src="https://user-images.githubusercontent.com/54850909/119581410-1aeeed80-bd88-11eb-9a60-53ec203e8020.png"/> 
  <img src="https://user-images.githubusercontent.com/54850909/119581351-fd218880-bd87-11eb-93ee-f485940e0146.png"/>
</p>

* Of the 1.3% purchases, most products were electronics and appliances
* Top brands include several large tech companies  

# Logistic Regression
![image](https://user-images.githubusercontent.com/54850909/120051669-2855e300-bfe7-11eb-96a4-cef641b0a43f.png)

![image](https://user-images.githubusercontent.com/54850909/120051678-2ee45a80-bfe7-11eb-9f54-6322feebd114.png)

# Model Evaluation

#### Confusion Matrix

![image](https://user-images.githubusercontent.com/54850909/126216203-eedd8b92-6c77-4283-aa48-2917f5ee2c61.png)

 Accuracy: 0.63 \
 Precision: 6.87e-05 \
 Recall: 0.24 
 
 The huge difference in true positives and true negatives is due to the fact that an overwhelming majority of events were not purchases and therefore the data is imbalanced. In order for this model to be useful, some adjustments should be made to the data. As this is e-commerce data, it is feasible to collect more data which could help to balance the classes. A likely better solution would be to resample the data using random oversampling (randomly duplicate examples in the minority class) or random undersampling (Randomly delete examples in the majority class). 
 

# Conclusion
* E-commerce plays a massive part in retail sales
* Of the thousands of people who browse e-commerce sites everyday, most tend to view multiple products
* A very small proportion of activity on e-commerce sights is purchasing, making the modeling process less straightforward
* On this site in particular, most purchases were electronics and appliances

