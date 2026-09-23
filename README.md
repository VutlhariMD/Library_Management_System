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

* AUTHORS
* <img width="300" height="350" alt="image" src="https://github.com/user-attachments/assets/cdbc3dbe-7292-4f7b-8f30-3dcf98406d4e" />

  

* BOOKS
  <img width="300" height="350" alt="image" src="https://github.com/user-attachments/assets/3684be2f-626c-4f7a-8799-f91f041be256" />

  
* PATRONS
<img width="300" height="350" alt="image" src="https://github.com/user-attachments/assets/eabf16d9-31bc-498f-b67f-98205abe5dfa" />

### Sprint 3: Read Operations (Queries)
* SELECT *
FROM books;

* SELECT * FROM books WHERE title= 'The Hobbit';
  
* SELECT * FROM books
WHERE author_id =2;



* SELECT *
FROM books
WHERE available = TRUE;

### Sprint 4: Update Operations
* Update books
SET available=false
Where id =3
