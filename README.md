## **📌 README Requirements**  

### **1️⃣ Steps to Set Up the Database (Migrations, Environment Variables)**  

#### **🔹 Create the PostgreSQL Database**  
```sql
CREATE DATABASE task_management;
\c task_management;
CREATE TABLE users (
    id SERIAL PRIMARY KEY,
    username VARCHAR(50) UNIQUE NOT NULL,
    password TEXT NOT NULL
);
CREATE TABLE tasks (
    id SERIAL PRIMARY KEY,
    title VARCHAR(255) NOT NULL,
    description TEXT,
    isComplete BOOLEAN DEFAULT FALSE,
    userId INTEGER REFERENCES users(id) ON DELETE CASCADE
);
```

#### **🔹 Set Up Environment Variables (.env file in backend)

```sql
DATABASE_URL=postgres://username:password@localhost:5432/task_management
JWT_SECRET=your_secret_key
```
### **2️⃣ How to Run the Backend

#### **🔹 Navigate to the Backend Directory

```sql
cd TaskManager_Backend
```

### 🔹 Install Dependencies

```sql
npm install
```

### 🔹 Start the Backend Server

```sql
npm run dev
```

📌 The backend will run on http://localhost:5000.


## 3️⃣ How to Run the Frontend

### 🔹 Navigate to the Frontend Directory

```sql
cd TaskManager_Frontend
```

### 🔹 Install Dependencies

```sql
npm install
```

### 🔹 Create .env file for the Frontend

```sql
REACT_APP_BACKEND_URL=http://localhost:5000
```

### 🔹 Start the Frontend Server

```sql
npm start
```

📌 The frontend will run on http://localhost:3000.

## 4️⃣ Any Relevant Notes on Testing

- > Ensure backend is running before starting the frontend.
      
- > Use Postman or cURL to test API endpoints.
      
- > Test with a new user registration, login, and CRUD operations.
      
- > If JWT authentication fails, check if the token is stored in localStorage.
      
- > If PostgreSQL is not running, restart the database service.

## 5️⃣ Salary Expectations per Month (Mandatory)

      💰 Expected Monthly Salary: 22

