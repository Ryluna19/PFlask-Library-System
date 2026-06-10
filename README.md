# 📚 Flask Library System

A web-based library system built with **Python, Flask, MySQL, HTML and CSS**.

This project was originally developed as an academic assignment and later improved as a portfolio project, with better code organization, environment-based configuration, password hashing, and a polished dark user interface.

---

## 🎯 10-Second Overview

* Flask web application with server-side rendered pages
* User registration, login and logout
* Session-based authentication
* MySQL database integration
* Password hashing using Werkzeug
* Environment variables with `.env`
* User account settings page
* Dark responsive interface
* Academic project improved for portfolio presentation

---

## 📸 Screenshots

### Login Page

<img width="1219" height="837" alt="login" src="https://github.com/user-attachments/assets/020593bb-9364-4d08-97cb-7d8c35334e37" />

### Create Account Page

<img width="918" height="585" alt="register" src="https://github.com/user-attachments/assets/e0613925-c4fd-466d-88a5-2ddda15a3406" />

### Library Page

<img width="985" height="864" alt="library" src="https://github.com/user-attachments/assets/4c75d8cc-1218-47d7-ace2-4015fcb1ded4" />

### User Settings Page

<img width="962" height="828" alt="setting" src="https://github.com/user-attachments/assets/bd7517c1-c49b-47b0-902a-efd336d85c64" />

---

## ✨ Features

### Authentication

* User registration
* User login
* User logout
* Session-based access control
* Protected library page
* Password hashing before storing user credentials

### User Management

* Update user name
* Update user email
* Update user password
* Delete user account

### Library Interface

* Library catalog page
* Book cards with title, author and rating
* Supporters/user list
* Navigation between library and account settings

### Security Improvements

* Database credentials moved to environment variables
* Passwords stored as hashes instead of plain text
* SQL queries using parameterized values
* `.env` ignored from version control

---

## 🛠 Tech Stack

### Backend

* Python
* Flask
* MySQL Connector
* Werkzeug Security
* python-dotenv

### Database

* MySQL
* MySQL Workbench

### Frontend

* HTML
* CSS
* Bootstrap
* Font Awesome

### Tools

* Git
* GitHub
* VS Code / PyCharm

---

## 🧩 Project Structure

```txt
PFlask-Library-System/
│
├── A3 API/
│   ├── app.py
│   ├── requirements.txt
│   ├── .env.example
│   ├── .gitignore
│   │
│   ├── templates/
│   │   ├── login_base.html
│   │   ├── registro_base.html
│   │   ├── biblioteca_base.html
│   │   └── usuario_configuracao_base.html
│   │
│   ├── static/
│   │   ├── css/
│   │   │   ├── main.css
│   │   │   ├── other.css
│   │   │   ├── custom.css
│   │   │   └── fontawesome-all.min.css
│   │   │
│   │   └── Fotos/
│   │
│   ├── Escopo.pdf
│   ├── Prototipação.pdf
│   └── Script Tabela.jpg
│
├── assets/
│   ├── login.png
│   ├── register.png
│   ├── library.png
│   └── settings.png
│
└── README.md
```

---

## 📋 Prerequisites

Before running this project, make sure you have installed:

* Python
* pip
* MySQL Server
* MySQL Workbench or MySQL Command Line Client
* Git

---

## 🚀 Installation & Setup

### 1. Clone the repository

```bash
git clone https://github.com/Ryluna19/PFlask-Library-System.git
cd PFlask-Library-System
```

---

### 2. Go to the project folder

```bash
cd "A3 API"
```

---

### 3. Create a virtual environment

```bash
python -m venv venv
```

Activate the virtual environment on Windows:

```bash
venv\Scripts\activate
```

---

### 4. Install dependencies

```bash
pip install -r requirements.txt
```

---

### 5. Configure environment variables

Create a `.env` file inside the `A3 API` folder:

```env
SECRET_KEY=your_secret_key
DB_HOST=localhost
DB_USER=your_mysql_user
DB_PASSWORD=your_mysql_password
DB_NAME=biblioteca
```

You can use `.env.example` as a reference.

---

### 6. Create the MySQL database

Open MySQL Workbench and run:

```sql
CREATE DATABASE biblioteca;

USE biblioteca;

CREATE TABLE usuarios (
    id INT AUTO_INCREMENT PRIMARY KEY,
    nome VARCHAR(255),
    email VARCHAR(255) UNIQUE,
    senha VARCHAR(255)
);
```

---

### 7. Run the application

```bash
python app.py
```

The application will run on:

```txt
http://127.0.0.1:5000
```

---

## 🗄 Database Schema

### usuarios

| Field | Type         | Description                 |
| ----- | ------------ | --------------------------- |
| id    | INT          | Primary key, auto increment |
| nome  | VARCHAR(255) | User name                   |
| email | VARCHAR(255) | Unique user email           |
| senha | VARCHAR(255) | Hashed user password        |

---

## 🔐 Authentication Flow

1. The user creates an account.
2. The password is hashed before being saved in the database.
3. During login, the system searches the user by email.
4. The typed password is compared with the saved hash.
5. If the credentials are valid, the user ID and name are stored in the session.
6. Protected pages check if the user is logged in before allowing access.

---

## 📌 Main Routes

| Route                   | Method     | Description            |
| ----------------------- | ---------- | ---------------------- |
| `/`                     | GET        | Protected library page |
| `/login`                | GET / POST | User login             |
| `/register`             | GET / POST | User registration      |
| `/usuario_configuracao` | GET / POST | User settings page     |
| `/logout`               | GET        | User logout            |

---

## 🎓 Project Context

This project was originally created for a college assignment focused on building a library website using Python, HTML, CSS and MySQL.

After the original version, the project was improved for portfolio purposes with:

* Environment variable configuration
* Password hashing
* Improved UI styling
* Cleaner GitHub presentation
* More professional documentation

---

## 🧠 What This Project Demonstrates

This project demonstrates knowledge of:

* Flask routes
* Template rendering with HTML
* Form handling
* User sessions
* MySQL database connection
* CRUD-style user account operations
* Password hashing
* Environment variables
* Basic web security practices
* Frontend styling with CSS
* Git and GitHub workflow

---

## 🚧 Future Improvements

* Add book management CRUD
* Add admin area
* Add flash message styling
* Add backend form validation
* Add pagination for larger catalogs
* Add automated tests
* Improve database migrations
* Deploy the application online
* Convert part of the project into a REST API

---

## 👨‍💻 Author

**Ryan Santos**

* GitHub: [Ryluna19](https://github.com/Ryluna19)
* Focused on full-stack development with React, Node.js, Python, Flask, SQL and PostgreSQL/MySQL
* Seeking internship / junior developer opportunities

---

## 📌 Note

This is a portfolio and academic project.

It is not intended for production use without additional improvements such as stronger validation, CSRF protection, deployment configuration, automated tests, logging, and production-ready database management.
