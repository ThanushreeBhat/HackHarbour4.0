# 📝 Internship Homework Assignments

Welcome to the homework repository for the Summer Internship. Below you will find the assignments for each day. Please ensure you complete them and submit the required deliverables.

---

## 📋 Homework Summary

| Day | Assignment | Main Skill | Lecture Notes |
| :--- | :--- | :--- | :--- |
| **Day 1** | [Collaborate on a Friend's Repository](#-day-1--git--github) | Git Collaboration | [Day 1 Notes](Day1_Git_GitHub.md) |
| **Day 2** | [Personal Portfolio Website](#-day-2--web-fundamentals) | HTML + CSS + JavaScript | [Day 2 Notes](Day2_Web_Fundamentals.md) |
| **Day 3** | [College Database & Queries](#-day-3--sql) | SQL + Database Design | [Day 3 Notes](Day3_API_Basics_Databases.md) |
| **Day 4** | [LeetCode Practice](#-day-4--competitive-programming) | Problem Solving + DSA | [Day 4 Notes](Day4_Competitive_Programming.md) |

---

## 🤝 Day 1 — Git & GitHub

### 📝 Assignment: Collaborate on a Friend's Repository
Work with a partner and contribute to your friend's GitHub repository.

#### 📋 Requirements
- [ ] **Clone** your friend's repository to your local machine.
- [ ] **Create or modify** a file in the repository.
- [ ] **Stage** your changes.
- [ ] **Commit** your changes with a meaningful commit message.
- [ ] **Push** your changes back to the GitHub repository.
- [ ] **Verify** the commit is visible on GitHub with your friend.

#### 💻 Commands to Practice
```bash
# Clone the repository
git clone <repository-url>

# Navigate into the project folder
cd <repository-name>

# Check current repository status
git status

# Stage all changes
git add .

# Commit changes with a descriptive message
git commit -m "Add contribution"

# Push changes to GitHub
git push
```

#### 📤 Submission Deliverables
* [ ] GitHub repository URL
* [ ] Screenshot showing your commit history/graph on GitHub
* [ ] The exact commit message you used

> 🎯 **Learning Outcome:** Understand how Git is used for collaborative team environments, not just for storing personal code.

---

## 🎨 Day 2 — Web Fundamentals

### 📝 Assignment: Personal Portfolio Website
Create a simple, elegant personal portfolio website using HTML, CSS, and JavaScript.

#### 📋 Minimum Requirements

##### 🌐 HTML Structure
- [ ] Introduction / Name
- [ ] About Me section
- [ ] Education details
- [ ] Skills list
- [ ] Projects showcase
- [ ] Contact section
- [ ] GitHub / profile link
- [ ] At least one image

##### 💅 CSS Styling
- [ ] Harmonious colors
- [ ] Professional fonts
- [ ] Clean spacing (margin & padding)
- [ ] Borders & outlines
- [ ] Custom backgrounds
- [ ] Interactive buttons
- [ ] Basic layout structured using **Flexbox**

##### ⚡ JavaScript Interaction
- [ ] Add at least one dynamic feature.
  *Examples: Dark/Light mode toggle, button that dynamically changes text, custom greeting based on user input, simple form validation/interaction, or collapsible content sections.*

#### 📁 Suggested Folder Structure
```text
portfolio/
├── index.html
├── style.css
└── script.js
```

#### 📤 Submission Deliverables
* [ ] GitHub repository link hosting the code
* [ ] Live website URL (if deployed)
* [ ] A concise `README.md` file explaining your project and features

#### 🌟 Bonus Challenges
- [ ] Make the website fully responsive for mobile and desktop screens.
- [ ] Deploy it live using GitHub Pages or another hosting platform (Vercel, Netlify, etc.).

> 🎯 **Learning Outcome:** Combine structure (HTML), styling (CSS), and behavior (JavaScript) to build and deploy a complete web project from scratch.

---

## 🗄️ Day 3 — SQL

### 📝 Assignment: College Database Design
Design a simple database schema for a college and perform key SQL operations.

#### 📋 Requirements
- [ ] Create at least **3 tables** (e.g., `students`, `departments`, `courses`).
- [ ] Insert at least **8–10 student records** into the database.

##### Example `students` table creation query:
```sql
CREATE TABLE students (
    id INTEGER PRIMARY KEY,
    name TEXT,
    age INTEGER,
    department TEXT,
    cgpa REAL
);
```

#### 🔍 SQL Queries to Write & Run

##### 1. Basic Queries
```sql
-- Retrieve all columns for all students
SELECT * FROM students;

-- Retrieve only student names and CGPAs
SELECT name, cgpa FROM students;

-- Filter students with CGPA greater than 8.0
SELECT * FROM students WHERE cgpa > 8.0;
```

##### 2. Aggregate Functions
Demonstrate the use of the following SQL functions:
```sql
SELECT COUNT(*) FROM students;
SELECT AVG(cgpa) FROM students;
SELECT MAX(cgpa) FROM students;
SELECT MIN(cgpa) FROM students;
SELECT SUM(cgpa) FROM students;
```

##### 3. GROUP BY Queries
```sql
-- Count students in each department
SELECT department, COUNT(*)
FROM students
GROUP BY department;

-- Find average CGPA by department
SELECT department, AVG(cgpa)
FROM students
GROUP BY department;
```

#### 📤 Submission Deliverables
* [ ] An `.sql` file containing all query scripts
* [ ] Screenshots of the created tables/database schema
* [ ] Screenshots of your query execution outputs
* [ ] A short written explanation of the aggregate functions used

> 🎯 **Learning Outcome:** Learn how real-world college entities and relationships are represented in database tables and how to retrieve and aggregate information using SQL.

---

## 🧠 Day 4 — Competitive Programming

### 📝 Assignment: LeetCode Practice
Implement and submit solutions to the three core algorithmic problems covered in the training session.

#### 📋 Covered Problems
For each problem, submit the required approaches:

##### 1. [Two Sum](https://leetcode.com/problems/two-sum/)
- [ ] Brute-force approach ($O(N^2)$)
- [ ] Optimized Hash Map approach ($O(N)$)

##### 2. [Best Time to Buy and Sell Stock](https://leetcode.com/problems/best-time-to-buy-and-sell-stock/)
- [ ] Brute-force approach ($O(N^2)$)
- [ ] Optimized one-pass approach ($O(N)$)

##### 3. [Trapping Rain Water](https://leetcode.com/problems/trapping-rain-water/)
- [ ] Brute-force approach ($O(N^2)$)
- [ ] Optimized Two Pointer approach ($O(N)$)

#### 📤 Submission Deliverables
* [ ] Links to your submitted LeetCode profiles/solutions
* [ ] Brute-force code solutions
* [ ] Optimized code solutions
* [ ] Written analysis of the time and space complexity for each approach
* [ ] A short paragraph explaining the logic behind why the optimized solution performs better

> 🎯 **Learning Outcome:** Strengthen problem-solving skills and learn how to optimize algorithms from $O(N^2)$ brute-force solutions to highly efficient $O(N)$ implementations.
