# SQL - Joins & Relationships

SQL queries for working with related tables using SQLite.

## Task 1: Books with Their Authors

1-books-with-authors.sql uses INNER JOIN to connect books to authors.
The join matches books.author_id with authors.id.
Returns title and author_name, ordered by title ascending.

## Usage

    sqlite3 library.db < 1-books-with-authors.sql

## Task 3: Students and Their Courses

3-students-and-courses.sql joins students, enrollments, and courses.
Returns one row per enrollment with student_name and course_title.
Results are ordered ascending by student_name, then course_title.

    sqlite3 library.db < 3-students-and-courses.sql
