# DGL 104 - Research and Reflection Journal

## Week 8: February 25 - March 3

### Mid-Semester Update Review
This week introduced a shift in focus from foundational coding concepts (debugging, testing, documentation, and refactoring) to functional user requirements, design patterns, architectures, and programming paradigms. The main transition in this phase is **moving from MIT App Inventor to a selected programming language for our app development work.

Key insights from the update:
- The shift from visual programming (MIT App Inventor) to coding-based development allows for more flexibility and scalability in projects.
- Understanding functional user requirements ensures that software development is aligned with user needs.
- We will work on documenting coding practices, maintaining project organization, and implementing design patterns in our development process.

---

### User Stories & Functional User Requirements
User stories provide a way to document software requirements from a user’s perspective. They are useful for:
1. **Understanding how a user interacts with a system**.
2. **Defining requirements in a structured and modular manner**.
3. **Helping developers build features that align with user expectations**.

#### **Example User Stories for Google Keep**
- **General User Story:**  
  "As a user, I want to create a new note so that I can quickly capture my thoughts."
- **Specific User Stories:**  
  - "As a user, I can set reminders on my notes so that I don’t forget important tasks."
  - "As a user, I can label my notes for better organization."
  - "As a user, I can archive notes that are no longer needed."

#### **Acceptance Criteria for 'Set Reminder' Feature**
- The reminder button should be clearly visible on each note.
- Users should be able to select a specific date and time for reminders.
- The app should send a notification when the reminder is due.
- Users should be able to view and manage their scheduled reminders.

**Reflection:**
- Writing user stories helped me break down a feature into actionable and understandable parts.
- Acceptance criteria provide a technical foundation for developers to implement the feature correctly.
- This activity made me think like an end-user**, which is crucial for **user-centered design.

---

### Research on a New Programming Language: Processing

#### **What is Processing?**
Processing is a programming language and environment** designed for **creative projects, including:
- **Drawings**
- **Animations**
- **Interactive visualizations**
- **Generative art**

It is widely used by artists, designers, and students because of its simplicity and focus on visual projects. It provides a beginner-friendly way to learn programming through creativity.

#### **Who Uses Processing?**
Processing is popular among:
- Artists and designers who use it for generative art and visual projects.
- Educators and students because it makes learning programming visual and interactive.
- Developers experimenting with creative coding.

#### **Useful Learning Resources**
- **[Official Processing Website](https://processing.org/)**  
  - Contains comprehensive tutorials, examples, and documentation.
  - Provides an IDE specifically for Processing.

- **[The Coding Train YouTube Channel](https://www.youtube.com/c/TheCodingTrain)**  
  - Daniel Shiffman explains how to use Processing in fun and interactive video tutorials.
  - Covers topics like animations, generative art, and simulations.

- **[OpenProcessing](https://openprocessing.org/)**  
  - A platform where users share their Processing projects.
  - Allows me to **view code, modify projects, and experiment interactively**.

#### **Example Code in Processing**
This simple Processing script draws a moving circle:

```java
int x = 50;

void setup() {
  size(400, 200);
}

void draw() {
  background(255);
  fill(0, 102, 153);
  ellipse(x, height/2, 50, 50);
  x = x + 1; // Moves the circle across the screen
}
```

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
```

## Week 10: March 11 - March 17

### Lecture: MV Patterns Overview
This week I focused on MV architectural patterns, which are used to organize applications in a structured way. Unlike design patterns that solve specific object-oriented programming (OOP) problems, MV* patterns help structure an entire application. They promote separation of concerns, making the code easier to manage and scale.

MV patterns are widely used in web and mobile development. Some popular MV* patterns include:

1. Model-View-Controller (MVC)
2. Model-View-ViewModel (MVVM)
3. Model-View-Presenter (MVP)

Understanding these patterns is essential for working with frameworks such as React, Angular, Vue, and mobile development environments like SwiftUI and Jetpack Compose.

### Key Takeaways from the Lecture
- MV patterns improve maintainability by separating data management, presentation, and logic.
- They provide a blueprint for structuring applications, making them scalable and modular.
- Different patterns are used depending on the framework and platform.

---

## Model-View-Controller (MVC)
MVC is a software design pattern that divides an application into three interconnected components:

- Model: Manages the data and business logic.
- View: Handles the user interface and presentation.
- Controller: Processes user inputs and interacts with the Model and View.

### Real-World Applications
- Used in web development frameworks such as Django, Ruby on Rails, and ASP.NET.
- Commonly used in JavaScript frameworks like Angular.
- Helps in separating concerns in large applications.

### Example Code in JavaScript
```javascript
class Model {
    constructor() {
        this.data = "MVC Pattern Example";
    }

    getData() {
        return this.data;
    }
}

class View {
    display(data) {
        console.log(`Displaying: ${data}`);
    }
}

class Controller {
    constructor(model, view) {
        this.model = model;
        this.view = view;
    }

    updateView() {
        const data = this.model.getData();
        this.view.display(data);
    }
}

const model = new Model();
const view = new View();
const controller = new Controller(model, view);

controller.updateView();





