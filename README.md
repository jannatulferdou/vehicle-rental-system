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

Paste your ERD public link here.

Example:

ERD Link: https://your-erd-link-here

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
