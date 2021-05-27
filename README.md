![Screen Shot 2021-05-25 at 6 14 24 PM](https://user-images.githubusercontent.com/54850909/119579921-1248e800-bd85-11eb-98dc-6b8484b6f18f.png)


## Introduction


## Data Description

Source: [Kaggle](https://www.kaggle.com/mkechinov/ecommerce-behavior-data-from-multi-category-store)

Full data contains online shopping information from October 2019 to April 2020. The data defines an 'event' as one of three shopper actions:
* **view** - a user viewed a product
* **cart** - a user added a product to their shopping cart
* **purchase** - a user purchased a product

Other variables include: the date of the event, the product id, the category id, the category code, the brand, the price, the user’s unique id, and user session id.

## Cleaning

* Used November data
* There were 3,696,117 unique user id’s
* Over 60 million events
* NA values
* Date and time
* Encode categorical variables for prediction

#### Added Variables

* Binary variable to indicate a purchase
* Day of the week the event occurred
* Separated category_code into two different columns

![Screen Shot 2021-05-25 at 6 53 21 PM](https://user-images.githubusercontent.com/54850909/119582650-8a65dc80-bd8a-11eb-81bf-16cee0e339e5.png)


## Analysis

### Events

![Screen Shot 2021-05-25 at 6 24 02 PM](https://user-images.githubusercontent.com/54850909/119580644-686a5b00-bd86-11eb-86ae-f27c070d2277.png)

* Majority of events were views
* A very small number of events were actual purchases

### Purchases
#### Most Frequently Purchased Brands and Categories

<p float="left">
  <img src="https://user-images.githubusercontent.com/54850909/119581410-1aeeed80-bd88-11eb-9a60-53ec203e8020.png"/> 
  <img src="https://user-images.githubusercontent.com/54850909/119581351-fd218880-bd87-11eb-93ee-f485940e0146.png"/>
</p>

* Of the 1.3% purchases, most products were electronics and appliances
* Top brands include several large tech companies  

## Prediction

