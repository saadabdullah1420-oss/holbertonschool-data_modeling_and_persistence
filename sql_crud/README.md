# SQL - CRUD Operations

SQL scripts for managing books using SQLite.

## Task 0: Create a Table

0-create_table.sql creates the books table with these columns:

- id: INTEGER PRIMARY KEY
- title: TEXT NOT NULL
- author: TEXT NOT NULL
- genre: TEXT
- price: REAL NOT NULL
- stock: INTEGER NOT NULL
- published_year: INTEGER

## Usage

Run on a database where the books table does not already exist:

    sqlite3 my_database.db < 0-create_table.sql

Inspect the table structure:

    sqlite3 my_database.db ".schema books"
