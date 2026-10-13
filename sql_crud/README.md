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

## Task 4: Filter Rows

- 4-filter_by_genre.sql: titles and authors of Tech books.
- 4-filter_by_price.sql: titles and prices where price > 20.
- 4-filter_with_and.sql: titles and prices where genre is Tech and price > 30.
- 4-filter_with_or.sql: titles and genres where genre is Fantasy or price < 10.

Each file contains one SELECT query and does not modify data.
Execute each file against the provided dataset, for example:

    sqlite3 books_dataset.db < 4-filter_by_genre.sql

## Task 5: Update Rows

- 5-update_by_id.sql: sets the price of book 3 to 35.00.
- 5-update_by_condition.sql: adds 5 to stock for books published before 2000.
- 5-update_with_and.sql: reduces prices by 10% for Tech books with stock > 5.

Each file contains one UPDATE statement with SET and WHERE.
Execute each file independently on a clean copy of the provided dataset.

## Task 6: Delete Rows

- 6-delete_by_id.sql: deletes the book with id 8.
- 6-delete_by_condition.sql: deletes books with zero stock.
- 6-delete_with_and.sql: deletes books published before 1950 with price < 9.

Each file contains one DELETE statement with WHERE.
Execute each file independently on a clean copy of the provided dataset.

## Task 7: Order and Limit Results

- 7-order_by_price_asc.sql: all books from lowest to highest price.
- 7-order_by_year_desc.sql: all books from newest to oldest publication year.
- 7-limit_results.sql: the three cheapest books.
- 7-order_and_limit.sql: the five books with the highest stock.

Each file contains one SELECT query and does not modify data.

## Task 8: Aggregate Functions

- 8-count_books.sql: counts all book records.
- 8-average_price.sql: calculates the average price.
- 8-max_stock.sql: finds the maximum stock.
- 8-total_stock.sql: sums all available units.
- 8-min_price.sql: finds the minimum price.

Each file returns a single value without modifying data.

## Task 9: Group Data

- 9-count_by_genre.sql: counts books per genre.
- 9-average_price_by_genre.sql: calculates average price per genre.
- 9-total_stock_by_genre.sql: sums available stock per genre.
- 9-count_by_author.sql: counts books per author.

Each file contains one grouped SELECT query without modifying data.
Result order is not guaranteed.
