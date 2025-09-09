📚 Library Management System – README

Overview

This project is a relational database system built in MySQL 8+ for managing a modern library. It handles core functions such as member registration, book cataloging, lending, reservations, and fine tracking.


---

Key Features

Structured Schema → Branches, librarians, members, books, authors, genres, publishers, and transactions.

Data Integrity → Primary/foreign keys, unique constraints, and check rules.

Indexes → Optimized performance for frequent queries.

Triggers → Automatic updates for book availability and fine calculation.

Stored Procedures → Simplify operations like checkout, return, and reservation.

Views → Ready-made reports (current loans, available copies, member fines).

Seed Data → Sample records for quick testing.



---

Example Usage

Checkout a copy


CALL sp_checkout('BC0001', 1, 1, DATE_ADD(CURDATE(), INTERVAL 14 DAY), @loan_id);

Return a copy


CALL sp_return('BC0002', CURDATE(), 2, @returned_loan);

View available copies


SELECT * FROM v_available_copies;


---

Requirements

MySQL 8.0 or later

SQL client (CLI, phpMyAdmin, DBeaver, or mobile SQL editor)



---

Learning Outcomes

Proper database normalization (1NF–3NF).

Use of views, triggers, and stored procedures.

Enforcing business rules at the database level.

Practical implementation of a Library Management System.
