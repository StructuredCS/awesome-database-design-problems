# Library Lending System

The Library Lending System is a classic database design problem featured in the book [Fundamentals of Database Systems](https://www.pearson.com/en-us/subject-catalog/p/fundamentals-of-database-systems/P200000003546) by Ramez Elmasri and Shamkant B. Navathe.

This problem involves designing a relational database that tracks books, their availability, the members who borrow them, and the transactions involved in issuing and returning books. The database is supposed to model the essential operations of a library, including the cataloging of books, managing borrowers, and handling the lending and return of books.

## Entities, attributes, and relationships

- **Book**: Represents the individual books in the library collection.
    - `isbn`: International Standard Book Number (can be shared among copies).
    - `title`: Title of the book.
    - `author`: Author(s) of the book.
    - `publisher`: Publisher of the book.
    - `year`: Year of publication.
    - `category`: Genre or subject of the book.
    - `available`: Boolean or status flag indicating if the book is available for lending.

- **Member**: Represents library users who can borrow books.
    - `first name`: First name of the member.
    - `last name`: Last name of the member.
    - `address`: Mailing address.
    - `phone`: Contact number.
    - `email`: Email address.
    - `membership date`: Date the member registered.

- **Loan**: Represents a book borrowing transaction.
    - `book id`: Foreign key referencing the `Book`.
    - `member id`: Foreign key referencing the `Member`.
    - `borrow date`: Date the book was borrowed.
    - `due date`: Date the book is due for return.
    - `return date`: Date the book was actually returned (can be NULL if not yet returned).
    - `status`: Status of the loan (e.g., "borrowed", "returned", "overdue").

- **Librarian**: Staff members responsible for managing loans.
    - `name`: Name of the librarian.
    - `email`: Contact email.
    - `hire date`: Date the librarian was hired.

Beyond the entities and attributes, you have also identified the following relationships:

- A **Book** can appear in multiple **Loan** records over time.
- A **Member** can borrow multiple **Books**, tracked via the **Loan** entity (one-to-many).
- A **Loan** is always linked to one **Book** and one **Member**.
- A **Librarian** may be associated with issuing or receiving **Loans**.
- A **Book** can have multiple copies, while `isbn` is used to group identical editions.
- A **Member** can have multiple loans, but each loan is associated with a single member.

## Constraints and other information

- A book cannot be borrowed if it is already marked as unavailable.
- Due dates are typically computed based on the borrow date plus a fixed lending period (e.g., 14 days).
- The `return date` must not be earlier than the `borrow date`.
- The system may flag overdue loans automatically based on `due date` and current date.
- Members with overdue books may not be allowed to borrow new books.
- The `available` status in the `Book` table should be updated appropriately upon loan and return.
- Inventory design can be expanded to include physical location (e.g., shelf and section).
- The system should maintain a history of loans for auditing purposes, including tracking overdue books and fines if applicable.

## Solution sample

A sample design of the database for the library system using the Crow's Foot Notation will be available soon.
