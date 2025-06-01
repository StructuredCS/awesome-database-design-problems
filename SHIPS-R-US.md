# SHIPS R US

SHIPS R US is a database design problem from the book [Grokking Relational Database Design](https://mng.bz/PRER) authored by Dr. Qiang Hao and Dr. Michail Tsikerdekis, published by Manning Publications in 2025.

SHIPS R US specializes in manufacturing spaceships. SHIPS R US distributes spaceships in large batches to dealers across the galaxy, who eventually sell the spaceships to customers. A good analogy is how Toyota and Ford sell cars. Like those companies, SHIPS R US requires a web application powered by a database to manage all the relevant information, such as spaceship models, production records, and dealer and customer information. Your task is to design a database for this web application.

## Entities, attributes, and relationships

Based on the interview with the owner, managers, and staff of SHIPS R US, you have identified the following entities and attributes:

- **brand**: The brand entity represents the spaceship brands. Each brand has the following attributes:
  - `name`: The name of the brand.
  - `description`: A description of the brand. 

- **model**: The model entity represents the spaceship models. Each model has the following attributes:
  - `name`: The name of the model.
  - `model number`: A unique identifier for the model. Each model number must be unique.

- **spaceship**: The spaceship entity represents the manufactured spaceships. Each spaceship has the following attributes:
  - `serial number`: A unique identifier for the spaceship. Each serial number must be unique.
  - `recommended retail price`: The recommended retail price of the spaceship.
  - `manufacturing year`: The year when the spaceship was manufactured.

- **dealer**: The dealer entity represents the dealers who distribute spaceships. Each dealer has the following attributes:
  - `name`: The name of the dealer.
  - `email`: The email address of the dealer. Each dealer must have a unique email address.
  - `phone number`: The phone number of the dealer. Each dealer must have a unique phone number.
  - `website url`: The URL of the dealer's website.
  - `address`: The address of the dealer. An address is composed of:
    - `street address`: The street address.
    - `city`: The city of the address.
    - `suburb`: The suburb of the address.
    - `state`: The state of the address (assuming the store is based in the United States).
    - `postal code`: The zip code of the address.
    - `country name`: The country of the address.
    - `country code`: The country code of the address.

Beyond the entities and attributes, you have also identified the following relationships:

* The database needs to maintain records on all spaceship brands and models, manufactured spaceships, dealers, customers, and relationships between dealers and customers. 
* A spaceship brand is associated with multiple models, and a model is associated with multiple spacecraft. 
* One or more spaceships are distributed to a dealer, who serves one or more customers. 
* A customer is served by one or more dealers and is associated with one or more spaceships that they bought from the dealer(s.) 
* A spaceship is associated with one model and can be associated with no more than one owner and no more than one dealer.
* A customer is allowed to update their email address and phone number. 
* A customer is associated with one or more spaceships that they bought.
* A customer is served by a dealer.
* A dealer is allowed to update their email address and phone number.
* A dealer serves one or more customers.

## Solution sample

A sample design (plus implementation) of SHIPS R US can be found [here](https://github.com/Neo-Hao/grokking-relational-database-design/tree/main/chapter_08). The design and alysis of the problem is also available in the book [Grokking Relational Database Design](https://mng.bz/PRER).