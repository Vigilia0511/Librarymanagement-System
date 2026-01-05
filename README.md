# Library Management System

This is a simple Library Management System developed as a school activity for BSIT 3A.

## Description

The Library Management System is a Java-based desktop application built using Swing for the GUI and MySQL for the database. It allows users to manage books, members, and book borrowings in a library.

### Features

- **Books Management**: Add, update, delete, and search books.
- **Members Management**: Add, update, delete, and search library members.
- **Borrowings Management**: Record book borrowings, returns, and calculate fines for overdue books.
- **Reports**: View reports on books, members, and borrowings.

## Prerequisites

- Java JDK (version 8 or higher)
- MySQL Server
- MySQL Connector/J (included in the project)

## Setup Instructions

1. **Install MySQL Server** and ensure it's running on localhost:3306.

2. **Create the Database**:
   - Open MySQL command line or phpMyAdmin.
   - Create a database named `library_db`.
   - Import the `database/library_db.sql` file to set up the tables and sample data.

3. **Configure Database Connection**:
   - In `src/librarymanagement/LibraryManagementSystem.java`, update the database credentials if necessary:
     ```java
     private static final String URL = "jdbc:mysql://localhost:3306/library_db";
     private static final String USER = "root";
     private static final String PASSWORD = ""; // Set your MySQL password here
     ```

4. **Compile and Run**:
   - Navigate to the `src` directory.
   - Compile the Java files:
     ```
     javac -cp "../mysql-connector-j-9.3.0/mysql-connector-j-9.3.0.jar" librarymanagement/*.java
     ```
   - Run the application:
     ```
     java -cp ".;../mysql-connector-j-9.3.0/mysql-connector-j-9.3.0.jar" librarymanagement.LibraryManagementSystem
     ```

## Project Structure

- `src/`: Source code
- `database/`: Database schema and sample data
- `mysql-connector-j-9.3.0/`: MySQL JDBC driver
- `bin/`: Compiled classes (if any)

## Note

This project was created as part of a school assignment and is for educational purposes only.