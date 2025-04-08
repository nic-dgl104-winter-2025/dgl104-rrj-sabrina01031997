# **Week 11: March 18 – March 24**  
**Topic:** Object-Oriented Programming (OOP) and Its Role in Modern Development

---

## **Introduction**

This week’s focus was on **Object-Oriented Programming (OOP)** — a foundational paradigm in modern software development. We explored the four main principles of OOP: **Encapsulation, Abstraction, Inheritance,** and **Polymorphism**. These were introduced through Java and JavaScript code examples, supported by two instructional videos and class lectures.

Additionally, we continued contributing to our group coding project and revisited our open-source contribution work. Understanding OOP is essential as we move deeper into building scalable and maintainable applications, especially in group-based and real-world projects.

---

## **Core Concepts of OOP**

### 1. **Encapsulation**

Encapsulation restricts direct access to an object’s internal data, allowing control through methods. This protects data integrity and improves security.

```java
class BankAccount {
    private double balance;

    public BankAccount(double balance) {
        this.balance = balance;
    }

    public void deposit(double amount) {
        if (amount > 0) balance += amount;
    }

    public double getBalance() {
        return balance;
    }
}
```

**What I learned:**  
Encapsulation hides internal object state and forces access through well-defined interfaces. This makes programs more robust and easier to debug.

**Reference:**  
YouTube – [Object-Oriented Programming – Part 1](https://youtu.be/hdVYcOgNKfc)

---

### 2. **Abstraction**

Abstraction hides unnecessary implementation details and shows only what’s relevant to the user.

```java
abstract class Animal {
    abstract void makeSound();

    void sleep() {
        System.out.println("Sleeping...");
    }
}

class Dog extends Animal {
    void makeSound() {
        System.out.println("Woof!");
    }
}
```

**What I learned:**  
Using abstract classes and methods, we can define base behavior and allow each subclass to implement its own version.

**Reference:**  
YouTube – [Object-Oriented Programming – Part 2](https://youtu.be/jzP2sw3I1nc)

---

### 3. **Inheritance**

Inheritance allows one class to use properties and methods of another, promoting code reuse and logical hierarchy.

```java
class Vehicle {
    void honk() {
        System.out.println("Beep!");
    }
}

class Car extends Vehicle {
    void displayModel() {
        System.out.println("Model: Camry");
    }
}
```

**What I learned:**  
Instead of repeating code, shared functionality can be placed in a parent class. This streamlines the development process and ensures consistency across classes.

**Reference:**  
Lecture – Week 11 notes by Ashley Blacquiere

---

### 4. **Polymorphism**

Polymorphism allows methods to behave differently based on the object that’s calling them.

```java
class Animal {
    void makeSound() {
        System.out.println("Some sound");
    }
}

class Dog extends Animal {
    void makeSound() {
        System.out.println("Woof!");
    }
}

public class Main {
    public static void main(String[] args) {
        Animal myAnimal = new Dog();
        myAnimal.makeSound();  // Outputs "Woof!"
    }
}
```

**What I learned:**  
Polymorphism supports flexibility and extensibility. It helps us write general code that can work with any object type that extends a base class.

**Reference:**  
YouTube – [OOP – Abstraction and Polymorphism](https://youtu.be/jzP2sw3I1nc)

---

## **How I Plan to Use OOP in Our Group Project**

We are building a **Task Management System** using **PHP and JavaScript**. Both languages support OOP (PHP natively since version 5, and JavaScript through ES6 class syntax). We're implementing user roles (Admin, Team Lead, User), and OOP will help us separate logic cleanly.

### Planned Structure:

- **Encapsulation:** Private properties like user credentials and controlled access via getter/setter functions.
- **Abstraction:** Base classes for users and tasks with abstract or shared methods like `assignTask()`.
- **Inheritance:** `User` class extended by `Admin`, `TeamLead`, and `RegularUser` classes.
- **Polymorphism:** Methods like `accessDashboard()` will behave differently depending on the user role.

**Example in PHP:**

```php
abstract class User {
    protected $name;

    public function __construct($name) {
        $this->name = $name;
    }

    abstract public function accessDashboard();
}

class Admin extends User {
    public function accessDashboard() {
        echo "Welcome Admin, {$this->name}";
    }
}
```

This approach improves maintainability and will make our app easier to expand as we add more features.

---

## **Follow-Up Reflection**

### Is my language OOP-capable?

Yes. We're using both PHP and JavaScript, and both are **multi-paradigm languages** that support object-oriented programming.

- **PHP:** Fully OOP-capable — supports classes, inheritance, interfaces, and access modifiers.
- **JavaScript:** Uses prototypal inheritance and ES6 class syntax — also supports functional programming.

**Reference:**  
Wikipedia – [List of Programming Languages by Paradigm](https://en.wikipedia.org/wiki/List_of_programming_languages_by_type)

---

### What was the hardest challenge this week?

The most difficult part was understanding how **abstraction** fits into our real project. While I understood the concept, figuring out what should go into a base class versus a child class took time. Watching the videos a second time and sketching out a class diagram with my group helped us decide where each method belonged.

---

## **Conclusion**

Object-Oriented Programming has given me a more structured way to approach software development. With encapsulation, inheritance, and abstraction, our team can write code that is easier to manage, reuse, and scale. As we continue our project, we plan to implement these principles to enhance performance and readability.

Understanding OOP now makes me more confident in handling backend logic and working with frameworks that rely on structured class-based systems.

---

## **References**

1. Blacquiere, Ashley. *Week 11 Lecture – Object-Oriented Programming*. North Island College, DGL 104. Modified by Dibya Prokash Sarkar.  
2. YouTube – [Object-Oriented Programming – Part 1](https://youtu.be/hdVYcOgNKfc)  
3. YouTube – [Object-Oriented Programming – Part 2](https://youtu.be/jzP2sw3I1nc)  
4. Wikipedia – [PHP](https://en.wikipedia.org/wiki/PHP)  
5. Wikipedia – [List of Programming Languages by Type](https://en.wikipedia.org/wiki/List_of_programming_languages_by_type)  

---
