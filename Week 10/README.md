# **Week 10: March 11 – March 17**  
**Topic:** MV* Patterns and External Community Contributions

---

## **Introduction**

This week in DGL 104, we moved from internal design patterns (like Singleton and Observer from Week 9) into broader **architectural patterns** — specifically **MV*** structures. We also focused on the continuation of our **Community Code Project**, which required analyzing contribution guidelines and beginning actual contributions to an external open-source repository.

The video resources provided for both MV* concepts and GitHub processes were very helpful in bridging theory with real-world development.

---

## **Understanding MV* Patterns**

### What are MV* Patterns?

MV* patterns, like **MVC (Model-View-Controller)** and **MVVM (Model-View-ViewModel)**, describe how to **structure applications** into separate components — making the application easier to manage, test, and scale. Unlike smaller design patterns, MV* patterns structure **entire applications**.

> “MV* patterns are typically thought of as architectural patterns, distinct from design patterns like Singleton or Observer.”  
> — Week 10 Lecture Notes

They provide **clear separation of concerns**:
- **Model** handles the data and business logic
- **View** is the user interface
- **Controller or ViewModel** mediates between the two

---

### MVC (Model-View-Controller)

MVC is one of the oldest and most commonly used architectural patterns, especially in **web development frameworks** like Ruby on Rails, Laravel (PHP), and ASP.NET.

- **Model** – Manages the data (e.g., database).
- **View** – What the user sees (HTML/CSS/JS).
- **Controller** – Handles user actions and logic.

**Example (PHP MVC concept):**

```php
// Controller
class TaskController {
    public function showTasks() {
        $tasks = TaskModel::getAll();
        include 'views/taskList.php';
    }
}
```

This example shows how logic is separated from view rendering, keeping code organized.

---

### MVVM (Model-View-ViewModel)

MVVM is mostly used in **modern mobile frameworks**, such as SwiftUI (iOS) and Jetpack Compose (Android). Unlike MVC, MVVM adds a **ViewModel**, which acts as an intermediary between the UI and the model.

- **Model** – Data layer.
- **ViewModel** – Manages UI-related data and logic.
- **View** – Reflects data and reacts to changes.

**Video Reference:**  
Ashley Blacquiere’s explanation on MVVM using SwiftUI and Kotlin Jetpack Compose helped clarify how MVVM supports **two-way data binding** and reactive updates.  
([Link to MVVM lecture](https://youtu.be/ZkeX4NLkhms))

---

### Key Learning:

> “MV* patterns aren’t just ways to organize files; they are strategies for managing complexity in large-scale applications.”  
> — Video: [MV* Concepts & Implementation](https://youtu.be/PkvOL-hWnGs)

---

## **External Community Contributions**

### Step 1: Assessing Community Guidelines

I chose to contribute to the **Public APIs** GitHub repository.

- **Link:** [https://github.com/public-apis/public-apis](https://github.com/public-apis/public-apis)
- I reviewed their **README.md** and **CONTRIBUTING.md** files thoroughly.
- They require contributors to:
  - Submit public and free APIs only.
  - Follow alphabetical order when adding entries.
  - Use a concise description (under 100 characters).

I documented this process in my personal CONTRIBUTING.md file, as required.

---

### Step 2: Forking and Setting Up the Project

Following Ashley’s video walkthrough ([GitHub Fork & PR Guide](https://youtu.be/o1M5hFLjcXw)), I:

1. Forked the repository to my GitHub account.
2. Cloned the fork locally.
3. Created a branch `add-weather-api`.
4. Added a new weather API (free and publicly available).
5. Committed the changes with clear messages.
6. Pushed the branch and opened a pull request.

This process helped me become more comfortable with version control in collaborative environments.

---

### Step 3: Summary Posted on Slack

I shared the following:

> “The Public APIs repo has well-written contributing guidelines. They clearly define expectations for new contributors and follow a structured pull request system. This made it easier for me to follow through with my addition.”

---

## **Follow-Up Reflection**

### What was the hardest part this week?

Understanding the **differences between MVC and MVVM** was initially challenging. At first, I assumed they were variations of the same idea. Watching videos like:

- [MVVM Explained Simply](https://youtu.be/cq7qi2ehEKE)
- [MVC vs MVVM Deep Dive](https://youtu.be/ZlysOUJs2_I)

helped me realize that **MVC uses user-driven control flow**, while **MVVM uses data binding and reactive UI updates**.

I overcame this by reviewing class materials, drawing diagrams, and re-watching key video segments.

---

## **Conclusion**

This week gave me two important tools:

1. A clear understanding of **application architecture** (MV* patterns).
2. Practical experience in the **GitHub open-source workflow**.

It’s becoming clear how design patterns and architectural structures play into long-term software success. Contributing to a real-world repo, even in a small way, gave me confidence and reinforced the skills we’ve been building.

---