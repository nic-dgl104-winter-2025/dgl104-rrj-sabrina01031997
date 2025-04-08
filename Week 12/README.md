# **Week 12: March 25 – March 31**  
**Topic:** Functional Programming & Final Group Project Development

---

## **Introduction**

This week we explored the final programming paradigm of the semester — **Functional Programming (FP)**. Unlike object-oriented programming (OOP), which focuses on objects and states, functional programming emphasizes **pure functions**, **immutability**, and **function composition**. We also reviewed modern programming methods like `map()`, `filter()`, and `reduce()`, which are available in many popular languages including JavaScript, Java, and Swift.

The lecture and video made it clear that functional programming is no longer limited to academic labs; it's widely used in real-world development, especially in **collection processing**, **data transformation**, and **API logic**.

---

## **Understanding the Functional Paradigm**

### What is Functional Programming?

Functional programming is a paradigm that treats computation as the **evaluation of mathematical functions** and **avoids changing state** or using mutable data. Core principles include:

- **Pure functions:** Functions return the same output for the same input and do not alter external states.
- **Immutability:** Data cannot be modified after it is created.
- **Higher-order functions:** Functions that can take other functions as arguments or return them as results.

> “Functional programming offers clean, predictable logic by avoiding side effects.”  
> — Week 12 Lecture Notes by Ashley Blacquiere

---

### Functional Tools in JavaScript

In JavaScript, functional programming methods are commonly applied to arrays using:

#### `map()`

Transforms each element in an array.

```javascript
const numbers = [1, 2, 3];
const doubled = numbers.map(num => num * 2);
console.log(doubled); // [2, 4, 6]
```

#### `filter()`

Filters elements that meet a specific condition.

```javascript
const nums = [1, 2, 3, 4];
const even = nums.filter(n => n % 2 === 0);
console.log(even); // [2, 4]
```

#### `reduce()`

Reduces an array to a single value.

```javascript
const values = [1, 2, 3, 4];
const sum = values.reduce((acc, cur) => acc + cur, 0);
console.log(sum); // 10
```

These methods make the code **cleaner**, **shorter**, and often easier to reason about compared to traditional `for` loops.

> "I strongly encourage you to consider adopting these types of methods where appropriate..."  
> — Ashley Blacquiere, [Week 12 Lecture](https://youtu.be/_uXZ8HvHH7o)

---

## **How Functional Programming Helps in Our Project**

We are using **JavaScript and PHP** in our **Task Management App**, and functional tools have already helped simplify our JavaScript logic.

### In JavaScript:

We use `filter()` to show tasks by status:

```javascript
const tasks = [
  { title: "Design UI", status: "in-progress" },
  { title: "Fix bug", status: "done" },
];

const doneTasks = tasks.filter(task => task.status === "done");
```

### In PHP:

Although PHP is not purely functional, it supports higher-order functions using array functions like `array_map`, `array_filter`, and `array_reduce`.

```php
$numbers = [1, 2, 3, 4];

$doubled = array_map(fn($n) => $n * 2, $numbers);
$even = array_filter($numbers, fn($n) => $n % 2 === 0);
$sum = array_reduce($numbers, fn($carry, $item) => $carry + $item);
```

Functional techniques like these help avoid unnecessary variables and loops.

---

## **Final Community Code Project Progress**

This week, we focused on cleaning up code, writing documentation, and organizing our pull requests.

### Our tasks included:

- Submitting a pull request to our **pattern-library**.
- Using `filter()` and `map()` to improve dashboard logic.
- Cleaning up repeated code using helper functions.
- Finalizing our **CONTRIBUTING.md** with commit history, feature descriptions, and issue references.

---

## **Follow-Up Reflection**

### What is the difference between OOP and Functional Programming?

| Concept                  | OOP                                | Functional Programming                     |
|--------------------------|-------------------------------------|---------------------------------------------|
| Data                    | Objects with state                  | Immutable values                           |
| Core Unit               | Objects + Methods                   | Pure functions                             |
| Focus                   | Behavior through class interaction  | Function chaining + transformations        |
| State management        | Maintains and changes internal state| No state changes (pure, stateless logic)   |
| Reusability             | Inheritance and interfaces          | Function composition and higher-order funcs|

### Which is more useful in our project?

Both paradigms are useful:
- **OOP** helped us structure our PHP backend and user roles.
- **Functional programming** improved our frontend logic, especially with task filtering and rendering.

---

## **Conclusion**

This final week before submission reminded me of how flexible programming can be. Functional programming, which once seemed abstract, now feels **practical** and **powerful**, especially when working with arrays or UI-based features. Using `map`, `filter`, and `reduce` has not only made our code cleaner but also improved performance and readability.

> “Functional tools allow us to write code that’s easier to debug and test — which is critical in group projects.”  
> — Personal Reflection

---

## **References**

1. Blacquiere, Ashley. *Week 12 Lecture – Functional Programming*. North Island College, DGL 104.  
2. YouTube – [Functional Programming Overview](https://youtu.be/_uXZ8HvHH7o)  
3. Mozilla Developer Network (MDN) – JavaScript Array Methods  
   https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array  
4. PHP Manual – [array_map, array_filter, array_reduce](https://www.php.net/manual/en/ref.array.php)  
5. Wikipedia – [Functional Programming](https://en.wikipedia.org/wiki/Functional_programming)

---