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
