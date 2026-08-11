# Day 3 - API Basics & Databases

## 1. What is an API?
An **API (Application Programming Interface)** acts as a messenger between different software systems, allowing them to communicate and share data.

> **Real-world analogy**: Think of a restaurant.
> * You (the Client) look at the menu and decide what to order.
> * The Cook (the Server) prepares the food.
> * The Waiter (the API) takes your order to the kitchen and returns the food to you.

<div style="text-align: center;">
  <img src="https://github.com/so-sc/HackHarbor-3.0/blob/main/Tech/assets/api-waiter-visual.webp" alt="API Waiter Analogy" width="400">
</div>

---

## 2. HTTP Request-Response Structure
When a client communicates with a server via an API, it uses the **HTTP protocol** with the following components:

### HTTP Methods (Verbs)
* **GET:** Retrieve data from a server (e.g., fetch a list of products).
* **POST:** Send new data to a server (e.g., create a new user account).
* **PUT/PATCH:** Update existing data on a server.
* **DELETE:** Remove data from a server.

### Common HTTP Status Codes
* **200 OK:** Request succeeded.
* **201 Created:** Request succeeded and a resource was created.
* **400 Bad Request:** Server could not understand the request due to invalid syntax.
* **401 Unauthorized:** Authentication is required.
* **404 Not Found:** The requested resource was not found.
* **500 Internal Server Error:** The server encountered an error.

<div style="text-align: center;">
  <img src="https://github.com/so-sc/HackHarbor-3.0/blob/main/Tech/assets/HTTP%20Status%20Code%20Chart.png" alt="HTTP Status Code Chart" width="500">
</div>

---

## 3. Testing APIs using Postman
Postman is a popular tool for building and using APIs. We can construct requests (defining methods, headers, and request body) and view the server's responses.

### Example: Making a GET Request in Postman
1. Set the request method to `GET`.
2. Enter the URL (e.g., `https://api.github.com/users/github`).
3. Click **Send** to view the JSON response.

<div style="text-align: center;">
  <img src="https://github.com/so-sc/HackHarbor-3.0/blob/main/Tech/assets/GET%20Request%20in%20Postman.png" alt="GET Request in Postman" width="600">
</div>

---

## 4. Introduction to Databases & SQL
A **database** is an organized collection of structured information or data, typically stored electronically in a computer system.

### SQL vs. NoSQL
* **SQL (Relational Databases):** Data is organized into tables with rows and columns (e.g., SQLite, MySQL, PostgreSQL).
* **NoSQL (Non-Relational Databases):** Data is stored in key-value pairs, document formats, or graphs (e.g., MongoDB, Redis).

### What is SQL?
**SQL (Structured Query Language)** is the standard language used to interact with relational databases.

---

## 5. Hands-on Database Practice with SQLite
We will use **SQLite Online** (https://sqliteonline.com/), a free browser-based tool to practice database commands.

### Step 1: Create a Table
Copy the SQL query below into the editor and click **Run**:
```sql
CREATE TABLE students (
    id INTEGER PRIMARY KEY,
    name TEXT,
    age INTEGER,
    grade TEXT
);
```

### Step 2: Insert Data (INSERT)
Add student records into the table:
```sql
INSERT INTO students (id, name, age, grade) VALUES (1, 'Alice', 20, 'A');
INSERT INTO students (id, name, age, grade) VALUES (2, 'Bob', 19, 'B');
INSERT INTO students (id, name, age, grade) VALUES (3, 'Charlie', 21, 'A');
```

### Step 3: Query Data (SELECT)
Retrieve information from the table:
```sql
-- Retrieve all columns for all students
SELECT * FROM students;

-- Retrieve only student names and grades
SELECT name, grade FROM students;

-- Filter students who received an 'A'
SELECT * FROM students WHERE grade = 'A';

-- Filter students older than 19
SELECT * FROM students WHERE age > 19;
```

### Step 4: Update Data (UPDATE)
Modify an existing record:
```sql
UPDATE students
SET grade = 'A'
WHERE name = 'Bob';
```

### Step 5: Delete Data (DELETE)
Remove records from the table:
```sql
DELETE FROM students WHERE name = 'Charlie';
```
Verify the deletion by running `SELECT * FROM students;`.
