# Distributed Book Storage Using XML

This repository contains the implementation of a distributed data storage system for storing and querying book information using XML files. The system partitions data by hashing author names and stores the data in two separate XML files.

---

## Table of Contents

- [Introduction](#introduction)
- [Operations](#operations)
  - [Add Book](#1-add_book)
  - [Search by Author](#2-search_by_author)
  - [Search by Year](#3-search_by_year)
---

## Introduction

The project demonstrates a distributed data storage system for a collection of books using XML files. Each book is represented as an XML element containing the following attributes:
- **author**: The author of the book.
- **title**: The title of the book.
- **year**: The publication year of the book.
- **price**: The price of the book.

Books are partitioned based on a hash of the author's name and stored in one of two XML files (`file0.xml` or `file1.xml`). The operations include adding books and querying by author or year, ensuring efficient data retrieval.

---

## Operations

### 1. `add_book`

This method stores book information in one of the two XML files based on the hash value of the author's name.

python3 script.py add_book 100 '{"author": "John Smith", "title": "Book Title", "year": 2023, "price": 19.99}'

### 2. `search_by_author`

This method retrieves all books written by a specific author from the XML files.

python3 script.py search_by_author "<author_name>"

### 3. `search_by_year`

This method retrieves all books published in a specified year from the XML files.

python3 script.py search_by_author "John Smith"
