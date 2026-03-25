# After TCS NQT — Interview Preparation Guide

## 🎯 What Happens After Clearing NQT?

1. **Results announced** (usually within 2-4 weeks)
2. **Profile assigned** (Ninja / Digital / Prime)
3. **Interview call** (date, time, location)
4. **Technical interview** (45-60 min)
5. **HR interview** (15-30 min)
6. **Offer letter** (within 1-2 weeks after interview)

---

## 💻 Technical Interview — What to Expect

### For Ninja Profile
- Basic DSA (arrays, strings)
- OOPs concepts
- Any one language basics (C/Java/Python)
- Database basics (SQL queries)
- Simple coding problems

### For Digital Profile
- Intermediate DSA (sorting, searching, linked lists)
- OOPs + design patterns
- Database (SQL joins, normalization)
- Web technologies (HTML/CSS/JS basics)
- Framework knowledge (React/Node/Spring)
- 1-2 coding problems

### For Prime Profile
- Advanced DSA (trees, graphs, DP)
- System design basics
- Database design
- Multiple coding problems
- Project discussion (deep dive)

---

## 📚 Common Technical Questions

### OOPs (Object-Oriented Programming)

**Q: What are the 4 pillars of OOPs?**
1. **Encapsulation** — Bundling data and methods together, hiding internal details
2. **Abstraction** — Showing only essential features, hiding complexity
3. **Inheritance** — Child class inherits properties from parent class
4. **Polymorphism** — Same method behaves differently (overloading/overriding)

**Q: Difference between Abstraction and Encapsulation?**
- Abstraction: Hides complexity (what to show)
- Encapsulation: Hides data (how to protect)

**Q: What is polymorphism? Give examples.**
- **Compile-time**: Method overloading (same name, different parameters)
- **Runtime**: Method overriding (child class redefines parent method)

**Q: What is an abstract class vs interface?**
- Abstract class: Can have both abstract and concrete methods
- Interface: Only abstract methods (in Java), all public

### Database / SQL

**Q: What is normalization?**
- Organizing data to reduce redundancy
- 1NF: Atomic values only
- 2NF: No partial dependencies
- 3NF: No transitive dependencies

**Q: Difference between WHERE and HAVING?**
- WHERE: Filters rows before grouping
- HAVING: Filters groups after GROUP BY

**Q: Write a SQL query to find the second highest salary.**
```sql
SELECT MAX(salary) FROM employees 
WHERE salary < (SELECT MAX(salary) FROM employees);

-- OR using LIMIT
SELECT salary FROM employees 
ORDER BY salary DESC LIMIT 1 OFFSET 1;
```

**Q: Types of JOINs?**
- INNER JOIN: Matching rows from both tables
- LEFT JOIN: All from left + matching from right
- RIGHT JOIN: All from right + matching from left
- FULL JOIN: All from both tables

### Data Structures

**Q: Array vs Linked List?**
| Feature | Array | Linked List |
|---------|-------|-------------|
| Memory | Contiguous | Scattered |
| Access | O(1) by index | O(n) |
| Insert | O(n) | O(1) at head |
| Size | Fixed | Dynamic |

**Q: Stack vs Queue?**
- Stack: LIFO (Last In First Out) — like a stack of plates
- Queue: FIFO (First In First Out) — like a line at store

**Q: What is a HashMap? How does it work?**
- Key-value pair storage
- Uses hashing function to compute index
- Average O(1) for insert/search/delete
- Collision handling: chaining or open addressing

### Algorithms

**Q: What is time complexity?**
- Measure of how runtime grows with input size
- O(1) < O(log n) < O(n) < O(n log n) < O(n²) < O(2ⁿ)

**Q: Binary Search — how does it work?**
- Works on sorted array
- Compares target with middle element
- Eliminates half the search space each time
- Time: O(log n)

**Q: What is recursion? When to use it?**
- Function calling itself
- Use when: problem can be broken into similar subproblems
- Need base case to stop
- Example: factorial, fibonacci, tree traversal

---

## 🗣️ HR Interview — Common Questions

### About You
1. **Tell me about yourself.**
   → Name, education, skills, projects, why TCS

2. **Why TCS?**
   → Great learning environment, global exposure, growth opportunities

3. **Where do you see yourself in 5 years?**
   → Senior developer/team lead, contributing to innovative projects

4. **What are your strengths and weaknesses?**
   → Strengths: Quick learner, problem-solver, team player
   → Weakness: Sometimes perfectionist (but working on it)

5. **Why should we hire you?**
   → Strong technical skills, passion for learning, adaptability

### Situational
6. **Tell me about a challenging project.**
   → Describe the project, challenge, solution, and outcome

7. **How do you handle pressure?**
   → Prioritize tasks, break problems into smaller parts, stay calm

8. **Do you prefer working alone or in a team?**
   → Both — independent work for coding, team for complex projects

### Technical + HR
9. **Explain your resume project.**
   → Be able to explain ANY project on your resume in detail

10. **What technologies are you learning?**
    → Mention something relevant (cloud, ML, full-stack, etc.)

---

## 💼 Your Resume Projects — Be Ready to Explain

### Smith Works (Full-Stack Marketplace)
**Be ready to explain:**
- How did you handle real-time chat with Socket.IO?
- How did you implement JWT authentication?
- What's the database schema?
- How did you deploy on AWS EC2?
- What challenges did you face?

### TopX AI Resume Analyzer
**Be ready to explain:**
- How does the NLP skill extraction work?
- What ML model did you use? Why RandomForest?
- How did you handle PDF parsing?
- What's the accuracy of company matching?

### PIXS (macOS App)
**Be ready to explain:**
- Why SwiftUI + AppKit?
- How did you integrate Gemini API?
- How do notifications work?
- What was the hardest part?

---

## 🎯 Interview Tips

### Before Interview
- [ ] Review ALL resume projects
- [ ] Practice explaining projects in 2 minutes
- [ ] Review OOPs concepts
- [ ] Practice 5 basic SQL queries
- [ ] Practice coding on paper/whiteboard
- [ ] Research TCS (recent news, projects, values)

### During Interview
- [ ] Dress formally (even for virtual)
- [ ] Be confident, maintain eye contact
- [ ] If you don't know something, say "I'm not sure, but I think..."
- [ ] Think aloud while solving problems
- [ ] Ask questions about the role/company

### Coding in Interview
- [ ] Clarify the problem first
- [ ] Discuss approach before coding
- [ ] Start with brute force, then optimize
- [ ] Test with examples
- [ ] Handle edge cases

---

## 📋 Quick Revision Before Interview

### Must-Know Topics
1. OOPs (4 pillars, examples)
2. SQL (JOINs, GROUP BY, subqueries)
3. Array/List operations
4. String operations
5. Sorting algorithms (at least 1)
6. Time complexity basics
7. Your resume projects (all details)

### Good to Know
8. Linked List basics
9. Stack & Queue
10. HashMap
11. Basic recursion
12. REST API basics
13. HTTP methods (GET, POST, PUT, DELETE)

### For Digital/Prime
14. Trees basics
15. Graph basics
16. Dynamic Programming
17. System design basics
18. Design patterns (Singleton, Factory)
