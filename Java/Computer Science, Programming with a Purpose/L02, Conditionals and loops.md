## 🧱 Building Blocks for Programming

- This lecture builds upon the basic programming skills from the previous lecture, such as primitive data types, math and text I/O, and assignment statements.
- These basic skills are equivalent to a calculator but now we're going to go "to infinity and beyond!" with **conditionals and loops**.
- Conditionals and loops allow for much more complex control flow.

## 🚦 Control Flow

- **Control flow** is the sequence of statements that are executed in a program.
- Conditionals and loops enable us to choreograph the control flow.
- Before, programs had a **straight-line control flow**, executing one statement after another.
- With conditionals and loops, the control flow can be much more complex, enabling richer calculations.

## 🚥 Conditionals: The `if` Statement

- The `if` statement executes certain statements depending on the values of certain variables.
    
- It evaluates a **boolean expression**.
    
- If the expression is true, it executes a statement.
    
- The `else` option allows execution of a different statement if the boolean expression is false.
    
- **Example:** `if (x < 0) x = -x;` This replaces `x` with its absolute value.
    
- **Example with else:** Computes the maximum of `x` and `y`.
    
    ```
    if (x > y) {
        max = x;
    } else {
       max = y;
    }
    ```
    
- **Example: Coin Flip** Simulates a coin flip using `Math.random()` and an `if-else` statement.
    
- **Good Practice**: Use conditionals to check for and avoid runtime errors, like division by zero.
    

### 📝 `if` statement Pop Quiz

- **TwoSort**: Reads two integers from the command line and prints them in numerical order using an `if` statement to exchange values if needed.
- **ThreeSort**: Puts three numbers in numerical order using three `if` statements.
- **IntOps**: Uses an `if-else` statement to avoid division by zero by checking if the denominator is zero.

## ₔ Loops: The `while` Statement

- The `while` loop executes certain statements repeatedly until certain conditions are met.
- It evaluates a **boolean expression**.
- If true, it executes a sequence of statements.
- Then repeats until the boolean expression is false.
- **Example:** Prints powers of two.
    
    ```
    int i = 0;
    int v = 1;
    while (i <= n) {
        System.out.println(v);
        i = i + 1;
        v = 2 * v;
    }
    ```
    
- **Trace**: A table of variable values after each statement, which is useful for understanding loop behavior.
- **Infinite loops**: Forgetting braces in while loops can lead to infinite loops that will keep printing the same result. You may need to use a command like Ctrl-C to stop the program.

### ➗ Example: Implementing Square Root with `while` loop

- **Newton-Raphson Method:** An iterative method to compute the square root of a number.
    - Initialize t₀ = c.
    - Repeat until tᵢ ≈ c/tᵢ : set tᵢ₊₁ to be the average of tᵢ and c/tᵢ.
- **Why it works**: If t = c/t, then t² = c.
- The while loop is useful for performing iterative calculations.
- Scientists studied computation well before the advent of computers.
- This method works to find the root of any function f(x) (value of x for which f(x) = 0).

## ➿ An Alternative: The `for` Loop

- The `for` loop is an alternative repetition structure.
- It has an initialization statement, a boolean expression, and an increment statement.
- **Structure**:
    
    ```
    for (initialization; boolean expression; increment) {
        // sequence of statements
    }
    ```
    
- **Every `for` loop has an equivalent `while` loop**.
- It can provide more compact and understandable code.

### ⚙️ Examples of `for` loop use

- **Compute sum (1 + 2 + ... + N)**.
- **Compute N! (1 * 2 * ... * N)**.
- **Print a table of function values**.
- **Subdivisions of a ruler**. The ruler program can produce a huge amount of output with a small amount of code.
- **Fibonacci numbers**: The program uses a `for` loop to print the first 11 Fibonacci numbers.
    
    ```
    int f = 0, g = 1;
    for (int i = 0; i <= 10; i++) {
        System.out.println(f);
        f = f + g;
        g = f - g;
    }
    ```
    

## 🪆 Nesting

- Any statement within a conditional or loop may itself be a conditional or a loop statement.
- Enables complex control flows.
- Adds to the challenge of debugging.
- **Example**: `if-else` statement within a `while` loop within a `for` loop.

### 🧾 Example of Nesting Conditionals: Tax Rate Calculation

- **Goal**: Calculate the proper tax rate based on income.
    
- Uses nested `if-else` statements to test among mutually exclusive possibilities.
    
    ```
    if (income < 47450) {
      rate = 0.22;
    } else {
      if (income < 114650) {
          rate = 0.25;
      } else {
         if (income < 174700) {
             rate = 0.28;
         } else {
            if (income < 311950) {
              rate = 0.33;
            } else {
              rate = 0.35;
            }
          }
      }
    }
    ```
    
- **Pop Quiz**: Need `else` clauses in nested `if` statements. Without them, code is equivalent to just the last `if` statement.
    
- Braces are not needed in this case but be careful about ambiguity with nesting.
    

### 🎰 Example of Nesting Conditionals and Loops: Gambler's Ruin

- **Problem:** Simulate a gambler making a series of fair $1 bets until they either go broke or reach a goal.
- **Monte Carlo Simulation:** Use a simulated coin flip and repeat to compute statistics.
- The code involves a `for` loop, a `while` loop within the `for` loop and an `if` statement within the `while` loop.
- The simulation can validate mathematical analysis and is useful for more complicated scenarios.
- **Mathematical Analysis**: Probability of winning = stake / goal; expected number of bets = stake * desired gain.
- Computer simulation can help validate mathematical analysis, and it may be the best approach for more complicated variants.

## 🐞 Debugging

- Debugging is a major part of program development, even for experts.
- A **bug** is a mistake in a program.
- **Debugging** is the process of eliminating bugs.
- Conditionals and loops dramatically increase the number of possible outcomes, making debugging more challenging.
- Most programs contain numerous conditionals and loops with nesting.
- **Good news**: Conditionals and loops provide structure that helps us understand our programs.

### 📜 Debugging a program: running example

- **Problem:** Factor a large integer `n`.
- **Method:** Consider each integer `i` less than `n`, print `i` as a factor while it divides `n` evenly, and replace `n` with `n/i`.
- Security of internet commerce depends on the difficulty of factoring large integers.
- The example program has bugs and goes through the process of debugging to fix them.

### 🛠️ Debugging Steps:

1. **Syntax Errors:** Is your program a legal Java program? Use the compiler to find syntax errors and fix them.
    - The compiler will point to the first error it finds.
    - Example: Missing semicolons and missing type declarations.
2. **Runtime and Semantic Errors**: Does your legal Java program do what you want it to do? Run it to find out.
    - Find the first runtime error (if any).
    - Example: `ArrayIndexOutOfBoundsException` due to missing command-line argument, division by zero.
3. **Testing**: Does your legal Java program always do what you want it to do? Test on many types of inputs.
    - Add trace code to find the first error.
    - Example: The need to print out the value of `n` if it is not equal to 1 after dividing.
4. **Performance**: Is the program efficient enough to solve the problem?
    - Test on increasing problem sizes.
    - May need to adjust the method for solving the problem.
    - Example: Modify the for loop to stop when `i * i` is greater than `n`.

### 📝 Debugging your program: Summary

- Program development is a four-step process with feedback.
- **EDIT:** Write or modify the code.
- **COMPILE:** Translate the code into machine-readable instructions, fix syntax errors, and repeat.
- **RUN:** Test if the code runs as imagined, fix runtime or semantic errors and repeat.
- **TEST:** Test for performance, fix errors and repeat.
- **SUBMIT:** Submit your program for independent testing and approval once you are satisfied with the results.

## 🔑 Key Concepts

- **Conditionals (`if` statements)** allow programs to make decisions based on conditions.
- **Loops (`while` and `for` statements)** allow programs to repeat a block of code multiple times.
- **Nesting** allows conditionals and loops within other conditionals and loops.
- **Debugging** is a critical part of the programming process.
