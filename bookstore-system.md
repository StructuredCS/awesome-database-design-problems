# Bookstore Inventory System  

The Bookstore Inventory System is a database design problem featured in the book [Database System Concepts](https://db-book.com/) authored by Abraham Silberschatz, Henry Korth, and S. Sudarshan, published by McGraw-Hill Education. This problem is often used in database courses to teach schema design, entity-relationship modeling, normalization, and SQL query formulation.

This problem involves designing a schema to manage the inventory of a bookstore. The database tracks books, their authors and publishers, current stock levels, and sales transactions.

## Entities, attributes, and relationships

- **Book**: Represents each book available in the store’s catalog.
    - `ISBN`: A unique identifier for the book.
    - `title`: The title of the book.
    - `year`: The year the book was published.
    - `price`: The price of the book.
    - `category`: The genre or category of the book (e.g., Fiction, Science).
    - `publisher name`: The name of the publisher (foreign key).

- **Publisher**: Represents the publishing companies.
    - `name`: The name of the publisher (primary key).
    - `address`: The mailing address of the publisher.
    - `phone`: The contact number of the publisher.

- **Author**: Represents individuals who have written books.
    - `name`: The full name of the author.
    - `email`: The email address of the author.

- **Customer**: Represents customers who purchase books.
    - `customer ID`: A unique identifier for each customer.
    - `name`: The name of the customer.
    - `email`: The email address of the customer.

- **Sale**: Represents a sales transaction.
    - `date`: The date of the purchase.

- **Sale Item**: Represents individual book items sold in each sale.
    - `ISBN`: A unique identifier for the book.
    - `quantity`: The number of copies sold.

- **Inventory**: Represents stock levels for each book.
    - `ISBN`: A unique identifier for the book.
    - `quantity in stock`: The current quantity available in the store.

Beyond the entities and attributes, you have also identified the following relationships:

- A **Book** is published by a **Publisher**.
- A **Book** can be written by multiple **Authors**, and an **Author** can write multiple **Books**.
- A **Customer** can be involved in multiple **Sales** of books.
- Each **Sale** can include multiple **Books**, and a **Book** can appear in multiple **Sales**.
- Each **Sale** consists of multiple **Sale Items**, where each item corresponds to a specific **Book**.
- **Inventory** maintains the stock count of each **Book**.

## Constraints and other information

- Each book must have at least one author.
- A sale must have at least one associated sale item.
- Inventory levels should be updated after each sale to reflect remaining stock.
- Book price must be a non-negative decimal.
- Inventory quantities cannot be negative.
- A book’s ISBN must be unique.
- Publisher names are assumed to be unique.
- Each book has an associated inventory record to track stock levels.


## Solution sample

A sample design of the database for the bookstore inventory system from the book [Database System Concepts](https://db-book.com/) can be found [here](samples/bookstore-system-sample.png). The sample adopts the Chen's Notation. Another sample design using the Crow's Foot Notation will be available soon.
