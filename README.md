<div align="center">
# 🎓 Student Course Management System
**COS 201 Laboratory Assessment — Object-Oriented Programming in Java**

[![Java](https://shields.io)](https://oracle.com)
[![IntelliJ IDEA](https://shields.io)](https://jetbrains.com)
[![Course](https://shields.io)](#)
[![Status](https://shields.io)](#)

*A console-driven Java application demonstrating Object-Oriented Programming principles, custom exception handling, and persistent file storage for academic course administration.*

[Features](#-key-features) • [Architecture](#-project-architecture) • [Getting Started](#-getting-started) • [Usage](#-usage-guide) • [Screenshots](#-screenshots)

</div>

---

## 📖 Overview

The **Student Course Management System** is a Java-based administrative utility developed for the **COS 201 Lab Assessment**. It enables users to create, manage, validate, and persist student course records through an interactive Command-Line Interface (CLI), eliminating volatile in-memory state by synchronizing data directly with local flat-file storage (`courses.txt`).

---

## ✨ Key Features

* **Course Lifecycle Management:** Add, view, update, and remove academic courses dynamically via `CourseManager`.
* **Custom Exception Handling:** Implements `InvalidCourseException` to catch and gracefully handle malformed course codes, invalid credit units, or duplicate entries without crashing the JVM.
* **Persistent File I/O:** Automatically reads from and writes to `courses.txt` so course records survive across application restarts.
* **Encapsulated Domain Modeling:** Clean separation between data representation (`Course`), business logic (`CourseManager`), validation (`InvalidCourseException`), and user interaction (`Main`).

---

## 🏗️ Project Architecture

```text
STUDENT-COURSE-MANAGEMENT-SYSTEM-COS-201-lab-assessment/
├── Screenshots/                  # Execution outputs and CLI demonstration captures
├── Course.java                   # Data model representing a Course entity (code, title, units, etc.)
├── CourseManager.java            # Core controller handling CRUD operations & courses.txt File I/O
├── InvalidCourseException.java   # Custom checked/unchecked exception for domain validation
├── Main.java                     # Application entry point and interactive CLI menu loop
├── courses.txt                   # Flat-file database storing persisted course records
└── new java lab ass.iml          # IntelliJ IDEA module configuration
```

### Class Responsibilities

| File | Role | Description |
| :--- | :--- | :--- |
| `Main.java` | **Entry Point & UI** | Renders the CLI menu, captures `Scanner` input, and routes commands to the manager. |
| `Course.java` | **Model / Entity** | Encapsulates course attributes with getters, setters, and formatted `toString()` output. |
| `CourseManager.java` | **Service / Logic** | Manages the collection of `Course` objects and handles `BufferedReader`/`FileWriter` persistence. |
| `InvalidCourseException.java` | **Error Handling** | Custom `Exception` subclass triggered when course constraints are violated. |
| `courses.txt` | **Storage** | Stores serialized course records on disk. |

---

## 🚀 Getting Started

### Prerequisites
* **Java Development Kit (JDK):** Version 8 or higher installed (`java -version`).
* **IDE (Optional):** IntelliJ IDEA, Eclipse, or VS Code with Java Extension Pack.

### Installation & Execution

1. **Clone the repository**
   ```bash
   git clone https://github.com
   cd STUDENT-COURSE-MANAGEMENT-SYSTEM-COS-201-lab-assessment
   ```

2. **Compile the Java source files**
   ```bash
   javac *.java
   ```

3. **Run the application**
   ```bash
   java Main
   ```

> **Note for IntelliJ IDEA users:** Open the project folder directly in IntelliJ IDEA, ensure your Project SDK is configured under `File > Project Structure`, and run `Main.main()`.

---

## 💻 Usage Guide

Once running, follow the on-screen CLI prompts to interact with the system:

```text
=========================================
   STUDENT COURSE MANAGEMENT SYSTEM
=========================================
1. Add Course
2. View All Courses
3. Search Course by Code
4. Compute Total Units
5. Save to File
6. Load from File
7. Exit Program
=========================================
Enter your choice:


## 📸 Screenshots

Visual proof of compilation, CRUD operations, exception handling, and `courses.txt` persistence can be found inside the [`Screenshots/`](./Screenshots) directory.


| Main Menu | Adding a Course | Exception Handling |
| :---: | :---: | :---: |
| ![Menu](./Screenshots/menu.png) | ![Add](./Screenshots/add.png) | ![Error](./Screenshots/error.png) |
-->

---

## 🧹 Repository Hygiene Tip
Notice that compiled `.class` files and `.idea/` workspace files are currently tracked in the root directory. For an even cleaner GitHub portfolio, consider adding a `.gitignore` file containing:
```gitignore
*.class
.idea/
out/
```

---

## 👨‍💻 Author

**Isaiah Talabi**
* GitHub: [@Isaiah-Talabi](https://github.com/Isaiah-Talabi)
* Course: COS 201 — Computer Programming / OOP Lab Assessment
