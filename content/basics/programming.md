+++
title = "Programming"
collection = "basics"
author = "Bard/Gemini"
date = 2023-12-26
weight = 2
chapter = false
disableToc = false
pre = "<b>📜</b>"
tags = ["programming", "basics"]
description = "Top programming languages"
+++

In this article we investigate several programming languages. We will understand the difference between them and we will try to explain why we have so many programming languages. Our favorite programming language is Julia. We will explain why and we will try to motivate you to learn multiple programming languages. We think a software engineer should know at least 3 programming languages.


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

## Famous Languages (2024)

We do not have evidence and data ourselves but we check [tiobe index](https://www.tiobe.com/tiobe-index/) to verify our assumptions. You can do the same and asses what language is famous and what is the trend. We have created two lists:

###  Interpreted Languages 

| Language | Description | Year of Creation |
|---|---|---|
| Python | General-purpose, user-friendly, popular for web dev, data science, and scripting | 1989 |
| Julia | High-performance, dynamic typing, strong in scientific computing and machine learning | 2011 |
| Bash | Shell scripting for Unix-like OS, automation, system administration | 1989 |
| JavaScript | Dominant language for web development, interactive web pages, and client-side applications | 1995 |
| Ruby | Elegant syntax, strong community, popular for web dev with Ruby on Rails | 1993 |

### Compiled Languages

| Language | Description | Year of Creation |
|---|---|---|
| Go | A fast, concurrently compiled language with simple syntax, static typing, and garbage collection. Great for web services, network applications, and command-line tools. | 2009 |
| Rust | A systems programming language focused on memory safety and concurrency, offering zero-cost abstractions and ownership to eliminate common errors. Suitable for high-performance systems, operating systems, and embedded systems. | 2010 |
| Zig | A general-purpose compiled language aiming for simplicity, expressiveness, and performance, featuring direct memory manipulation and meta-programming capabilities. Ideal for game development, systems programming, and embedded systems. | 2015 |
| Swift | A modern, open-source language for building powerful applications for Apple platforms (iOS, macOS, watchOS, tvOS) and beyond. Emphasizes clean syntax, safety, and interoperability with C and Objective-C. | 2014 |
| Carbon | A new systems programming language aiming to bridge the gap between safety and expressiveness (like Rust) and raw power and efficiency (like C++). Emphasizes zero-cost abstractions and static memory safety. Designed for system libraries, high-performance applications, and interoperability with C++. | 2022 |

---

## Generations of languages

Programming languages have evolved through generations, each offering increased abstraction and ease of use:

* **First Generation (1GL):** Machine code - Direct instructions for the hardware, requiring detailed understanding of the machine's architecture. (e.g., assembly language)
* **Second Generation (2GL):** Assembly mnemonics - Symbolic abbreviations for machine code instructions, making programs slightly more readable. (e.g., MACRO-32)
* **Third Generation (3GL):** High-level languages - Instructions closer to natural language, focusing on logic and algorithms rather than hardware specifics. (e.g., C, Java, Python)
* **Fourth Generation (4GL):** Very high-level languages - Further abstraction for specific domains like databases or web development, often with pre-built functions and declarative syntax. (e.g., SQL, HTML)
* **Fifth Generation (5GL):** Natural language programming - Aiming for programming in natural language like English, still under development.

### Domain-Specific Languages (DSLs):

DSLs are specialized languages designed for a specific domain or problem area, offering conciseness and expertise-specific constructs. Examples include:

* **SQL:** Querying databases
* **Verilog/VHDL:** Hardware design
* **MATLAB/Octave:** Matrix manipulation
* **HTML/CSS:** Web development

### Other Classifications:

Programming languages can be further categorized by:

* **Paradigm:** Imperative, functional, object-oriented, declarative, etc.
* **Typing:** Statically typed, dynamically typed, untyped
* **Compilation vs. Interpretation:** Compiled to machine code for execution, interpreted directly by the computer
* **Concurrency:** Ability to handle multiple tasks simultaneously

### Why so many languages?

Several factors contribute to the abundance of programming languages:

* **Evolving needs:** New hardware, platforms, and domains require specialized tools.
* **Innovation:** Developers seek better ways to express ideas and improve program efficiency.
* **Readability and maintainability:** New languages address shortcomings of existing ones for specific tasks.
* **Community and popularity:** Some languages thrive due to large communities and ecosystem support.

Ultimately, the variety of languages reflects the constantly evolving nature of software development and the diverse needs of programmers. New languages emerge to address specific problems or offer more elegant solutions, while established languages remain relevant for their proven reliability and broad communities.

---

## Sage-Code Research

Do you ever look at a programming language and think, "There's gotta be a better way"? Join Sage-Code, a collective of veteran developers on a mission to do just that. We're not just talking tweaks and patches; we're talking about reimagining what programming can be – easier, more intuitive, and downright *fun*.

Forget steep learning curves and arcane syntax. We believe everyone deserves the power to create with code, not just the coding elite. That's why we're building languages from the ground up, focused on:

* **Effortless Learning:** Forget tutorials that feel like climbing Mount Syntax. We're crafting languages that speak your language, making coding as natural as reading.
* **Memory-Friendly Design:** No more cramming cryptic keywords. Our languages are intuitive and logical, letting your code practically write itself (almost!).
* **Fun Factor on High:** Coding shouldn't be a chore! We're injecting joy into the process, making building software an experience you'll actually look forward to.

But don't think of us as lone inventors toiling in a basement. We're a community, and we need your passion! Whether you're a seasoned pro or a curious newcomer, your unique perspective is the missing piece in our puzzle.

**Here's what awaits you at Sage-Code:**

* **Work with the best:** Collaborate with seasoned developers who have seen the inside of every compiler and lived to tell the tale. Learn from their experience, shape the future of coding alongside them.
* **Be a pioneer:** Contribute to languages that haven't even been written yet! Your ideas could shape the foundation of how millions code in the future.
* **Leave your mark:** Make a real difference in the world of technology. Help us democratize programming and empower everyone to unleash their creativity through code.

**This isn't just about building languages; it's about building a better future for software development.** Join us, and let's create a world where anyone can code, anyone can innovate, and anyone can build their dreams with lines of beautiful, intuitive code.

**Ready to be part of the revolution?** Visit our website and discover how you can contribute. Together, we can rewrite the rules of coding, one line at a time.

**Remember,** the future of programming isn't just written, it's built. **Build it with us.**


**We can't wait to welcome you to the Sage-Code core team!**

---

You should learn at least one interpreted language one compiled language and some domain specific languages for your career in tech. Our favorite languages will get more attention in future articles. Learn and prosper 🖖