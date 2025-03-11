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
  - Allows me to view code, modify projects, and experiment interactively.

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
