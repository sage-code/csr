+++
title = "go language"
collection = "compilers"
author = "Bard/Gemini"
date = 2023-12-26
weight = 52
chapter = false
disableToc = false
pre = "<b>📜</b>"
tags = ["go", "compilers"]
description = "co programming language overview"
+++

## Fibonacci Sequence in Go

Here's a Go program that defines and calls a Fibonacci function:

```go
package main

import (
  "fmt"
  "strconv"
)

func main() {
  // Prompt user for a positive integer
  fmt.Println("Enter a positive integer:")

  var input string
  fmt.Scanln(&input)

  // Parse input as integer
  n, err := strconv.Atoi(input)
  if err != nil {
    fmt.Println("Invalid input. Please enter a positive integer.")
    return
  }

  // Calculate the nth Fibonacci number
  result := fibonacci(n)

  // Print the result
  fmt.Printf("The %dth Fibonacci number is %d\n", n, result)
}

func fibonacci(n int) int {
  if n == 0 {
    return 0
  } else if n == 1 {
    return 1
  } else {
    return fibonacci(n-1) + fibonacci(n-2)
  }
}
```

**Explanation:**

* **Imports:** `fmt` for input/output, `strconv` for string conversion.
* **Main Function:**
    * Prompts for a positive integer.
    * Reads input using `fmt.Scanln`.
    * Parses input to `int` using `strconv.Atoi`.
    * Handles potential errors with `err` check.
    * Calls `fibonacci` function with the parsed number.
    * Prints the result with formatted string.
* **fibonacci Function:**
    * Defines a recursive function with base cases for 0 and 1.
    * Returns the sum of previous two Fibonacci numbers for other cases.

**Running the program:**

1. Save the code as `main.go`.
2. Open a terminal in the directory with the file.
3. Run `go run main.go` to execute the program.
4. Enter a positive integer and see the corresponding Fibonacci number displayed.

This program follows a similar structure to the Rust version, demonstrating a recursive approach to calculating Fibonacci numbers in Go.
