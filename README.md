# Student Result Management System

A Java web application for managing student academic records, including admin login, student result entry, and result viewing. The project uses Java, JSP, MySQL, and a web-based front end for student and administrator workflows.

## Overview

This project provides a simple student result management portal where:

- Admins can log in and manage student records.
- New students can be added to the system.
- Results can be inserted and tracked.
- Students can view their academic results on a dedicated dashboard.
- The application is structured as a Java web project with JSP pages and MySQL connectivity.

## Features

- Admin login flow
- Student dashboard
- Add new student records
- Insert and manage results
- View student results
- Responsive web UI using HTML/CSS
- Database-backed persistence via JDBC and MySQL

## Tech Stack

- Java
- JSP / Java EE web pages
- MySQL
- JDBC
- Apache Tomcat (expected for deployment)
- HTML, CSS, JavaScript

## Project Structure

```text
Student Result Management System/
├── build/
│   └── classes/
├── src/
│   └── main/
│       ├── java/
│       │   └── Project/
│       │       └── ConnectionProvider.java
│       └── webapp/
│           └── webcontent/
│               ├── adminLogin.html
│               ├── adminHome.jsp
│               ├── studentHome.jsp
│               ├── addNewStudent.jsp
│               ├── insertNewResult.jsp
│               ├── style.css
│               ├── index.html
│               └── ...
└── README.md
```

## Prerequisites

Before running the project, make sure you have:

- Java JDK installed
- Apache Tomcat or a Java web server
- MySQL Server installed and running
- MySQL Connector/J JDBC driver
- A MySQL database named `project1`

## Database Setup

The application connects to MySQL using the following JDBC URL in `ConnectionProvider.java`:

```java
jdbc:mysql://localhost:3306/project1
```

Update the database credentials in `ConnectionProvider.java` if your local MySQL setup differs:

```java
Connection con = DriverManager.getConnection(
    "jdbc:mysql://localhost:3306/project1",
    "root",
    "Vicky@18may"
);
```

Create the database and required tables before starting the app. The project expects a local MySQL instance with the `project1` database available.

## Running the Application

1. Install and start MySQL.
2. Create the `project1` database.
3. Configure the database username/password in `ConnectionProvider.java`.
4. Deploy the project in Apache Tomcat or your preferred Java web server.
5. Open the application in a browser using the Tomcat URL, typically:

```text
http://localhost:8080/Student_Result_Management_System/
```

or the appropriate context path configured in your server.

## Main Application Pages

- `adminLogin.html` – admin login page
- `adminHome.jsp` – admin dashboard
- `studentHome.jsp` – student result dashboard
- `addNewStudent.jsp` – add a new student
- `insertNewResult.jsp` – add marks/results
- `index.html` – landing/entry page

## Notes

This repository currently contains a Java web application rather than a modern Spring Boot or React app. The project is well suited for learning database-driven Java web development and managing academic records through JSP pages and MySQL.

## License

This project does not currently include an explicit license file. If you plan to share or publish it publicly, consider adding a license such as MIT or Apache 2.0.
