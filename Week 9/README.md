# Week 9: March 4 – March 10  
**Primary Focus: Design Patterns, Open Source Contribution, and Project Planning**

## Introduction

This week’s content introduced several important concepts that expand beyond basic syntax and debugging. We focused on understanding and applying **design patterns**, exploring how to **contribute to open source projects**, and continuing the collaborative development of our **group application project**. These areas are essential in preparing us for real-world development environments, where scalable and maintainable code is key.

---

## Design Patterns

> "Design patterns are reusable fragments of code that provide a solution to a specific - and typically well-understood - coding problem."  
> — Week 9 Lecture Notes (Ashley Blacquiere)

From this, I understood that design patterns are not copy-paste solutions. They are flexible templates that help developers solve common programming problems in a more organized and understandable way. The patterns I explored this week came from the Refactoring Guru website and Addy Osmani's *Learning JavaScript Design Patterns*. The YouTube lecture by Ashley Blacquiere also provided clear Java and Kotlin examples that helped me see how the same pattern can be used across multiple languages.

### 1. Singleton Pattern
- **Purpose:** Ensures that only one instance of a class exists and provides a global access point to it.
- **Use Case:** Database connection handling.
- **Resource:** Refactoring Guru – Singleton Pattern
- **Lecture Reference:** Explained around 2:14 in the YouTube lecture

```java
public class Database {
    private static Database instance;

    private Database() {}

    public static Database getInstance() {
        if (instance == null) {
            instance = new Database();
        }
        return instance;
    }
}
```

### 2. Factory Pattern
- **Purpose:** Creates objects without specifying the exact class.
- **Use Case:** UI component rendering based on user input.
- **Resource:** Refactoring Guru – Factory Method Pattern
- **Lecture Reference:** Discussed around 4:48 in the YouTube lecture

```javascript
function PizzaFactory(type) {
    if (type === 'cheese') return new CheesePizza();
    if (type === 'veggie') return new VeggiePizza();
}
```

### 3. Observer Pattern
- **Purpose:** Lets one object notify others about state changes.
- **Use Case:** Notification systems or live updates.
- **Resource:** Addy Osmani’s book on JavaScript Design Patterns
- **Lecture Reference:** Demonstrated around 7:09 in the video

```javascript
class NewsFeed {
    constructor() {
        this.subscribers = [];
    }

    subscribe(user) {
        this.subscribers.push(user);
    }

    notify(news) {
        this.subscribers.forEach(user => user.update(news));
    }
}
```

### 4. Strategy Pattern
- **Purpose:** Allows selection of algorithms at runtime.
- **Use Case:** Payment systems supporting multiple options.
- **Resource:** Refactoring Guru – Strategy Pattern
- **Lecture Reference:** Covered around 10:12 in the lecture

```java
interface PaymentStrategy {
    void pay(int amount);
}

class CreditCardPayment implements PaymentStrategy {
    public void pay(int amount) {
        System.out.println("Paid " + amount + " with credit card");
    }
}
```

### Reflection on Design Patterns
The lecture and reading helped me understand that design patterns are not tied to a specific language. They are architectural tools that help write cleaner, more maintainable code. Understanding their structure and purpose allows developers to apply them across different projects regardless of the tech stack.

---

## Open Source Contribution

I read GitHub's official guide, [How to Contribute to Open Source](https://opensource.guide/how-to-contribute/), and it significantly changed how I view open source. I had assumed only experienced developers could contribute, but this guide explained that contributions can range from writing documentation and fixing typos to reporting bugs and reviewing pull requests.

### Key Insights
- Contributions don't have to be code-based.
- Communication, clarity, and documentation are equally valued.
- The guide encourages trying small fixes and progressing gradually.

### My Preferred Ways to Contribute
1. **Improving documentation:** I enjoy writing clearly and think this is a good way to start.
2. **UI-related suggestions:** I often notice accessibility or design issues that I can help refine.
3. **Beginner-friendly issues:** Looking for "good first issues" helped me filter approachable tasks.

### Identified Issue
- **Repository:** [Public APIs](https://github.com/public-apis/public-apis)
- **Issue:** Fixing a broken API link in the README
- **Reason:** It's a low-barrier, non-code task that still improves project quality

This was shared with my peers and instructor on Slack, as part of the week's activities.

---

## Application Development Coding Project

Our group finalized the concept for our **Task Management App**. We've created the GitHub repository and started working collaboratively. The app will include three user roles:
- **Admin**
- **Team Lead**
- **Regular User**

Each role will have specific permissions. We also discussed integrating at least two design patterns into our project:
- **Singleton Pattern** for database connection (in PHP)
- **Factory Pattern** for creating task objects based on user role and input

We are using PHP, JavaScript, Bootstrap, and MySQL. The language choice still feels right based on our current skill set and project scope.

### Development Plan
- We’ve created a feature breakdown in GitHub Projects.
- Weekly milestones are set up.
- Everyone in the group is assigned different sections of the app (e.g., authentication, dashboard, task flow).

---

## Follow-Up Reflection Questions

**Is the programming language I chose last week still the right one?**  
Yes. PHP and JavaScript are suitable for this web-based task management system. The structure and backend features we need can be efficiently implemented in PHP.

**What is my development plan moving forward?**  
- Finalize the login/authentication system next week.
- Begin role-based dashboard development.
- Integrate design pattern logic for task creation and role assignment.

---

## Final Reflection

This week emphasized real-world software engineering techniques. Design patterns gave me tools to solve programming problems efficiently and in a reusable way. The open source activity helped me realize that I can contribute meaningfully even as a student. Lastly, collaborating with my team on the app made me appreciate the planning and structure needed in development.

> “Patterns aren’t just reusable code – they’re reusable thinking.”  
This idea stuck with me throughout the week and will definitely shape how I approach development in future courses and projects.

---

