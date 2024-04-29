+++
title = "Python Syntax"
description = "Essential Python syntax elements"
collection = "interpreters"
date =  2024-01-04
weight = 43
chapter = false
disableToc = false
pre = "<b>📜</b>"
tags = ["python", "interpreters"]
+++

## What is Python?

Python is a **high-level, general-purpose programming language** known for its **readability, simplicity, and versatility**. It was created by Guido van Rossum in 1991 and has since become one of the most popular languages in the world. 

Here are some key characteristics of Python:

* **Easy to learn:** Python has a clear and concise syntax that resembles plain English, making it easier to pick up compared to other languages.
* **Versatile:** Python can be used for a wide range of tasks, including web development, data science, machine learning, automation, and scientific computing.
* **Powerful:** Despite its simplicity, Python is a powerful language with a rich set of libraries and frameworks that can handle complex tasks.
* **Interpreted:** This means you don't need to compile your code before running it, making the development process faster and more iterative.
* **Open-source:** Python is free to use and develop, with a large and active community that contributes to its libraries and tools.

**Topics covered**

In this short tutorial we will cover fundamental topics to understand Python from beginer to intermediate developer.  After reading this page is a good idea to consider taking our advanced Python course that is hostet on Sage-Code main web-site. 


1. **Data Types:** Learn about Python's fundamental data types like numbers, strings, lists, dictionaries, and sets. How to define, interpret, and manipulate them.
2. **Variables and Constants:** Understand how to store and reference data using variables, and utilize constants for unchanging values.
3. **Operators:** Learn about arithmetic, comparison, logical, and assignment operators used to perform calculations and expressions.
4. **Conditional Statements:** Master `if`, `else`, and `elif` statements to control program flow based on conditExplaions.
5. **Loops:** Discover `for` and `while` loops to iterate through sequences and repeat code blocks.
6. **Functions:** Define and call functions to modularize your code, improve reusability, and simplify complex tasks.
7. **Modules and Packages:** Understand how to import and use external code written by others to expand your capabilities.
8. **Basic Input and Output:** Learn how to get user input and display information on the console.

These are just the foundational topics to get you started with Python syntax. As you progress, you will explore more advanced concepts like classes, objects, object-oriented programming, and exception handling.

{{% notice warning %}}
This tutorial is created using AI (Gemini) and may not be perfect. We will continue to improve this tutorial in the future with help from students like yourself. Join Discord and GitHub to contribute. This tutorial is open source. If you conntinue reading and encounter errors, please report them and create work items for us to resolve them.
{{% /notice %}}

---

## Fundamental Elements

- **Case Sensitivity:** Python is case-sensitive. `name` and `Name` are distinct variables.
- **Indentation:** Code blocks (like `if` statements and loops) are defined by consistent indentation (usually 4 spaces), not curly braces.
- **Comments:** Use `#` for single-line comments and `"""` or `'''` for multi-line comments.
- **Whitespace:** Extra spaces or newlines don't generally affect code, except within strings.

**Data Types:**

- **Numbers:** `int` (integers), `float` (decimals), `complex` (real and imaginary parts).
- **Strings:** Text enclosed in single or double quotes (both are equivalent).
- **Booleans:** `True` or `False`.
- **Variables:** Store values using lowercase names (uppercase for class names).

**Operators:**

- **Arithmetic:** `+`, `-`, `*`, `/`, `//` (integer division), `%` (remainder).
- **Comparison:** `==`, `!=`, `<`, `>`, `<=`, `>=`.
- **Logical:** `and`, `or`, `not`.
- **Assignment:** `=`, `+=`, `-=`, `*=`, `/=`, etc.

**Control Flow:**

- **`if` Statements:** Decide which code to execute based on a condition:

   ```python
   if age >= 18:
       print("You are eligible to vote.")
   ```

- **`else` and `elif` Statements:** Provide alternative choices:

   ```python
   if grade >= 90:
       print("Excellent!")
   elif grade >= 80:
       print("Good job!")
   else:
       print("Keep practicing!")
   ```

- **`for` Loops:** Repeat code for a sequence of steps:

   ```python
   for i in range(5):  # Iterates 5 times
       print(i)
   ```

- **`while` Loops:** Repeat code until a condition is met:

   ```python
   num = 1
   while num <= 10:
       print(num)
       num += 1  # Increase num by 1
   ```

**Functions:**

- Reusable blocks of code that perform a task:

   ```python
   def greet(name):
       print("Hello, " + name + "!")

   greet("Alice")  # Output: Hello, Alice!
   ```

**Essential Tips:**

- Start with simple examples and gradually build complexity.
- Experiment with different code snippets to understand how they work.
- Indentation is crucial; maintain consistent spacing.
- Use good variable names that reflect their purpose.
- Practice regularly to solidify your understanding.
- Leverage online resources, tutorials, and communities for help.

**Additional Considerations:**

- Python also supports data structures like lists, dictionaries, and tuples, as well as object-oriented programming concepts.
- Error messages can be cryptic at times, but carefully reading them can provide valuable clues.
- The official Python documentation ([https://docs.python.org/3/](https://docs.python.org/3/)) is a comprehensive resource.

---

### Introductiory example

Explaining Python syntax is not yet good enaugh for you to understand Python. Therefore we will ceate examples and explain the code using AI. You can read all about Python in the documentation but using these examples you can dive deeper and have a better start. Let's try our first example:

```python
def factorial(n):
    """Calculates the factorial of a non-negative integer n.

    Args:
        n: The non-negative integer for which to calculate the factorial.

    Returns:
        The factorial of n, or None if n is negative.

    Raises:
        ValueError: If n is negative.
    """

    if n < 0:
        raise ValueError("n must be non-negative")

    if n == 0:
        return 1  # Base case: factorial of 0 is 1

    result = 1
    for i in range(1, n + 1):
        result *= i  # Multiply result by each number from 1 to n
    return result

# Test cases with assert statements
assert factorial(0) == 1, "factorial(0) should be 1"
assert factorial(5) == 120, "factorial(5) should be 120"
assert factorial(10) == 3628800, "factorial(10) should be 3628800"

# Print the results of 3 calls
print(f"factorial(0) = {factorial(0)}")
print(f"factorial(5) = {factorial(5)}")
print(f"factorial(10) = {factorial(10)}")
```

**Explanation:**

1. **Function Definition:**
   - `def factorial(n):` defines a function named `factorial` that takes one argument `n`.
2. **Docstring:**
   - The triple-quoted string explains what the function does.
3. **Input Validation:**
   - `if n < 0:` checks for invalid input (negative numbers).
   - `raise ValueProgramError("n must be non-negative")` raises an error if input is invalid.
4. **Base Case:**
   - `if n == 0:` handles the special case where `n` is 0, returning 1.
5. **Factorial Calculation:**
   - `result = 1` initializes a variable to store the factorial.
   - `for i in range(1, n + 1):` iterates from 1 to `n`.
   - `result *= i` multiplies `result` by each number in the range, calculating the factorial.
6. **Return Value:**
   - `return result` returns the calculated factorial.
7. **Test Cases:**
   - `assert` statements check if the function produces expected results for specific inputs.
8. **Printing Results:**
   - `print(f"factorial(x) = {factorial(x)}")` calls the function with different values and prints the results.

**Output:**

```text
factorial(0) = 1
factorial(5) = 120
factorial(10) = 3628800
```

{{% notice tip %}}
Observe, the function factorial(n) is ending with statement: "return result", that has an indentation of 4 spaces. The program continue with "assert". There is nothing to tell you that the function dyefinition has ended. This is an inconvenient for beginners and this is one of the reasons I do not like Python.
{{% /notice %}}

---

### Python Data Types

Here's a breakdown of Python's fundamental data types, complete with explanations, examples, and code snippets:

**Numbers:**

* **Integers (`int`)** represent whole numbers without decimals, like `10`, `-5`, or `42`.
* **Floats (`float`)** represent numbers with decimals, like `3.14`, `-2.718`, or `1.0e6` (scientific notation).
* **Complex numbers (`complex`)** represent numbers with real and imaginary parts, like `3 + 4j` or `5.2 - 1.8j`.

**Example:**

```python
age = 30  # int
price = 29.99  # float
complex_number = 3 + 2j  # complex
```

**Strings:**

* **Strings (`str`)** represent sequences of characters, enclosed in single or double quotes (`'hello'` or `"world!"`).
* They can hold text, numbers, symbols, or any combination.
* Use backslashes (`\`) to escape special characters like quotes or newlines.

**Example:**

```python
name = "Alice"
greeting = 'Hello, world!'
multiline_string = """This is a
multiline string"""
```

**Lists:**

* **Lists (`list`)** are ordered collections of items, enclosed in square brackets `[]`.
* Items can be of any data type, including other lists.
* You can access, modify, and add elements using their index (starting from 0).

**Example:**

```python
fruits = ["apple", "banana", "cherry"]
mixed_list = [1, "two", 3.0]
empty_list = []
```

**Tuples:**

* **Tuples (`tuple`)** are similar to lists but **immutable**, meaning their elements cannot be changed after creation.
* Enclosed in parentheses `()`, they are useful for data that shouldn't be modified.

**Example:**

```python
coordinates = (10, 20)  # Immutable
nested_tuple = (1, [2, 3], (4, 5))
```

**Dictionaries:**

* **Dictionaries (`dict`)** are unordered collections of key-value pairs, enclosed in curly braces `{}`.
* Keys must be unique and immutable (like strings or numbers), while values can be any data type.
* Access values using their keys.

**Example:**

```python
person = {"name": "Bob", "age": 35, "city": "New York"}
empty_dict = {}
```

**Sets:**

* **Sets (`set`)** are unordered collections of unique items, enclosed in curly braces `{}`.
* They are useful for removing duplicates and checking membership.
* Order of elements is not guaranteed.

**Example:**

```python
unique_fruits = {"apple", "banana", "apple"}  # Removes duplicates
numbers = {1, 2, 3, 2}  # Keeps only unique values
```

**Remember:**

* You can check the data type of a variable using the `type()` function: `print(type(age))`.
* Python is dynamically typed, so you don't need to declare data types explicitly.
* Choose the appropriate data type based on your needs:
    * Numbers for calculations.
    * Strings for text and formatting.
    * Lists for ordered collections that may change.
    * Tuples for fixed data.
    * Dictionaries for key-value relationships.
    * Sets for unordered, unique collections.

By understanding these fundamental data types, you'll have a solid foundation for building Python programs!

---

### Data Literals & Variables

Here's an explanation of data literals, global vs. local scope, and best practices for variables and constants in Python:

**Data Literals:**

- Data literals are fixed values directly written into code, representing specific data types.
- Examples:
    - Integer literals: `10`, `-5`, `0`
    - Floating-point literals: `3.14159`, `-2.718`, `1.0e6`
    - String literals: `"hello"`, `'world'`, `'''multiline string'''`
    - Boolean literals: `True`, `False`
    - List literals: `[1, 2, 3]`, `["apple", "banana"]`
    - Tuple literals: `(10, 20)`, `("x", "y", "z")`
    - Dictionary literals: `{"name": "Alice", "age": 30}`, `{}`
    - Set literals: `{1, 2, 3}`, `{"apple", "banana"}`

**Global and Local Scope:**

- **Global Variables:** Declared outside of any function, accessible throughout the program.
    - Example:
    ```python
    PI = 3.14159  # Global variable

    def calculate_area(radius):
        area = PI * radius**2  # Can access PI here
        return area
    ```
- **Local Variables:** Declared inside a function, accessible only within that function.
    - Example:
    ```python
    def greet(name):
        greeting = "Hello, " + name  # Local variable
        print(greeting)
    ```

**Best Practices:**

- **Variables:**
    - Use descriptive names to improve readability.
    - Prefer lowercase for variable names (by convention).
    - Avoid unnecessary global variables, as they can make code less modular and harder to test.
    - Use local variables whenever possible to limit scope and potential side effects.
- **Constants:**
    - Declare with uppercase names to signal their immutability.
    - Use `ALL_CAPS` for constants by convention.

**Additional Tips:**

- Use comments to explain the purpose of variables and constants.
- Consider using type hints to make code more readable and maintainable.
- Avoid naming variables the same as built-in functions or keywords.

---

### Collections Explained

While Python doesn't have built-in arrays like some other languages, it offers powerful alternatives like lists, tuples, and dictionaries for storing and organizing data. Let's break down each one:

**1. Lists: The Flexible All-Rounders**

Imagine lists like shopping carts. They're **mutable** (you can add, remove, or change items), **ordered** (items have a specific sequence), and can hold **different data types** (numbers, strings, even other lists!).

**Example:**

```python
fruits = ["apple", "banana", "orange"]  # Create a list
fruits.append("mango")  # Add an item
print(fruits[1])  # Access the second item ("banana")
```

**Use lists when:**

* You need to manage a changing collection of items.
* The order of items matters.
* You want to store diverse data types together.

**2. Tuples: The Immutable Champions**

Think of tuples like museum exhibits. They're **immutable** (you can't modify them), **ordered**, and can also hold **mixed data types**. But once created, their contents are fixed.

**Example:**

```python
coordinates = (10, 20)  # Create a tuple
# coordinates[0] = 15  # This will raise an error (tuples are immutable)
print(coordinates[1])  # Access the second item (20)
```

**Use tuples when:**

* You need a fixed set of data that shouldn't be changed accidentally.
* You want to use elements as dictionary keys (immutability guarantees uniqueness).

**3. Dictionaries: The Key-Value Keepers**

Imagine dictionaries like phonebooks. They store **key-value pairs**, where the key uniquely identifies an item (like a name) and the value is the associated data (like a phone number). Dictionaries are **mutable** and can hold **different data types** for both keys and values.

**Example:**

```python
person = {"name": "Alice", "age": 30, "city": "New York"}
print(person["age"])  # Access the value for key "age" (30)
person["city"] = "London"  # Update the city
```

**Use dictionaries when:**

* You need to associate data with unique identifiers.
* The order of items doesn't matter.
* You want to efficiently access data using keys.

**Bonus Tip:**

* **Arrays in Python:** While Python doesn't have built-in arrays, the `array` module provides array-like functionality for specific use cases (e.g., storing large numbers efficiently).

{{% notice tip %}}
Remember, choosing the right collection depends on your specific needs. Lists offer versatility, tuples ensure data integrity, and dictionaries excel in key-based lookups. So, experiment and find the perfect fit for your Python projects!
{{% /notice %}}

---

## Python Packages

In Python, packages are like pre-built components that offer reusable code, modules, and functions. Think of them as modular tools you can integrate into your projects to save time and effort. Here's a breakdown:

**1. What are Packages in Python?**

- A package is a directory containing Python modules, data files, and metadata (`setup.py` or `pyproject.toml`).
- Modules within a package follow a specific structure for organization and import.
- You can reuse functions and classes defined in these modules across different projects.
- They help avoid code duplication and promote modular development.

**2. What is a Package Manager?**

- A package manager is a tool that simplifies finding, installing, and managing Python packages.
- The most popular package manager for Python is **pip**.
- Pip interacts with the Python Package Index (PyPI), a vast repository of third-party packages.

**3. Finding Packages:**

- Use the `pip search` command followed by keywords to find relevant packages on PyPI.
- Explore PyPI's website ([https://pypi.org/](https://pypi.org/)) for browsing and filtering packages.
- Read documentation and user reviews to understand packages before installing.

**4. Using Packages in Projects:**

- Install the package using `pip install <package_name>`.
- Import the desired module from the package in your Python script using `import <module_name>`.
- Access functions and classes within the module using dot notation (e.g., `module_name.function_name()`).

**Examples:**

- Use `numpy` for numerical computations: `import numpy as np`
- Use `requests` for making HTTP requests: `import requests`
- Use `matplotlib` for data visualization: `import matplotlib.pyplot as plt`

**Tips:**

- Create virtual environments to isolate project dependencies and avoid conflicts.
- Use a tool like `pipreqs` to generate a `requirements.txt` file listing project dependencies.
- Keep packages updated to benefit from bug fixes and new features.

By understanding packages and package managers, you can leverage the vast ecosystem of tools and libraries available in Python, making your development process more efficient and productive!

---

## Built In Packages

 **Built-in Packages in Python: Ready-to-Use Tools at Your Fingertips**

While Python offers a rich ecosystem of third-party packages, it also comes with a set of valuable built-in packages, pre-installed and ready to use. These packages provide essential functionality for common tasks, saving you time and effort.

**The `io` Package: Your Gateway to File Input and Output**

One of these built-in packages is the `io` package, which empowers you to interact with files effectively. Here's how to use it for reading and writing files:

**1. Reading from Files:**

- **Open the file in read mode:**

```python
with open("my_file.txt", "r") as file:
    # Read the entire contents
    contents = file.read()
    print(contents)
```

- **Read lines individually:**

```python
with open("my_file.txt", "r") as file:
    for line in file:
        print(line, end="")  # Print each line without extra newlines
```

**2. Writing to Files:**

- **Open the file in write mode (creates a new file or overwrites an existing one):**

```python
with open("new_file.txt", "w") as file:
    file.write("This is some new text.")
```

- **Append to an existing file:**

```python
with open("existing_file.txt", "a") as file:
    file.write("\nThis text is appended.")
```

**Key Points:**

- The `with` statement ensures proper file closure, even if errors occur.
- Different modes control how you open files: "r" for reading, "w" for writing (overwrites), "a" for appending, and "r+" for both reading and writing.
- Use `file.read()` to read the entire content, `file.readlines()` to read all lines into a list, or iterate through lines using a `for` loop.
- Use `file.write()` to write text to a file.

**Additional Tips:**

- Explore other file-related methods in the `io` package for tasks like seeking within a file (`file.seek()`) and checking your current position (`file.tell()`).
- Consider using context managers (`with` statements) for clean resource management.
- Remember to always close files when you're finished working with them.

By mastering the `io` package and other built-in packages, you'll tap into Python's core capabilities and streamline your development process!

---

## Advanced Course

So far you have learned the basics of Python. If you enjoy reading so far, I'm proud of you. Next maybe you wish to study more. You can chose to follow the documentation or other mentors. We offer an advanced Python course, that will teach you again the basics and then enable introductions of advance topics. 

Follow next: [CSP04-Python](https://sagecode.pro/index.html)

---

> "Python is a beautiful language. It's easy to learn and use, but it's also very powerful. It's one of the most popular languages in the world, and for good reason." (Mark Zuckerberg, co-founder of Facebook)