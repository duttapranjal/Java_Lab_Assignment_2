# Java_Lab_Assignment_2
# 🎓 Student Management System 

## 📘 Overview
This project implements a **Student Management System** in **Java** using the core **Object-Oriented Programming (OOP)** principles:
- **Inheritance**
- **Polymorphism**
- **Abstract Classes**
- **Interfaces**
- **Method Overloading** and **Overriding**

The system manages student records such as name, email, roll number, course, marks, and grade. It allows operations like adding, updating, deleting, searching, and viewing all student records.

---

## 🧠 Objective
To design and implement a Student Management System that demonstrates:
- The use of inheritance between classes.
- The application of abstract classes and interfaces.
- Polymorphism through method overriding and overloading.
- Prevention of duplicate student records using data structures.

---

## 🏗️ Class Hierarchy


### 1. **Person (Abstract Class)**
- Fields: `name`, `email`
- Method: `displayInfo()` (abstract)

### 2. **Student (Subclass of Person)**
- Fields: `rollNo`, `course`, `marks`, `grade`
- Methods:
  - `calculateGrade()`
  - `displayInfo()` → overrides abstract method
  - `displayInfo(String researchArea)` → overloaded method

### 3. **RecordActions (Interface)**
Defines methods for CRUD operations:
- `addStudent()`
- `deleteStudent()`
- `updateStudent()`
- `searchStudent()`
- `viewAllStudents()`

### 4. **StudentManager (Implements RecordActions)**
- Uses a `HashMap<Integer, Student>` to store and manage student records.
- Prevents duplicate roll numbers.
- Provides concrete implementations of all CRUD operations.

---

## 💡 Key OOP Concepts Demonstrated

| Concept | Description | Implemented In |
|----------|--------------|----------------|
| **Inheritance** | Student inherits from Person | `class Student extends Person` |
| **Abstraction** | Person is abstract and cannot be instantiated | `abstract class Person` |
| **Interface Implementation** | StudentManager implements RecordActions | `implements RecordActions` |
| **Method Overriding** | Student overrides displayInfo() | `@Override displayInfo()` |
| **Method Overloading** | displayInfo() method with parameter | `displayInfo(String researchArea)` |
| **Polymorphism** | Base class reference for subclass object | `Person p = s1; p.displayInfo();` |

---

## 🧮 Data Types Used
| Field | Data Type |
|--------|------------|
| Name, Email, Course | `String` |
| Roll Number | `int` |
| Marks | `double` |
| Grade | `char` |
| Student Records | `Map<Integer, Student>` |
