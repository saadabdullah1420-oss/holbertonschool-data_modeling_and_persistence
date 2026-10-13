# SQL - CRUD Operations

SQL scripts for managing books using SQLite.

## Task 0: Create a Table

0-create_table.sql creates the books table.

- id: INTEGER PRIMARY KEY
- title: TEXT NOT NULL
- author: TEXT NOT NULL
- genre: TEXT NOT NULL
- price: REAL NOT NULL
- stock: INTEGER NOT NULL
- published_year: INTEGER NOT NULL

## Usage

    sqlite3 my_database.db < 0-create_table.sql

Run on a database where the books table does not already exist.
