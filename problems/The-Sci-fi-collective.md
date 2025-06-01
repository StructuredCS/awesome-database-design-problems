# The Sci-Fi Collective

The Sci-Fi Collective is a database design problem from the book [Grokking Relational Database Design](https://mng.bz/PRER) authored by Dr. Qiang Hao and Dr. Michail Tsikerdekis, published by Manning Publications in 2025. For this problem, you will design a database for an online store that sells sci-fi products online. The online store is named "The Sci-Fi Collective" and it offers a wide range of products.

## Entities, attributes, and relationships

Based on the interview with the owner, managers, and staff of The Sci-Fi Collective, you have identified the following entities and attributes:

- **user**: The user entity represents the customers of The Sci-Fi Collective. Each user has the following attributes:
  - `username`: The username of the user.
  - `email`: The email address of the user. Each user must have a unique email address.
  - `password`: The password for the user's account.
  - `first name`: The first name of the user.
  - `last name`: The last name of the user.
  - `address`: The address of the user. An address is composed of:
    - `street address`: The street address.
    - `city`: The city of the address.
    - `state`: The state of the address (assuming the store is based in the United States).
    - `postal code`: The zip code of the address.
  - `phone number`: The phone number of the user.
  - `last login time`: The time when the user last logged in to their account.

- **product**: The product entity represents the products sold by The Sci-Fi Collective. Each product has the following attributes:
  - `name`: The name of the product.
  - `code`: A Universal Product Code (UPC) for the product, which must be unique.
  - `description`: A description of the product.
  - `manufacturer`: The manufacturer of the product.
  - `photo`: A URL to an image of the product.
  - `price`: The price of the product.
  - `cost`: The cost of the product to The Sci-Fi Collective.
  - `inventory quantity`: The quantity of the product in stock.

- **order**: The order entity represents the orders placed by users. Each order has the following attributes:
  - `total price`: The total price of the order.
  - `product price`: Itemized price of each product in the order.
  - `product quantity`: The quantity of each product in the order.
  - `date and time`: The time when the order was placed.

- **review**: The review entity represents the reviews left by users for products. Each review has the following attributes:
  - `review text`: The text of the review left by the user.
  - `date and time`: The time when the review was left.

- **payment method**: The payment method entity represents the payment methods used by users to pay for their orders. Each payment method has the following attributes:
  - `name`: The name of the payment method; the name is given by the user (e.g., "Visa", "Master"). 
  - `credit card number`: The details of the payment method (e.g., credit card number, PayPal account).
  - `expiration date`: The expiration date of the payment method.
  - `address`: The address associated with the payment method. This address is composed of:
    - `street address`: The street address.
    - `city`: The city of the address.
    - `state`: The state of the address (assuming the store is based in the United States).
    - `postal code`: The zip code of the address.


Beyond the entities and attributes, you have also identified the following relationships:

* A user can make multiple orders. An order can be made by only one user. 
* A user can review multiple products. A product can be reviewed by multiple users. 
* A user can maintain multiple payment methods. A payment method can be associated with only one user. 
* An order can have more than one product. A product can show up in multiple orders.
* An order is associated with one payment method. A payment method can be used for multiple orders.

## Constraints and other information

* A phone number is not required for a user to create an account.
* A username is unique for each user.
* When a user has a phone number, the phone number must be unique.
* The combination of product name and manufacturer must be unique for each product.
* There are 50 states plus the District of Columbia in the United States.
* The postal code in The United States is a five-digit number.
* A user can have only one delivery address, but mulitple users may share the same delivery address.
* A payment method is associated with a single address, but multiple payment methods can share the same address.
* The delivery address of a user is not required to be the same as the address associated with the payment method.
* The Sci-Fi Collective should not store sensitive information such as credit card numbers in plain text.
* The Sci-Fi Collective sells products to users in the United States only, and users may live in different time zones.

## Solution sample

A sample design (plus implementation) of The Sci-Fi Collective can be found [here](https://github.com/Neo-Hao/grokking-relational-database-design/tree/main/chapter_07). The design and alysis of the problem is also available in the book [Grokking Relational Database Design](https://mng.bz/PRER).