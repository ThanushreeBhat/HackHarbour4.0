# Day 4 - Introduction to Competitive Programming

Competitive Programming (CP) is a mind sport where programmers solve algorithmic and logical problems under constraints (time, memory). It tests your problem-solving skills, algorithmic knowledge, and coding speed.

---

## 1. Time & Space Complexity (Big O Notation)
To write code that runs fast and uses minimal memory, we analyze it using **Big O notation**.

### Time Complexity
Represents how the running time of an algorithm grows relative to the size of the input ($N$).
* **$O(1)$ - Constant Time:** Execution time is independent of input size (e.g., accessing an array element by index).
* **$O(N)$ - Linear Time:** Execution time grows proportionally to input size (e.g., iterating through a list of size $N$).
* **$O(N^2)$ - Quadratic Time:** Execution time grows quadratically (e.g., nested loops, bubble sort).
* **$O(\log N)$ - Logarithmic Time:** Execution time halves at each step (e.g., binary search).

### Space Complexity
Represents the amount of extra memory an algorithm needs relative to the size of the input.

---

## 2. Core Data Structures for Competitive Programming
Understanding how to organize data efficiently is key to solving complex problems. In this course, we refer to the C implementation of these data structures:

* **Arrays:** A contiguous block of memory storing elements of the same type. Allows $O(1)$ lookup but has a fixed size.
* **Linked Lists:** Nodes linked via pointers. Allows dynamic sizing. Refer to the implementation guide: [C Linked Lists](../C/day7.md).
* **Stacks:** Last-In, First-Out (LIFO) data structure. Refer to the implementation guide: [C Data Structures (Stacks & Queues)](../C/day6.md).
* **Queues:** First-In, First-Out (FIFO) data structure. Refer to the implementation guide: [C Data Structures (Stacks & Queues)](../C/day6.md).

---

## 3. Recommended Coding Platforms
Get started by creating accounts and practicing on these platforms:
1. **LeetCode:** Best for interview preparation and learning specific data structure patterns.
2. **HackerRank:** Excellent for learning programming language syntax and basic algorithms.
3. **CodeChef / Codeforces:** Best for competitive contests and advanced problem-solving.

---

## 4. Starter Practice Problems & Logic

### Problem 1: Two Sum

Problem: Given an array of integers nums and an integer target, return the indices of the two numbers such that they add up to target.

* **Brute Force Approach ($O(N^2)$):** Use nested loops to check every possible pair.
* **Optimal Approach ($O(N)$):** Use a Hash Map to store numbers already seen and check whether the complement (target - nums[i]) exists.
### Problem 2: Best Time to Buy and Sell Stock

Problem: You are given an array prices where prices[i] represents the price of a stock on the ith day. Choose one day to buy and a different day in the future to sell to maximize your profit.

* **Brute Force Approach ($O(N^2)$):** Try every possible buying day and every later selling day, calculate the profit, and keep track of the maximum profit.
* **Optimal Approach ($O(N)$):** Keep track of the minimum price seen so far while traversing the array. For each price, calculate the possible profit and update the maximum profit.
### Problem 3: Trapping Rain Water

Problem: Given an array of non-negative integers representing an elevation map where the width of each bar is 1, calculate how much water can be trapped after raining.

* **Brute Force Approach ($O(N^2)$):** For every position, find the maximum height on the left and right and calculate the water that can be stored at that position.
* **Optimal Approach — Two Pointers ($O(N)$):** Use two pointers, left and right, along with leftMax and rightMax to calculate trapped water while traversing the array only once.Space Complexity: $O(1)$ extra space.