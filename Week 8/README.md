

# **Week 8: February 25 – March 3**  
## **Mid-Semester Update Review**

This week marked a significant transition in our course: we shifted from foundational programming practices like **debugging**, **testing**, **documentation** and **refactoring** toward a deeper focus on **functional user requirements**, **design patterns**, and **software architectures**.

### Key Learnings:

- **Transition from MIT App Inventor to a selected programming language**:  
  This shift means moving from block-based, visual logic to syntax-based coding. I learned that this change brings more **flexibility, custom logic**, and **scalability** to our development work.  
  _Cited from course lecture on Feb 27 and discussion notes during class activity._

- **Functional user requirements**:  
  These help define **what** the system should do from the user's perspective, making the development process more user-centered.  
  _Learned through in-class brainstorming activity on user stories._

- **Design patterns and software architecture principles**:  
  These provide repeatable solutions to common coding challenges and help us structure larger applications more efficiently.  
  _Mentioned in slides from the mid-semester lecture and examples shared in class._

---

## **User Stories & Functional Requirements**

### What I Learned:

**User stories** provide a structured method to define application features from the end-user's point of view. They help in translating abstract features into **concrete, actionable development tasks**.

### Example User Stories (inspired by Google Keep):

- **General Story:**  
  "As a user, I want to create a new note so that I can quickly capture my thoughts."  
  _Learned how to structure these stories during the class discussion on Feb 29._

- **Specific Stories:**  
  - "As a user, I can set reminders on my notes so that I don’t forget important tasks."  
  - "As a user, I can label my notes for better organization."  
  - "As a user, I can archive notes that are no longer needed."  
  _These examples were modeled after the Google Keep interface and analyzed in our group activity._

### Acceptance Criteria Example – 'Set Reminder' Feature:

- A visible reminder button should be available on each note.  
- Users must be able to set a specific date and time.  
- The app must send a notification when the reminder is due.  
- Users can view/edit/delete their reminders.  
  _We drafted acceptance criteria in a class worksheet to define when a feature is “done.”_

#### **Reflection:**

> “Writing user stories helped me break down each feature into smaller, understandable pieces. It made me think like a user instead of just a developer.”  
— _This mindset shift came during our whiteboard brainstorming exercise._

> “The acceptance criteria are like a checklist that ensures the developer builds exactly what the user needs.”  
— _I noticed this especially when reviewing a peer’s user story and identifying missing requirements._

---

## **Research on a New Programming Language: Processing**

This week, I also started exploring **Processing**, a new programming language for me. It’s designed specifically for **visual and interactive** projects, such as digital art, generative design, and animations.

### What is Processing?

Processing is a flexible software sketchbook and a language for learning how to code in a visual context. It is often used by artists, designers, and educators because of its creative focus and beginner-friendly syntax.  
_Cited from [Processing.org](https://processing.org/)._

### Who Uses It?

- Artists for creating **generative artwork**
- Designers for **visual prototypes**
- Educators to teach **programming with visuals**
- Developers for **experimental creative coding**  
_Learned from reading project showcases on [OpenProcessing](https://openprocessing.org/)._

### Resources I Used:

1. **Official Processing Website** – [https://processing.org/](https://processing.org/)  
   - I used their “Getting Started” and “Examples” sections to understand the basics of syntax and functions.

2. **The Coding Train YouTube Channel** – [https://www.youtube.com/c/TheCodingTrain](https://www.youtube.com/c/TheCodingTrain)  
   - Daniel Shiffman’s videos helped me visualize how code creates dynamic graphics. I especially liked his explanations on `setup()` and `draw()` functions.

3. **OpenProcessing** – [https://openprocessing.org/](https://openprocessing.org/)  
   - I explored and modified a few visual art projects to get hands-on experience.

### Example Code:

This script makes a blue circle move across the screen horizontally:

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

### What I Learned from It:

- `setup()` is called once at the beginning. It’s like a starting point.  
- `draw()` runs in a loop, like an animation frame.  
- `ellipse()` draws a circle.  
- I learned that using the `x` variable with `x = x + 1` creates motion.  
  _All of these came from watching Daniel Shiffman’s beginner tutorials._

---

## Final Thoughts on Week 8

- I now understand the **importance of thinking from a user’s perspective** (user stories) and **writing testable criteria** (acceptance criteria).
- The transition from visual programming (MIT App Inventor) to real code (like Java or Processing) is challenging but exciting.
- Learning **Processing** helped me reconnect programming with creativity, and it made coding more enjoyable.

This week laid a strong foundation for the rest of the semester as we move deeper into **user-focused development** and build more **robust applications** using real-world languages and tools.

---