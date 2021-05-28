![Screen Shot 2021-05-25 at 6 14 24 PM](https://user-images.githubusercontent.com/54850909/119579921-1248e800-bd85-11eb-98dc-6b8484b6f18f.png)


## Introduction

Retail e-commerce has seen rapid growth for many years now, evolving from its beginning in the 1990s and becoming a major component of many businesses. More recently, e-commerce has increased significantly due to the coronavirus pandemic. As people began staying home for long periods of time, many started to rely heavily on online shopping. With the increase in demand for online retail, many businesses have moved their inventory to the internet in order to stay open. In short, e-commerce is probably more important now than ever before, for both consumers and retailers. By analyzing e-commerce data, I hope to gain some experience dealing with real questions that data analysts working in the industry are facing regarding consumer behavior. For example:

* How many customers visited the site in a certain time period?
* What kind of activity went on during that time (viewing, buying, etc.)?
* What products are most frequently purchased?
* What might be some factors that contribute to purchases?

## Data Description

Source: [Kaggle](https://www.kaggle.com/mkechinov/ecommerce-behavior-data-from-multi-category-store)

Full data contains online shopping information from October 2019 to April 2020. For my analysis, I used the November data. The data defines an 'event' as one of three shopper actions:
* **view** - a user viewed a product
* **cart** - a user added a product to their shopping cart
* **purchase** - a user purchased a product

Other variables include: the date of the event, the product id, the category id, the category code, the brand, the price, the user’s unique id, and user session id.

![Screen Shot 2021-05-28 at 1 46 56 PM](https://user-images.githubusercontent.com/54850909/120029064-33931980-bfbb-11eb-94c3-1d7248d1684d.png)


## Exploratory Analysis

### Shoppers
![Screen Shot 2021-05-28 at 1 42 13 PM](https://user-images.githubusercontent.com/54850909/120028946-06df0200-bfbb-11eb-930b-6fc56b355666.png)

* There were 3,696,117 unique user id’s
* Over 67 million events
* NA values
* Date and time
* Encode categorical variables for prediction

![Screen Shot 2021-05-28 at 2 22 00 PM](https://user-images.githubusercontent.com/54850909/120032693-2d536c00-bfc0-11eb-9c09-cf4f4b0914ba.png)

![image](https://user-images.githubusercontent.com/54850909/120032716-36443d80-bfc0-11eb-8b72-f93e4d8c7dea.png)


### Events
![Screen Shot 2021-05-28 at 2 11 56 PM](https://user-images.githubusercontent.com/54850909/120031684-bcf81b00-bfbe-11eb-9708-d6164b888566.png)


![Screen Shot 2021-05-25 at 6 24 02 PM](https://user-images.githubusercontent.com/54850909/119580644-686a5b00-bd86-11eb-86ae-f27c070d2277.png)

* Majority of events were views
* A very small number of events were actual purchases


### Purchases
#### Added Variables

* Binary variable to indicate a purchase
* Day of the week the event occurred
* Separated category_code into two different columns

![Screen Shot 2021-05-25 at 6 53 21 PM](https://user-images.githubusercontent.com/54850909/119582650-8a65dc80-bd8a-11eb-81bf-16cee0e339e5.png)

#### Most Frequently Purchased Brands and Categories

<p float="left">
  <img src="https://user-images.githubusercontent.com/54850909/119581410-1aeeed80-bd88-11eb-9a60-53ec203e8020.png"/> 
  <img src="https://user-images.githubusercontent.com/54850909/119581351-fd218880-bd87-11eb-93ee-f485940e0146.png"/>
</p>

* Of the 1.3% purchases, most products were electronics and appliances
* Top brands include several large tech companies  

## Prediction

