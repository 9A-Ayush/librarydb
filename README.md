# 📚 Library Management System - Database Schema

## 🧠 Objective
Design and implement a structured relational database schema for a Library Management System using SQL and visualize the structure via an ER diagram.

---

## 🧰 Tools Used
- MySQL Workbench / pgAdmin / SQLiteStudio
- SQL (Structured Query Language)
- ER Diagram Tool (draw.io / MySQL Workbench / dbdiagram.io)

---

## 📦 Features
- Manage books, authors, and categories
- Track members and their borrow records
- Define relationships between books and authors (Many-to-Many)
- Implement loans with return tracking

---

## 🧱 Database Entities

### 1. Authors
Stores author information.
- author_id (Primary Key)
- name

### 2. Categories
Book categories/genres.
- category_id (Primary Key)
- name

### 3. Books
Contains book information.
- book_id (Primary Key)
- title
- category_id (Foreign Key → Categories)
- published_year

### 4. BookAuthors
Join table for many-to-many relationship between books and authors.
- book_id (Foreign Key → Books)
- author_id (Foreign Key → Authors)

### 5. Members
People who borrow books.
- member_id (Primary Key)
- name
- email
- membership_date

### 6. Loans
Tracks borrowed books and return dates.
- loan_id (Primary Key)
- book_id (Foreign Key → Books)
- member_id (Foreign Key → Members)
- loan_date
- return_date

---

## 🔗 Relationships

- A book can have multiple authors (Many-to-Many)
- A book belongs to one category
- A member can borrow many books (One-to-Many)
- Each loan records a book borrowed by a member

---

## 📜 How to Use

1. *Create Database*
   ```sql
   CREATE DATABASE LibraryDB;
   USE LibraryDB;
2.Run SQL Schema Script

    Execute the provided SQL script to create all tables with foreign keys.

3.Visualize

    Use the provided ER diagram image to understand relationships.

🖼 ER Diagram

![WhatsApp Image 2025-06-23 at 19 32 48_cb133270](https://github.com/user-attachments/assets/9b345388-ba23-4018-be35-68c109c55fb8)
