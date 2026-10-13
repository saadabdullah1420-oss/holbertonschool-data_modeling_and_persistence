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

## Task 1: Insert Data

1-insert_data.sql inserts the five required books using one INSERT statement.
All columns are explicitly listed to map values correctly.

Run once after creating the books table:

    sqlite3 my_database.db < 1-insert_data.sql

## Task 2: Retrieve All Data

2-select_all.sql retrieves every column and row from books.
The query does not filter, sort, limit, or modify data.

    sqlite3 my_database.db < 2-select_all.sql

## Task 3: Select Specific Columns

3-select_columns.sql retrieves title and price for all books.
The output columns are ordered as title, then price.

    sqlite3 my_database.db < 3-select_columns.sql
