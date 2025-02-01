## 💡 Foundations of Recursion

- **Recursion** is when something is defined in terms of itself.
- It represents a new way of thinking and a powerful programming paradigm.
- Recursion enables reasoning about correctness and gives insight into the nature of computation.
- Many computational artifacts are naturally self-referential, such as file systems, fractal patterns, and divide-and-conquer algorithms.
- A **recursive program** has two key components: a **base case** and a **reduction step**.
    - The **base case** returns a value for small inputs without making any further recursive calls.
    - The **reduction step** uses the function to compute a return value for the input, assuming it works for smaller values.

## 🔢 Example: Integer to Binary Conversion

- A classic example is converting an integer to its binary representation.
- The `convert(int N)` method recursively converts an integer `N` to a binary string.
    - If `N` is 1, it returns `"1"` (base case).
    - Otherwise, it returns `convert(N/2) + (N % 2)` (reduction step).
- The method can be proven correct using **mathematical induction**.
- **Mathematical induction** involves:
    - Proving a base case for a specific value of `N`.
    - Assuming the statement is true for all integers less than `N` and proving it for `N`.

## ⚙️ Mechanics of a Function Call

- When a function is called, the system saves the current environment, including variable values and the call location.
- It initializes argument variables, transfers control to the function, and, after execution, restores the environment and returns control to the calling code.
- This mechanism allows recursive calls to function correctly because the system handles the environment of each call separately.

## ⚠️ Potential Pitfalls of Recursion

- **Missing base case:** A recursive function without a base case will cause infinite recursion.
- **No convergence guarantee**: A function may not converge to the base case, leading to an infinite loop.
- **Excessive memory requirements**: If a function calls itself recursively an excessive number of times before returning, the memory required by Java to keep track of the recursive calls may be prohibitive.
- **Excessive recomputation:** Simple recursive programs can require exponential time due to recomputing the same subproblems. For example, the naive recursive Fibonacci calculation is highly inefficient.

## 📐 Classic Example: Ruler Subdivision

- The `ruler(int n)` function creates subdivisions of a ruler to 1/2^n inches.
    - For `n = 0`, it returns a space.
    - Otherwise, it sandwiches `n` between two copies of `ruler(n-1)`.
- **Tracing a recursive program** can be done with a recursive call tree, where each node represents a call and is labeled with its return value.

## 🗼 Towers of Hanoi

- The **Towers of Hanoi** puzzle involves moving disks from one post to another using a third post, without placing a larger disk on a smaller one.
- A recursive solution involves:
    - Moving `n-1` disks to the left (recursively).
    - Moving the largest disk to the right.
    - Moving `n-1` disks to the left again (recursively).
- The `hanoi(int n, boolean left)` function prints the moves for `n` disks, using `L` for left and `R` for right.
- The recursive call tree has a structure similar to the ruler function, illustrating several facts:
    - Each disk always moves in the same direction.
    - Moving a smaller disk always alternates with a unique legal move.
    - Moving `n` disks requires 2^n - 1 moves.

## 🎨 Recursive Graphics

- Simple recursive drawing schemes can create complex and intricate patterns.
- **H-trees** are a "Hello, World" of recursive graphics.
    - An H-tree of order `n` draws an H, then recursively draws four H-trees of order `n-1` at the tips of the H.
- Recursive graphics have applications like connecting regularly spaced sites to a single source.
- **Fractional Brownian motion** is a recursive process that models natural phenomena like stock prices, fluid dispersion, mountains, and nerve membranes.
    - The midpoint displacement method involves perturbing the midpoint of a line segment by a random value and recursing on the subintervals.
- A 2D version is used to generate **plasma clouds**, where a rectangle's midpoints are colored by averaging endpoint colors and the center pixel is perturbed randomly and the method is applied recursively to the four quadrants.

## 📉 Avoiding Exponential Waste

- The naive recursive computation of **Fibonacci numbers** is highly inefficient due to excessive recomputation.
- **Memoization** is a technique to avoid recomputation by storing previously computed values in an array.
- Dynamic programming provides an alternative to recursion by building computations from the "bottom up".

## 🧮 Dynamic Programming

- **Dynamic programming** solves problems by combining solutions to smaller subproblems, typically in a bottom-up fashion.
- It involves:
    - Solving small subproblems and saving the solutions.
    - Using these solutions to build bigger solutions.
- Dynamic programming avoids recomputation, making it more efficient than naive recursion.
- The **longest common subsequence (LCS)** problem is an example of where dynamic programming can be applied.
    - The goal is to find the longest string that is a subsequence of two given strings.
    - Dynamic programming efficiently computes the length of the LCS by keeping track of lengths of LCS of the tails of the two strings.

## ⚖️ Recursion vs. Dynamic Programming

- Both recursion and dynamic programming are useful for combining solutions to subproblems.
- **Recursion** is often simpler for decomposition and reasoning about correctness, but may lead to exponential waste.
- **Dynamic programming** avoids exponential waste and can be simpler than memoization, but decomposition may not be so simple.

## 🔑 Key Concepts

- **Recursion:** Defining something in terms of itself.
- **Base case:** The condition that stops recursion.
- **Reduction step:** Recursive call with a smaller argument.
- **Mathematical induction:** Technique for proving correctness of recursive programs.
- **Memoization:** Storing previously computed values to avoid recomputation.
- **Dynamic programming:** Building solutions from the bottom up to avoid recomputation.
- **Recursive graphics:** Using recursion to generate patterns.
- **Towers of Hanoi:** Classic puzzle to demonstrate recursion.
