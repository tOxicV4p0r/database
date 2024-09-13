# Database Schema
![Tux, the Linux mascot](https://github.com/tOxicV4p0r/database/blob/main/diagram.png?raw=true)

## Customer Table

| Column Name     | Description                                             |
|-----------------|---------------------------------------------------------|
| customer_id     | Unique identifier                 |
| date_of_birth   |                           |
| gender          |                                  |
| location        | Location (e.g., city, country)          |
| first_name      |                           |
| last_name       |                            |
| created_at      | Timestamp record was created |

---

## Product Category Table

| Column Name   | Description                                      |
|---------------|--------------------------------------------------|
| category_id   | Unique identifier       |
| name          | Name of the product category |

---

## Product Table

| Column Name   | Description                                                        |
|---------------|--------------------------------------------------------------------|
| product_id    | Unique identifier                                |
| category_id   | Foreign key referencing the Product Category table                 |
| name          |                                                |
| color         |                                             |
| size          |                           |
| description   |                                      |
| price         |                                                |
| created_at    | Timestamp record was created                  |

---

## Cart Table

| Column Name   | Description                                      |
|---------------|--------------------------------------------------|
| cart_id       | Unique identifier                 |
| customer_id   | Foreign key referencing the Customer table       |
| date          | Date when the cart was created                   |
| status        | open, checked out    |

---

## Cart Item Table

| Column Name   | Description                                      |
|---------------|--------------------------------------------------|
| product_id    | Foreign key referencing the Product table        |
| cart_id       | Foreign key referencing the Cart table           |
| quantity      |      |

