HOMEWORK ASSIGNMENTS

Day 1 — Git & GitHub
Assignment: Collaborate on a Friend's Repository
Work with a partner and contribute to your friend's GitHub repository.
Requirements
•	Clone your friend's repository using Git.
•	Create or modify a file in the repository.
•	Add your changes using git add.
•	Commit your changes with a meaningful commit message.
•	Push your changes to the repository.
•	Ask your friend to verify the commit on GitHub.
Commands to Practice
git clone <repository-url>
cd <repository-name>
git status
git add .
git commit -m "Add contribution"
git push
Submission
•	GitHub repository link
•	Screenshot showing your commit
•	Commit message
Learning Outcome: Students understand how Git is used for collaboration, not just for storing their own code.





Day 2 — Web Fundamentals
Assignment: Personal Portfolio Website
Create a simple personal portfolio website using HTML, CSS and JavaScript.
Minimum Requirements
HTML
•	Name / Introduction
•	About Me
•	Education
•	Skills
•	Projects
•	Contact section
•	GitHub/profile link
•	At least one image
CSS
•	Colors
•	Fonts
•	Spacing
•	Borders
•	Background
•	Buttons
•	Basic layout using Flexbox
JavaScript
•	Add at least one interactive feature.
•	Examples: Dark/Light mode, button that changes text, greeting based on user input, simple form interaction, or show/hide section.
Suggested Folder Structure
portfolio/
├── index.html
├── style.css
└── script.js
Submission
•	GitHub repository link
•	Working portfolio website
•	Short README explaining the project
Bonus
•	Make the website responsive.
•	Deploy it using GitHub Pages or another hosting platform.
Learning Outcome: Students combine HTML, CSS and JavaScript to create a complete small web project.




Day 3 — SQL
Assignment: College Database
Design a simple database for a college and perform basic SQL operations.
Requirements
Create at least 3 tables. Suggested tables:
•	students
•	departments
•	courses
Example students table:
CREATE TABLE students (
    id INTEGER PRIMARY KEY,
    name TEXT,
    age INTEGER,
    department TEXT,
    cgpa REAL
);
Insert at least 8–10 student records.
Basic Queries
SELECT * FROM students;

SELECT name, cgpa FROM students;

SELECT * FROM students WHERE cgpa > 8.0;
Aggregate Functions
Demonstrate the following:
SELECT COUNT(*) FROM students;
SELECT AVG(cgpa) FROM students;
SELECT MAX(cgpa) FROM students;
SELECT MIN(cgpa) FROM students;
SELECT SUM(cgpa) FROM students;
GROUP BY
SELECT department, COUNT(*)
FROM students
GROUP BY department;

SELECT department, AVG(cgpa)
FROM students
GROUP BY department;
Submission
•	SQL file containing all queries
•	Screenshot of the database/tables
•	Screenshots of query outputs
•	Short explanation of the aggregate functions used
Learning Outcome: Students learn how real-world college data can be represented in tables and how SQL can be used to retrieve and summarize data.





Day 4 — Competitive Programming
Assignment: LeetCode Practice
Solve the three problems covered during the session. For each problem, submit the required approaches.
1. Two Sum
Submit the brute-force solution and the optimized Hash Map solution.
2. Best Time to Buy and Sell Stock
Submit the brute-force solution and the optimized one-pass solution.
3. Trapping Rain Water
Submit the brute-force solution and the optimized Two Pointer solution.
Submission
•	LeetCode problem links
•	Brute-force solutions
•	Optimized solutions
•	Time and space complexity for each approach
•	A short note explaining why the optimized solution is better
Homework Summary
Day	Assignment	Main Skill
Day 1	Commit to friend's GitHub repository	Git collaboration
Day 2	Personal portfolio website	HTML + CSS + JavaScript
Day 3	College database + SQL queries	SQL + Aggregate Functions
Day 4	Three LeetCode problems	Problem Solving + DSA

