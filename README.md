## Node.js + MySQL CRUD API

A simple and clean CRUD (Create, Read, Update, Delete) RESTful API built with Node.js, Express, and MySQL using `mysql2/promise`. Ideal for learning full-stack development or integrating with frontend applications.

---

## 🛠️ Technologies Used

- Node.js
- Express.js
- MySQL (with `mysql2/promise`)
- dotenv
- Morgan (logging middleware)

---

## ⚙️ Getting Started

### 1. Clone the Repository
```bash
git clone https://github.com/Devkoyani/Node_MySQL_CRUD.git
cd node-mysql-crud
npm install
```

### 2. Create a .env file in the project root and add
```bash
PORT = 8080
```

### 3. Start MySQL Server and open MySQL Workbench.
Run the following SQL:
```bash
CREATE DATABASE students_db;
USE students_db;

CREATE TABLE students (
  id INT AUTO_INCREMENT PRIMARY KEY,
  name VARCHAR(100) NOT NULL,
  roll_no INT UNIQUE_INDEX NOT NULL,
  standard INT NOT NULL,
  fees INT,
  medium VARCHAR(50)
);
```

### 4. Configure DB Credentials
Update the file at config/db.js to match your MySQL setup:
```bash
const mysql = require('mysql2/promise');

const mySqlPool = mysql.createPool({
  host: 'localhost',
  user: 'root',
  password: 'your-password',
  database: 'students_db',
});

module.exports = mySqlPool;
```

### 5. Start the Server
```bash
npm run server
```
