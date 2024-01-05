+++
title = "Programming"
collection = "basics"
author = "Bard/Gemini"
date = 2023-12-26
weight = 1
chapter = false
disableToc = false
pre = "<b>📜</b>"
tags = ["programming", "basics"]
description = "Top programming languages"
+++

## What is a Programming Language?

Here's an explanation of programming languages, interpreters, and compilers:

* It's a set of instructions that humans can use to communicate with computers.
* It allows us to create programs, which are sets of instructions that tell a computer what to do.
* It offers a structured way to write code that machines can understand and execute.

**Interpreters vs. Compilers:**

These are two different ways to translate code written in a programming language into machine language that a computer can execute.

### 1. Interpreter

* Translates code one line at a time, executing each instruction as it goes.
* No separate machine code file is generated.
* Pros:
    - Faster to start running code.
    - Easier to debug, as errors are reported line by line.
    - More adaptable to changes (no need to recompile).
* Cons:
    - Generally slower execution speed compared to compiled code.
    - Source code might be less secure as it's visible during execution.


### 2. Compiler

* Translates the entire code into machine code before execution.
* Creates a separate executable file that can run independently.
* Pros:
    - Faster execution speeds.
    - Source code can be protected (not distributed).
    - More efficient use of memory.
* Cons:
    - Takes longer to create the executable file.
    - Debugging can be more challenging as errors are reported after the entire code is compiled.

**Examples of compiled languages:** C, C++, Java, Go

**Key Differences Summary:**

| Feature        | Interpreter                       | Compiler                                       |
|----------------|-----------------------------------|------------------------------------------------|
| Translation    | Line by line                       | Entire code at once                             |
| Execution      | During translation                 | After translation                               |
| Output         | No separate machine code file      | Separate executable file                       |
| Speed          | Generally slower                   | Generally faster                                |
| Debugging      | Easier (errors reported as they occur) | More challenging (errors reported after compilation) |
| Security      | Source code potentially less secure | Source code can be protected                    |
| Flexibility    | More adaptable to changes          | Requires recompilation for changes              |

**Hybrid Approaches:**

* Some languages, like Java, use a combination of compiling and interpreting.
* Code is first compiled into bytecode, which is then interpreted by a virtual machine.
* This approach offers some benefits of both compilers and interpreters.


## Famous Interpreted Languages (2024)

| Language | Description | Year of Creation |
|---|---|---|
| Python | General-purpose, user-friendly, popular for web dev, data science, and scripting | 1989 |
| Julia | High-performance, dynamic typing, strong in scientific computing and machine learning | 2011 |
| Bash | Shell scripting for Unix-like OS, automation, system administration | 1989 |
| JavaScript | Dominant language for web development, interactive web pages, and client-side applications | 1995 |
| Ruby | Elegant syntax, strong community, popular for web dev with Ruby on Rails | 1993 |

## Modern Compiled Languages (2024)

| Language | Description | Year of Creation |
|---|---|---|
| Go | A fast, concurrently compiled language with simple syntax, static typing, and garbage collection. Great for web services, network applications, and command-line tools. | 2009 |
| Rust | A systems programming language focused on memory safety and concurrency, offering zero-cost abstractions and ownership to eliminate common errors. Suitable for high-performance systems, operating systems, and embedded systems. | 2010 |
| Zig | A general-purpose compiled language aiming for simplicity, expressiveness, and performance, featuring direct memory manipulation and meta-programming capabilities. Ideal for game development, systems programming, and embedded systems. | 2015 |
| Swift | A modern, open-source language for building powerful applications for Apple platforms (iOS, macOS, watchOS, tvOS) and beyond. Emphasizes clean syntax, safety, and interoperability with C and Objective-C. | 2014 |
| Carbon | A new systems programming language aiming to bridge the gap between safety and expressiveness (like Rust) and raw power and efficiency (like C++). Emphasizes zero-cost abstractions and static memory safety. Designed for system libraries, high-performance applications, and interoperability with C++. | 2022 |

We will explain syntax of these modern languages!

---

You should learn at least one interpreted language and two or 3 compiled languages. Our favorite languages will get more attention in articles. Julia is our favorite language. We endorse this language and we make examples of code to explain Computer science using Julia.

