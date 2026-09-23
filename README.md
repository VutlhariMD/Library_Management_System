# Library_Management_System (PostgreSQL)

## Sprint 1

* Create the Required tables

 CREATE TABLE authors (
id SERIAL PRIMARY KEY,
name VARCHAR(100),
nationality VARCHAR(100),
birth_year INT,
death_year INT
);

CREATE TABLE books (
id SERIAL PRIMARY KEY,
title VARCHAR(255),
author_id INT REFERENCES authors(id),
genres VARCHAR(100),
published_year INT,
available BOOL

);
CREATE TABLE patrons (
id SERIAL PRIMARY KEY,
name VARCHAR(255),
email VARCHAR(100),
borrowed_books INT[]
);

### Populate the tables with data

