# Express + TypeScript + PostgreSQL CRUD API

A simple REST API built with **Express**, **TypeScript**, and **PostgreSQL**. This project demonstrates basic CRUD (Create, Read, Update, Delete) operations using the `pg` package.

---

## 🚀 Features

* Express.js Server
* TypeScript Support
* PostgreSQL Database
* Create User
* Get All Users
* Get Single User
* Update User
* Delete User
* JSON Request Handling
* Parameterized SQL Queries (SQL Injection Protection)

---

## 🛠️ Technologies Used

* Node.js
* Express.js
* TypeScript
* PostgreSQL
* pg
* ts-node-dev

---

## 📁 Project Structure

```text
express-server-auth/
│
├── src/
│   ├── config/
│   │   └── index.ts
│   └── server.ts
│
├── package.json
├── tsconfig.json
├── .env
└── README.md
```

---

## 📦 Installation

Clone the repository:

```bash
git clone <repository-url>
```

Go to the project directory:

```bash
cd project-name
```

Install dependencies:

```bash
npm install
```

---

## ▶️ Run the Project

Development Mode

```bash
npm run dev
```

Production Build

```bash
npm run build
```

Run Production

```bash
npm start
```

---

## ⚙️ Environment Variables

Create a `.env` file.

```env
DATABASE_URL=postgresql://username:password@host/database?sslmode=require
PORT=9000
```

---

## 🗄️ Database Table

```sql
CREATE TABLE IF NOT EXISTS users (
    id SERIAL PRIMARY KEY,
    name VARCHAR(20),
    email VARCHAR(255) UNIQUE NOT NULL,
    password VARCHAR(255) NOT NULL,
    is_active BOOLEAN DEFAULT TRUE,
    age INT,
    created_at TIMESTAMP DEFAULT NOW(),
    updated_at TIMESTAMP DEFAULT NOW()
);
```

---

# API Endpoints

## Create User

**POST**

```text
/api/user
```

Request Body

```json
{
  "name": "Munna",
  "email": "munna@gmail.com",
  "age": 22,
  "password": "123456"
}
```

Response

```json
{
  "message": "Successfully created",
  "data": {
    "id": 1,
    "name": "Munna",
    "email": "munna@gmail.com",
    "age": 22
  }
}
```

---

## Get All Users

**GET**

```text
/api/user
```

---

## Get Single User

**GET**

```text
/api/user/:id
```

Example

```text
/api/user/1
```

---

## Update User

**PUT**

```text
/api/user/:id
```

Request Body

```json
{
  "name": "Updated Name",
  "age": 25,
  "password": "newpassword",
  "is_active": true
}
```

---

## Delete User

**DELETE**

```text
/api/user/:id
```

Example

```text
/api/user/1
```

---

## 📌 HTTP Status Codes

| Status Code | Description           |
| ----------- | --------------------- |
| 200         | OK                    |
| 201         | Created               |
| 400         | Bad Request           |
| 404         | Not Found             |
| 409         | Duplicate Resource    |
| 500         | Internal Server Error |

---

## 📌 Example Response

```json
{
  "success": true,
  "message": "User retrieved successfully",
  "data": {
    "id": 1,
    "name": "Munna",
    "email": "munna@gmail.com",
    "age": 22,
    "is_active": true
  }
}
```

---

## 📌 Future Improvements

* Password Hashing (bcrypt)
* JWT Authentication
* Login API
* Refresh Token
* Input Validation
* Environment Variables
* MVC Architecture
* Error Handling Middleware
* Docker Support
* Swagger API Documentation

---

## 👨‍💻 Author

**Mofazzal Hossen**

Learning Backend Development using:

* TypeScript
* Express.js
* PostgreSQL
* REST API
* Authentication

---

## ⭐ If you like this project

Give the repository a ⭐ on GitHub.
