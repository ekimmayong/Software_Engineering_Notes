# Phase 1 — Fundamentals (0–3 months)

Goal: Gain fluency in a programming language and core programming concepts.

## Topics

- Syntax, variables, types, expressions
  - Definition: Syntax is the set of rules that define valid programs in a language. Variables are named storage locations. Types describe the kind of data a value holds (e.g., integer, string). Expressions combine values, variables, and operators to produce new values.
  - Discussion: Focus first on writing small snippets that use different types and expressions. Pay attention to language-specific syntax quirks (indentation in Python, semicolons in JavaScript/Java). Practice reading error messages when syntax or type errors occur and fix them. Try small exercises that convert between types and manipulate strings and numbers.
  - Examples:

    - Python:

    ```python
    # variables and expressions
    name = "Alice"
    age = 30
    greeting = f"Hello, {name}. You are {age} years old."
    print(greeting)
    ```

    - JavaScript:

    ```javascript
    // variables and expressions
    const name = 'Alice';
    let age = 30;
    console.log(`Hello, ${name}. You are ${age} years old.`);
    ```

- Control flow: conditionals and loops
  - Definition: Control flow constructs (if/else, switch, for, while) determine the order in which statements execute based on conditions or repetition.
  - Discussion: Learn the differences between loop types and when to use each. Watch for off-by-one errors in loops and infinite-loop risks. Practice by implementing algorithms that require branching (e.g., decision trees) and iteration (e.g., summing elements, searching).
  - Examples:

    - Summing numbers in Python:

    ```python
    total = 0
    for i in range(1, 6):
        total += i
    print(total)  # 15
    ```

    - Conditional in JavaScript:

    ```javascript
    const score = 85;
    if (score >= 90) {
      console.log('A');
    } else if (score >= 80) {
      console.log('B');
    } else {
      console.log('C');
    }
    ```

- Functions, scopes, parameters, return values
  - Definition: Functions are named blocks of code that perform a task. Parameters are inputs to functions; return values are outputs. Scope determines where variables are accessible.
  - Discussion: Start by writing pure functions (no side effects) to understand inputs and outputs. Learn how local vs global scope affects state and bugs. Practice creating reusable functions and composing them. Experiment with default parameters and variable argument lists if your language supports them.
  - Examples:

    - Python:

    ```python
    def add(a, b):
        return a + b

    result = add(2, 3)
    print(result)  # 5
    ```

    - JavaScript:

    ```javascript
    function add(a, b) {
      return a + b;
    }
    console.log(add(2, 3));
    ```

- Basic data structures: arrays/lists, dictionaries/maps, sets
  - Definition: Data structures organize data for efficient access. Lists/arrays store ordered collections; dictionaries/maps store key-value pairs; sets store unique elements.
  - Discussion: Implement small tasks using each structure (e.g., frequency count with a map, deduplication with a set). Understand common operations and their costs (indexing, insertion, deletion). Try implementing a simple wrapper around a native structure to deepen understanding.
  - Examples:

    - Python list and dict:

    ```python
    items = [1, 2, 2, 3]
    unique = set(items)
    counts = {}
    for x in items:
        counts[x] = counts.get(x, 0) + 1
    print(unique)   # {1,2,3}
    print(counts)   # {1:1, 2:2, 3:1}
    ```

    - JavaScript Map and Set:

    ```javascript
    const items = [1,2,2,3];
    const unique = new Set(items);
    const counts = new Map();
    for (const x of items) {
      counts.set(x, (counts.get(x) || 0) + 1);
    }
    console.log(unique); // Set {1,2,3}
    console.log(counts); // Map {1 => 1, 2 => 2, 3 => 1}
    ```

- Intro to OOP: classes, objects, methods
  - Definition: Object-oriented programming models software as objects that combine data (attributes) and behavior (methods). Classes are blueprints for objects.
  - Discussion: Learn to design small classes with clear responsibilities. Practice encapsulation (hide internal state) and composition over inheritance. Build a few domain models (e.g., Task/Project for a todo app) to see how objects interact.
  - Examples:

    - Python class:

    ```python
    class Task:
        def __init__(self, title):
            self.title = title
            self.done = False

        def complete(self):
            self.done = True

    t = Task('Buy milk')
    t.complete()
    print(t.done)  # True
    ```

    - JavaScript class:

    ```javascript
    class Task {
      constructor(title) {
        this.title = title;
        this.done = false;
      }
      complete() {
        this.done = true;
      }
    }
    const t = new Task('Buy milk');
    t.complete();
    console.log(t.done);
    ```

- Basic input/output and file handling
  - Definition: I/O covers reading input from users or files and writing output to the console, files, or network. File handling includes opening, reading, writing, and closing files safely.
  - Discussion: Practice reading and writing text and simple binary files. Learn to handle errors (file not found, permission issues) and to use context managers or try/finally to ensure resources are closed. Build small scripts that parse CSV or JSON files as practical exercises.
  - Examples:

    - Python read/write JSON:

    ```python
    import json
    data = {'name': 'Alice', 'age': 30}
    with open('data.json', 'w') as f:
        json.dump(data, f)

    with open('data.json') as f:
        loaded = json.load(f)
    print(loaded)
    ```

    - Node.js write/read file:

    ```javascript
    const fs = require('fs');
    const data = { name: 'Alice', age: 30 };
    fs.writeFileSync('data.json', JSON.stringify(data));
    const loaded = JSON.parse(fs.readFileSync('data.json'));
    console.log(loaded);
    ```

## Exercises

- Follow the official tutorial for your chosen language.
- Implement 20 small programs (FizzBuzz, factorial, palindrome check, prime tester).
- Complete 30 code katas on practice sites.

## Projects

- CLI calculator
- Simple todo list (file-based)
- Small script to automate a repetitive task on your computer

## Tools

- VS Code debugger, REPL, language-specific linters
- Git for version control
