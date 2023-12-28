+++
title = "Objects"
description = "Object Oriented Programming in Julia"
collection = "basics"
date = 2023-12-27
weight = 6
chapter = false
disableToc = false
pre = "<b>📜</b>"
tags = ["basics", "data", "objects"]
+++

Here is an explanation of object-oriented programming (OOP) paradigm and principles, its advantages and disadvantages, and 3 top languages that are considered pure OOP:

## OOP Principles

Object-oriented programming (OOP) is a programming paradigm that focuses on creating objects, which are self-contained entities that combine data (attributes) and behavior (methods). OOP principles are:

* **Encapsulation:** Bundling data and methods together within an object, protecting internal data from unauthorized access.
* **Inheritance:** Creating new classes (subclasses) based on existing classes (superclasses), inheriting their attributes and methods.
* **Polymorphism:** Defining methods with the same name but different implementations in subclasses, allowing for flexible behavior.
* **Abstraction:** Focusing on the essential aspects of an object, hiding complex internal details from the user.

**Advantages of OOP**

* **Modularization:** Breaking down complex programs into smaller, manageable units (objects).
* **Reusability:** Code written for one object can be reused in other objects through inheritance.
* **Maintainability:** Easier to modify and update code due to encapsulation and clear object boundaries.
* **Scalability:** OOP programs can be easily extended by adding new objects and classes.

**Disadvantages of OOP**

* **Complexity:** Can be more complex to design and understand compared to procedural programming.
* **Overhead:** Creating and managing objects can add overhead, especially for small programs.
* **Steeper learning curve:** Requires understanding of object-oriented concepts, which can be challenging for beginners.

**Top 3 Pure OOP Languages**

1. **Smalltalk:** Considered the purest OOP language, with everything built around objects and messages.
2. **Eiffel:** Designed specifically for OOP principles, with strong emphasis on correctness and reliability.
3. **Clojure:** A functional programming language with strong OOP features, offering a unique blend of paradigms.

There are other languages out there that can use object oriented programming but are not so pure. For example Java and C++. In this article we will talk about Julia.

---

### Julia's Approach to OOP

While Julia is not a traditional OOP language, it supports key OOP principles in alternative ways:

**1. Encapsulation:**
   - Achieved through structs (similar to classes) that encapsulate data.
   - Julia doesn't enforce strict private access modifiers, but conventions and documentation encourage respecting data hiding.

**2. Inheritance:**
   - Not supported for concrete types (structs with fields) due to performance and type stability concerns.
   - Inheritance-like behavior is achieved through abstract types and traits.

**3. Polymorphism:**
   - Implemented through multiple dispatch, a powerful mechanism that selects the appropriate function version based on the types of all arguments, not just the object's type.
   - This enables flexible behavior adaptation without traditional OOP inheritance.

**4. Abstraction:**
   - Achieved through type hierarchies and interfaces defined by abstract types and traits.
   - They specify expected behaviors without defining concrete implementations, promoting code reusability and maintainability.

**Simulating OOP in Julia**

1. **Struct-Based Objects:**
   - Create structs to model objects with data fields.
   - Define separate functions to operate on struct instances, resembling methods.

2. **Multiple Dispatch for Polymorphism:**
   - Define multiple versions of functions for different argument types, achieving polymorphic behavior.

3. **Type Hierarchies with Abstract Types and Traits:**
   - Construct type hierarchies using abstract types as "interfaces."
   - Use traits to group related behaviors and share them across types without inheritance.

**Key Point:**
- Julia's approach prioritizes performance, type stability, and flexible code organization over strict adherence to traditional OOP structures.
- It offers a unique blend of paradigms, effectively supporting OOP principles while emphasizing multiple dispatch and type systems for expressive and efficient code.

---

### What is a Struct?

* A struct (short for structure) is a composite data type that allows you to group multiple related values together under a single name.
* It acts as a blueprint for creating objects with specific fields (also called members or attributes) to hold data of various types.
* It's similar to classes in OOP, but without methods directly attached to them.

**Primary Function:**

* **Organizing Data:** Structs provide a way to structure and organize data in a meaningful way, making code more readable and maintainable.
* **Creating Custom Data Types:** You can define custom data types to model real-world entities or concepts, tailored to your specific needs.

**Example in Julia:**

```julia
struct Person
    name::String
    age::Int
    address::String
end

# Create an instance of the Person struct
person1 = Person("Alice", 30, "123 Main St")

# Access individual fields
println("Name:", person1.name)
println("Age:", person1.age)
println("Address:", person1.address)
```

**Explanation:**

1. **Defining the Struct:**
   - `struct Person` creates a new struct type named `Person`.
   - `name::String`, `age::Int`, and `address::String` define the fields with their expected data types.

2. **Creating an Instance:**
   - `person1 = Person("Alice", 30, "123 Main St")` creates an instance of the `Person` struct, assigning values to its fields.

3. **Accessing Fields:**
   - `person1.name`, `person1.age`, and `person1.address` access the individual fields of the struct instance.

**Comments:**

- Structs are immutable by default, meaning their fields cannot be changed after creation. This ensures data consistency and enhances performance.
- To make a struct mutable, use the `mutable struct` keyword.
- Structs can be nested, creating complex data structures to model intricate relationships.
- They are fundamental for organizing data in Julia, enabling code clarity and flexibility.

---

### Recursive Structs

* A recursive struct is a struct that includes a field of its own type, allowing for the creation of self-referential data structures.
* This enables modeling hierarchical or tree-like structures where elements can have children of the same type.

**Example:**

```julia
struct TreeNode
    value::Int
    left::Union{TreeNode, Nothing}
    right::Union{TreeNode, Nothing}
end
```

**Key Points:**

- The `TreeNode` struct has three fields:
    - `value`: Stores the integer value at the node.
    - `left`: Holds a reference to the left child node, which can be either another `TreeNode` or `Nothing` if there's no left child.
    - `right`: Holds a reference to the right child node, similarly using `Union{TreeNode, Nothing}`.

**Creating a Simple Tree:**

```julia
root = TreeNode(10)
root.left = TreeNode(5)
root.right = TreeNode(15)
```

**Accessing Node Values:**

```julia
println(root.value)   # Output: 10
println(root.left.value)  # Output: 5
```

**Applications:**

- Modeling tree-like structures (e.g., file systems, family trees, decision trees)
- Creating linked lists
- Representing graphs
- Implementing recursive algorithms that operate on self-similar data

**Remember:**

- Handle recursive structures carefully to avoid infinite loops or excessive memory usage.
- Consider using functions that operate recursively on these structures to simplify code and manage complexity effectively.

---

### Dot Notation

Julia does not use dot notation to access methods directly.** While it might resemble object-oriented syntax, the usage and semantics are different. Here's how Julia approaches method calls:

**1. Functions as Methods:**

- Methods are essentially functions that are designed to operate on specific data types, including structs.
- They are not tied to struct definitions like traditional OOP methods.
- You call them like regular functions, passing the struct instance as an argument.

**2. Multiple Dispatch:**

- Julia's powerful multiple dispatch system selects the appropriate method version based on the types of all arguments, not just the object's type.
- This enables flexible behavior adaptation without traditional inheritance.

**Example:**

```julia
struct Point
    x::Int
    y::Int
end

# Function acting as a method for Point instances
function distance_to_origin(p::Point)
    return sqrt(p.x^2 + p.y^2)
end

p1 = Point(3, 4)
distance = distance_to_origin(p1)  # Call the method like a function
println("Distance:", distance)
```

**Key Points:**

- Dot notation is primarily used in Julia for:
    - Accessing struct fields (e.g., `p1.x`)
    - Calling certain built-in functions on objects (e.g., `length(p1)` to get the number of fields)
- It's not used for direct method calls like in OOP languages.
- Julia's approach emphasizes functions and multiple dispatch for flexible and performant code organization.


**Think of Julia functions as tools in a toolbox:**

- Each tool (function) is designed for specific tasks (operating on specific data types).
- You select the right tool (function) based on the job at hand (the types of arguments).
- Multiple dispatch is like having multiple versions of a tool, each fine-tuned for different materials (data types).
- This flexibility allows for efficient and adaptable code without the overhead of traditional OOP structures.

---

## Object Structures

While Julia doesn't have traditional classes and objects, it simulates object-oriented behavior effectively using structs and functions:

**1. Defining the Struct:**

- Create a struct to represent the object's data fields:

```julia
struct Person
    name::String
    age::Int
end
```

**2. Defining Functions as Methods:**

- Define functions outside the struct to act as methods, operating on struct instances:

```julia
function greet(person::Person)
    println("Hello, my name is $(person.name)!")
end

function age_up(person::Person)
    person.age += 1
end
```

**3. Creating and Using the Object:**

- Create an instance o **Inheritance in Julia: Key Concepts and Alternatives**

**While Julia doesn't support traditional inheritance for concrete types (structs with fields), it offers mechanisms to achieve inheritance-like behavior:**

**1. Abstract Types as Interfaces:**

- Define abstract types to act as blueprints, specifying expected methods without concrete implementations.
- Concrete types can subtype abstract types, ensuring they provide required methods.

**Example:**

```julia
abstract type Shape end

function area(shape::Shape)
    error("Abstract method area not implemented for $(typeof(shape))")
end

struct Rectangle <: Shape
    width::Float64
    height::Float64
end

function area(rectangle::Rectangle)
    return rectangle.width * rectangle.height
end

struct Circle <: Shape
    radius::Float64
end

function area(circle::Circle)
    return pi * circle.radius^2
end
```

**2. Traits for Shared Behavior:**

- Traits are collections of methods that can be mixed into types without traditional inheritance.
- This enables sharing behavior across unrelated types without creating a strict hierarchy.

**Example:**

```julia
trait Printable
    function print(obj::Printable)
        println("Printable object: $(obj)")
    end
end

struct Person
    name::String
    age::Int
end

Base.extend(Person, Printable)  # Mix the Printable trait into Person

person1 = Person("Alice", 30)
print(person1)  # Output: Printable object: Person("Alice", 30)
```

**Comments:**

- Julia's approach prioritizes performance, type stability, and flexible code organization over strict inheritance hierarchies.
- Abstract types and traits provide effective ways to create type hierarchies and share behavior without the overhead of traditional inheritance.
- Multiple dispatch often complements these mechanisms, enabling flexible behavior adaptation based on argument types.
- Understanding these alternatives is crucial for designing well-structured and performant code in Julia.
f the struct:

```julia
person1 = Person("Bob", 35)
```

- Use functions like methods on the instance:

```julia
greet(person1)  # Output: Hello, my name is Bob!
age_up(person1)
println("New age:", person1.age)  # Output: New age: 36
```

### Why Julia's Approach:

**1. Performance and Type Stability:**

- Traditional OOP's inheritance can introduce overhead and potential type instability.
- Julia prioritizes performance and predictable behavior, especially for numerical computing.

**2. Flexibility and Multiple Dispatch:**

- Julia's multiple dispatch system allows functions to behave differently based on the types of all arguments, not just the object's type.
- This enables more flexible and adaptable code, often surpassing traditional OOP's inheritance model.

**3. Composition over Inheritance:**

- Julia encourages building complex types by combining simpler types, aligning with the concept of composition over inheritance.
- This often leads to more modular and reusable code structures.

**4. Clearer Separation of Concerns:**

- Separating data (structs) from behavior (functions) can enhance code readability and maintainability.
- It makes data dependencies more explicit and promotes modular design.

**5. Embracing Multiple Paradigms:**

- Julia embraces multiple programming paradigms, including functional and procedural elements.
- This flexibility allows developers to choose approaches that best suit their problem domains.

**Adapting to Julia's Model:**

- While initially unfamiliar for those accustomed to traditional OOP, Julia's approach offers significant advantages for performance, flexibility, and type safety.
- By understanding structs, functions, multiple dispatch, and composition, developers can effectively create well-structured, performant, and maintainable code in Julia.

---

### Encapsulation in Julia

While Julia doesn't have strict private access modifiers like traditional OOP languages, it still encourages encapsulation through conventions and design practices. Here's how it's achieved:

**1. Structs for Data Encapsulation:**

- Structs create custom data types that group related data fields together.
- This bundling of data inherently promotes encapsulation.

**2. Descriptive Naming for Clarity:**

- Use clear and meaningful names for struct fields to signal their intended use and discourage direct access.
- For example, prefer `person.full_name` over `person.name1`.

**3. Separate Functions for Behavior:**

- Define functions outside of structs to operate on struct instances, resembling methods.
- This separates data from behavior, enhancing code organization and modularity.

**4. Internal Modules for Private Data:**

- Group fields and functions within an internal module within a struct to create a stronger sense of privacy.
- This signals that these elements are intended for internal use and discourages external access.

**Example:**

```julia
struct Person
    name::String
    age::Int

    # Internal module for private data and functions
    module _private
        address::String

        function greet(person::Person)
            println("Hello, my name is $(person.name) and I live at $(person.address)")
        end
    end
end

function create_person(name, age, address)
    person = Person(name, age)
    person._private.address = address  # Access private field within the module
    return person
end

person1 = create_person("Alice", 30, "123 Main St")
Person._private.greet(person1)  # Call private function using module syntax
```

**Key Points:**

- Julia's approach to encapsulation prioritizes code clarity and flexibility over strict access controls.
- It relies on conventions and design practices to encourage data hiding and modularity.
- Internal modules create a stronger sense of privacy for sensitive data and functions.
- It's essential to respect these conventions to maintain code organization and prevent unintended side effects.

---

 ### Inheritance in Julia

While Julia doesn't support traditional inheritance for concrete types (structs with fields), it offers mechanisms to achieve inheritance-like behavior:

**1. Abstract Types as Interfaces:**

- Define abstract types to act as blueprints, specifying expected methods without concrete implementations.
- Concrete types can subtype abstract types, ensuring they provide required methods.

**Example:**

```julia
abstract type Shape end

function area(shape::Shape)
    error("Abstract method area not implemented for $(typeof(shape))")
end

struct Rectangle <: Shape
    width::Float64
    height::Float64
end

function area(rectangle::Rectangle)
    return rectangle.width * rectangle.height
end

struct Circle <: Shape
    radius::Float64
end

function area(circle::Circle)
    return pi * circle.radius^2
end
```

**2. Traits for Shared Behavior:**

- Traits are collections of methods that can be mixed into types without traditional inheritance.
- This enables sharing behavior across unrelated types without creating a strict hierarchy.

**Example:**

```julia
trait Printable
    function print(obj::Printable)
        println("Printable object: $(obj)")
    end
end

struct Person
    name::String
    age::Int
end

Base.extend(Person, Printable)  # Mix the Printable trait into Person

person1 = Person("Alice", 30)
print(person1)  # Output: Printable object: Person("Alice", 30)
```

**Comments:**

- Julia's approach prioritizes performance, type stability, and flexible code organization over strict inheritance hierarchies.
- Abstract types and traits provide effective ways to create type hierarchies and share behavior without the overhead of traditional inheritance.
- Multiple dispatch often complements these mechanisms, enabling flexible behavior adaptation based on argument types.
- Understanding these alternatives is crucial for designing well-structured and performant code in Julia.

---

### Abstraction in Julia

Abstraction involves focusing on essential aspects of an object or concept while hiding complex implementation details. In Julia, it's achieved primarily through:

**1. Abstract Types:**

- **Definition:** Abstract types act as blueprints, specifying expected behaviors without providing concrete implementations.
- **Purpose:**
    - Define interfaces for related types, ensuring they share common functionality.
    - Create type hierarchies to organize code and enforce consistency.

**Example:**

```julia
abstract type Shape
    area()
end

struct Rectangle <: Shape
    width::Float64
    height::Float64
end

function area(rectangle::Rectangle)
    return rectangle.width * rectangle.height
end

struct Circle <: Shape
    radius::Float64
end

function area(circle::Circle)
    return pi * circle.radius^2
end
```

**2. Traits:**

- **Definition:** Traits are collections of methods that can be mixed into types to share behavior without traditional inheritance.
- **Purpose:**
    - Modularize code by separating behavior from type definitions.
    - Share common functionality across unrelated types, promoting code reuse.

**Example:**

```julia
trait Printable
    function print(obj::Printable)
        println("Printable object: $(obj)")
    end
end

struct Person
    name::String
    age::Int
end

Base.extend(Person, Printable)  # Mix the Printable trait into Person

person1 = Person("Alice", 30)
print(person1)  # Output: Printable object: Person("Alice", 30)
```

**Key Points:**

- Abstraction enhances code readability, maintainability, and flexibility.
- It promotes code reuse and reduces coupling between components.
- Abstract types and traits are powerful tools for achieving abstraction in Julia.
- Understanding their roles is essential for designing well-structured Julia programs.

---

### Polymorphism in Julia:

While Julia doesn't have traditional OOP inheritance, it achieves polymorphism through multiple dispatch:

**1. Multiple Dispatch:**

- Julia's core mechanism for selecting the appropriate function version based on the types of all arguments, not just the object's type.
- This enables functions to behave differently for different combinations of argument types.

**2. Defining Multiple Methods:**

- Create multiple versions of a function with different signatures (combinations of argument types).
- Julia dispatches to the correct version at runtime, ensuring the most appropriate behavior.

**Example:**

```julia
function greet(person::Person)
    println("Hello, $(person.name)!")
end

function greet(animal::Animal)
    println("Hello, furry friend!")
end

function greet(obj)
    println("Hello, unknown thing!")  # Catch-all for other types
end

person1 = Person("Alice")
animal1 = Animal("Dog")
unknown_thing = 123

greet(person1)   # Output: Hello, Alice!
greet(animal1)   # Output: Hello, furry friend!
greet(unknown_thing)  # Output: Hello, unknown thing!
```

**Comments:**

- Multiple dispatch is more flexible than traditional OOP polymorphism, as it considers all argument types, not just the receiver's type.
- It leads to more adaptable and expressive code, often eliminating the need for explicit type checks or conditional logic.
- Julia's type system and compiler optimizations make multiple dispatch efficient, even for complex scenarios.
- Understanding multiple dispatch is crucial for writing effective and versatile Julia code.

---

## Parametric Types

While Julia doesn't have generics in the traditional OOP sense, it achieves similar functionality through a combination of multiple dispatch and parametric types:

**1. Multiple Dispatch as the Core Mechanism:**

- Allows functions to behave differently based on the specific types of their arguments.
- This enables a form of generic behavior without traditional generic types.

**2. Parametric Types for Flexible Definitions:**

- Define functions and types that can work with a range of different types, specified by parameters.
- This creates generic-like constructs that can adapt to various data types.

**Example:**

```julia
# Parametric function using multiple dispatch
function add{T}(x::T, y::T)
    return x + y
end

# Works for various numeric types
println(add(1, 2))   # Output: 3
println(add(3.5, 1.2))  # Output: 4.7

# Parametric type
struct Point{T}
    x::T
    y::T
end

# Works with different coordinate types
point1 = Point{Int}(3, 4)
point2 = Point{Float64}(1.5, 2.8)
```

**Comments:**

- Julia's approach prioritizes performance and type specialization over traditional generics.
- Multiple dispatch often eliminates the need for type erasure or boxing/unboxing, leading to faster code.
- Parametric types provide flexibility for defining generic-like constructs.
- Understanding multiple dispatch and parametric types is essential for writing adaptable and efficient Julia code.

---

## Modules in Julia:

Modules offer a powerful way to structure code, encapsulate functionality, and create reusable libraries in Julia. Here's how they effectively handle object types:

**Understanding Modules:**

- **Definition:** Modules are namespaces that group related functions, types, and variables.
- **Purpose:**
    - Organize code into logical units for better readability and maintainability.
    - Prevent naming conflicts by controlling the visibility of identifiers.
    - Create reusable libraries that can be shared across projects.

**Use Cases for Object Handling:**

1. **Encapsulating Object-Related Functionality:**
    - Define functions that operate on specific object types within a module.
    - This keeps related code together and promotes modularity.

2. **Creating Reusable Libraries:**
    - Package object-related code as a module (or a collection of modules).
    - This enables sharing and reusing functionality across different projects.

3. **Controlling Visibility:**
    - Use `public`, `private`, and `export` to manage which names are accessible outside the module.
    - This helps protect internal implementation details and create clear interfaces.

**Best Practices:**

- **Clear Naming:** Choose descriptive names for modules and functions to enhance code clarity.
- **Cohesive Organization:** Group related functionality within modules for logical structure.
- **Meaningful Exports:** Only export essential elements for external use, avoiding unnecessary complexity.
- **Docstrings:** Provide clear documentation for modules, functions, and types to explain their purpose and usage.

**Example Structure for Handling an Object Type:**

```julia
module MyObjectLibrary

export MyObjectType, create_object, get_value, set_value

struct MyObjectType
    value::Int
end

function create_object(value)
    return MyObjectType(value)
end

function get_value(obj::MyObjectType)
    return obj.value
end

function set_value(obj::MyObjectType, new_value)
    obj.value = new_value
end

end  # module MyObjectLibrary
```

By effectively using modules, you can create well-structured, reusable, and maintainable code that effectively handles object types in Julia.

---

> "Modern languages dance with agility, but ancient voices echo in their bones." -- Gemini AI













