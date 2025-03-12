## Week 9: March 4 - March 10

### Lecture: Design Patterns Overview
This week, I focused on design patterns, which provide reusable solutions for common coding problems. Design patterns are not implementations but rather templates that help developers structure their code effectively. They improve code maintainability, scalability, and readability by following well-established programming best practices.

### Key Concepts Learned:
1. Design patterns encapsulate common solutions to software design problems.
2. They help in standardizing development practices.
3. Using design patterns makes it easier for developers to understand and modify code.
4. They are language-independent and can be applied across Java, JavaScript, Python, and other OOP-based languages.
5. There are three main categories of design patterns:
   - Creational Patterns – Control how objects are created.
   - Structural Patterns – Define relationships between objects.
   - Behavioral Patterns – Manage communication between objects.

---

## Research on Four Key Design Patterns

### 1️⃣ Singleton Pattern
**Definition:**  
A Singleton Pattern ensures that a class has only one instance and provides a global point of access to it.

#### Why is it used?
- Ensures controlled access to a shared resource.
- Prevents unnecessary object duplication, which saves memory.
- Useful for managing global application state.

#### **Real-World Applications**
- Database connections – Prevents redundant connections that consume memory.
- Logging mechanisms – Ensures a centralized logging instance.
- Configurations settings – Stores global settings accessible throughout the application.

#### **Example in JavaScript**
```javascript
class Singleton {
    constructor() {
        if (!Singleton.instance) {
            Singleton.instance = this;
        }
        return Singleton.instance;
    }

    getInstance() {
        return this;
    }
}

// Usage
const instance1 = new Singleton();
const instance2 = new Singleton();

console.log(instance1 === instance2); // Output: true (same instance)
