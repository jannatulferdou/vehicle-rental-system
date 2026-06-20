# Vehicle Rental System - Database Design & SQL Queries

## Project Overview

The Vehicle Rental System is a database project designed to manage vehicle rental operations. The system stores information about users, vehicles, and bookings. It demonstrates the use of relational database concepts such as Primary Keys, Foreign Keys, relationships, and SQL queries.

## Objectives

* Design an Entity Relationship Diagram (ERD)
* Implement relational database tables
* Understand Primary Key and Foreign Key concepts
* Write SQL queries using JOIN, EXISTS, WHERE, GROUP BY, and HAVING clauses

---

## Database Tables

### 1. Users Table

This table stores information about system users.

| Field    | Description                     |
| -------- | ------------------------------- |
| user_id  | Unique identifier for each user |
| name     | User's full name                |
| email    | User email (must be unique)     |
| password | User password                   |
| phone    | User phone number               |
| role     | User role (Admin/Customer)      |

---

### 2. Vehicles Table

This table stores vehicle information.

| Field               | Description                                   |
| ------------------- | --------------------------------------------- |
| vehicle_id          | Unique identifier for each vehicle            |
| name                | Vehicle name                                  |
| type                | Vehicle type (car/bike/truck)                 |
| model               | Vehicle model                                 |
| registration_number | Vehicle registration number (unique)          |
| rental_price        | Rental price per day                          |
| status              | Vehicle status (available/rented/maintenance) |

---

### 3. Bookings Table

This table stores booking information.

| Field      | Description                 |
| ---------- | --------------------------- |
| booking_id | Unique booking ID           |
| user_id    | Reference to Users table    |
| vehicle_id | Reference to Vehicles table |
| start_date | Rental start date           |
| end_date   | Rental end date             |
| status     | Booking status              |
| total_cost | Total booking cost          |

---

## Database Relationships

* One User can make many Bookings (One-to-Many).
* One Vehicle can have many Bookings (One-to-Many).
* Each Booking belongs to exactly one User and one Vehicle.

---

## SQL Queries Implemented

### Query 1: INNER JOIN

Retrieve booking information along with customer name and vehicle name.

### Query 2: NOT EXISTS

Find all vehicles that have never been booked.

### Query 3: WHERE Clause

Retrieve all available vehicles of a specific type.

### Query 4: GROUP BY and HAVING

Find vehicles that have more than two bookings.

---

## ERD Link


ERD Link: https://viewer.diagrams.net/?tags=%7B%7D&lightbox=1&highlight=0000ff&edit=_blank&layers=1&nav=1&title=erd.drawio&dark=auto#R%3Cmxfile%3E%3Cdiagram%20name%3D%22Page-1%22%20id%3D%22iKpMpuFXHy1AOTLhEHNK%22%3EzVdtb9owEP41kboPlUJMoF%2FHWztVQ%2B1atn1DJrklVhM7sh0I%2B%2FVz5rw4DgOKhlQ%2BoNzj89l3zz1HcNA0Le45zuKvLITE8dywcNDM8bzxeKi%2BS2CvAX8w0kDESaihQQu8kN9QgW6F5iQE0XGUjCWSZF0wYJRCIDsY5pztum6%2FWNI9NcMR9ICXACd99AcJZazRO99t8QcgUVyfPHCrlRTXzhUgYhyynQGhuYOmnDGpn9JiCklZu7ouet%2FiH6vNxThQec6G9NVbPgYPy2XxOgyKn8P4eZncHohSQULu6xrsYiLhJcNBae8UzQ6axDJNlDVQj9p%2Fi5O88l8J4MLxFNFI0Ygmt9bHWMqV61rd0HNvnh4%2FGQsUp2CYkGJSJnOzWn55Xs1NzwwLsWM8NKGYUXM3ZyoVfUvgEgoj0apW98BSkHyvXGKTTlSRt2u5H9SEFg3l2t5b67hqvaiJ3bKjHiqC3kGWdw2yvkNMggTO5Gurvc%2BhTO4z00z1ZGg5gYgIybEkjK5pnm6AH%2Ba3TBYn64yTwIwnJJa5uIxV%2FzSrI89idXAtVn0dF8LeIOrTzHIewJFYqNcOQMPP5RhUFi1F0WkGznIaQnk591BrnK5kXUgOiSJy203AqK5%2FpHjVCU%2BMqGyb%2BqNxt%2F7ItULoWlS7zLFnBRpaRPbuIjGPQPYC%2FeWySftyetE1RDth7I3Q6EzRbrT3QdEaA3jRWegqvbumtMflOsSyM6JpaEO1RtuZwEopB0zIqwkX3VnCtRvnvwn37h3CPSjI%2BbcU0%2F0xSaoByd6aFw9PV3lBynvOGiLqcBssYIZFXOOG34eStjeyFHmptJF%2FItCVpV3%2FJFzeAQZlR3rA4LhpGZthuy%2FsvvlQHeDbM%2FnSDhi51%2BoAZbav5tq9%2FX%2BD5n8A%3C%2Fdiagram%3E%3C%2Fmxfile%3E

---

## Technologies Used

* SQL
* PostgreSQL/MySQL
* Draw.io / Lucidchart

---

## Repository Structure

```text
vehicle-rental-system/
│
├── README.md
├── queries.sql
```

---

## Author

Jannatul Ferdous
