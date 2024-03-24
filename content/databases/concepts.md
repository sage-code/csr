+++
title = "Concepts"
collection = "databases"
author = "Bard/Gemini"
date = 2024-03-24
weight = 31
chapter = false
disableToc = false
pre = "<b>📜</b>"
tags = ["basic", "concepts"]
description = "General database concepts and definitions"
+++

Absolutely, databases are the backbone of many data-centric applications. Here's a breakdown of the fundamental concepts and lingo programmers use:

**Building Blocks:**

* **Database:**  An organized collection of structured data, typically stored electronically. Think of it as a digital filing cabinet for information.
* **Table:**  The core unit of organization within a database. Imagine a table like a spreadsheet with rows and columns. Each table stores data about a specific subject, like "Customers" or "Products."
* **Row:**  A horizontal entry in a table, representing a single instance of data. In the "Customers" table, each row might represent a customer.
* **Column (Field):**  A vertical category in a table, containing a specific type of data about each row. In the "Customers" table, columns might hold data like "Customer ID," "Name," or "Email."

**Keys and Relationships:**

* **Primary Key:** A unique identifier for each row in a table. It ensures no two entries are identical.  Think of it as a customer ID number that distinguishes each customer in the "Customers" table. 
* **Foreign Key:** A column in one table that references the primary key of another table. This establishes connections between tables.  For example, an "Orders" table might have a "CustomerID" foreign key that links it back to the "Customers" table.

**Queries and Data Manipulation:**

* **SQL (Structured Query Language):** The standard language for interacting with relational databases. Programmers use SQL statements to retrieve, insert, update, and delete data. 
* **CRUD:**  An acronym for Create, Read, Update, and Delete, representing the fundamental operations performed on data in a database.

**Additional Lingo:**

* **Schema:**  The overall structure of a database, defining how tables are organized and related. 
* **DBMS (Database Management System):** Software that facilitates creating, managing, and interacting with databases.  Examples include MySQL, Oracle Database, and Microsoft SQL Server.

By understanding these core concepts, you'll have a solid foundation for grasping data-centric applications and the language programmers use when building them.