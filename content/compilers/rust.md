+++
title = "rust language"
collection = "compilers"
author = "Bard/Gemini"
date = 2023-12-26
weight = 54
chapter = false
disableToc = false
pre = "<b>📜</b>"
tags = ["rust", "compilers"]
description = "Rust programming language overview"
+++

 **Here's a Rust program that defines a Fibonacci function and calls it:**

```rust
fn main() {
    // Prompt the user to enter a positive integer
    println!("Enter a positive integer:");

    let mut input = String::new();

    // Read the user's input
    std::io::stdin().read_line(&mut input).expect("Failed to read input");

    // Parse the input as a u32 (unsigned 32-bit integer)
    let n: u32 = match input.trim().parse() {
        Ok(num) => num,
        Err(_) => {
            // Handle invalid input
            println!("Invalid input. Please enter a positive integer.");
            return;
        }
    };

    // Calculate the nth Fibonacci number using the recursive fib function
    let result = fib(n);

    // Print the result
    println!("The {}th Fibonacci number is {}", n, result);
}

// Define the recursive Fibonacci function
fn fib(n: u32) -> u32 {
    // Base cases:
    if n == 0 {
        return 0;
    } else if n == 1 {
        return 1;
    } else {
        // Recursively calculate the Fibonacci numbers
        return fib(n - 1) + fib(n - 2);
    }
}
```

**Explanation:**

1. **Imports:** The code implicitly imports the `std::io` module for input/output operations.
2. **Main Function:**
   - Prompts the user to enter an integer.
   - Reads the input using `std::io::stdin().read_line()`.
   - Parses the input into a `u32` integer using `parse()`.
   - Handles potential parsing errors with `match`.
   - Calls the `fib` function to calculate the Fibonacci number.
   - Prints the result.
3. **fib Function:**
   - Recursively calculates the nth Fibonacci number using base cases for 0 and 1.
   - Returns the calculated Fibonacci number.

**To run this program:**

1. Save it as `main.rs`.
2. Open a terminal in the directory where you saved the file.
3. Run `rustc main.rs` to compile the code.
4. Run `./main` to execute the program.
