# Database Schema
![Tux, the Linux mascot](https://github.com/tOxicV4p0r/database/blob/main/diagram.png?raw=true)

## Customer Table

| Column Name     | Description                                             |
|-----------------|---------------------------------------------------------|
| customer_id     | Unique identifier for each customer                     |
| date_of_birth   | Date of birth of the customer                           |
| gender          | Gender of the customer                                  |
| location        | Location (e.g., city, country) of the customer          |
| first_name      | First name of the customer                              |
| last_name       | Last name of the customer                               |
| created_at      | Timestamp indicating when the customer record was created |

---

## Product Category Table

| Column Name   | Description                                      |
|---------------|--------------------------------------------------|
| category_id   | Unique identifier for each product category       |
| name          | Name of the product category (e.g., Electronics, Clothing) |

---

## Product Table

| Column Name   | Description                                                        |
|---------------|--------------------------------------------------------------------|
| product_id    | Unique identifier for each product                                 |
| category_id   | Foreign key referencing the Product Category table                 |
| name          | Name of the product                                                |
| color         | Color of the product                                               |
| size          | Size of the product (if applicable)                                |
| description   | Description of the product                                         |
| price         | Price of the product                                               |
| created_at    | Timestamp indicating when the product was created                  |

---

## Cart Table

| Column Name   | Description                                      |
|---------------|--------------------------------------------------|
| cart_id       | Unique identifier for each cart                  |
| customer_id   | Foreign key referencing the Customer table       |
| date          | Date when the cart was created                   |
| status        | Status of the cart (e.g., open, checked out)      |

---

## Cart Item Table

| Column Name   | Description                                      |
|---------------|--------------------------------------------------|
| product_id    | Foreign key referencing the Product table        |
| cart_id       | Foreign key referencing the Cart table           |
| quantity      | Quantity of the product added to the cart        |
"""