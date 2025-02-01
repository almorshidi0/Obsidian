## 🗣️ The Tower of Babel

- The lecture begins with the story of the Tower of Babel, where a single language was believed to grant people the ability to achieve anything they imagined.
- **Yahweh** "confounded the language of all the earth".
- The story suggests that the **proliferation of cultural differences and multiple languages** is a basis of civilization. This idea is extended to programming languages, where diversity can foster innovation.

## 🧰 Many Ways to Solve a Problem

- Just like there are many ways to get from one place to another (rollerskates, cars, planes), there are many ways to solve a programming problem.
- Different programming languages are appropriate for different tasks.
    - Examples: **C, Java, MATLAB, C++, Python**

## 💻 Programming Languages: A Tour

This section looks at different programming languages, highlighting their syntax, structure, and key differences.

### Java

- You can write Java code.
- The lecture uses the `ThreeSum` program as a running example.
    - This program reads integers from standard input and prints triples that sum to zero.
- Java code is compiled using `javac` and executed using `java`.

### C

- You can also write C code.
- C code for the `ThreeSum` problem is presented, with differences highlighted in red.
    - Differences include:
        - **Library conventions**: `#include <stdio.h>`
        - **Array creation**: `int *a = malloc(N*sizeof(int));`
        - **Standard input**: `scanf("%d", &a[i]);`
        - **Pointer manipulation** (using `*` and `&`).
- C code is compiled using `cc` and executed with `a.out`.
- **Key Difference**: C has no data abstraction and a C program is a set of static methods.

### C++

- You can also write C++ code.
- C++ adds **data abstraction to C** and is often described as "C with classes".
- The lecture shows a `ThreeSum` example in C++, highlighting differences.
    - Differences include:
        - **Library conventions**: `#include <iostream>`
        - **Standard input**: `std::cin >> a[i];`
        - **Standard output**: `std::cout << a[i] << ...`
- C++ code is compiled with `cpp` and executed with `a.out`.
- C++ also has **pointer manipulation**.
- C++ can be used like C, or with objects, as shown with the example of a binary search tree.
- **Challenges in C++**: pointer manipulation, templates/generics.

### C/C++ Memory Management

- In **C/C++, the programmer is responsible for memory allocation**.
    - Programs manipulate pointers, explicitly calling methods to allocate and free memory for objects.
    - This can lead to **memory leaks** if not managed properly.
    - Example: `calloc` and `free` are used to manage memory.
- **Java uses automatic "garbage collection"**, where the system keeps track of references and reclaims memory that is no longer accessible.
    - This frees the programmer from explicit memory management.

### Python

- You can use Python, and you can write Python code.
- Python can be used like a **calculator**.
    - It has an interactive mode where expressions can be evaluated directly.
- The lecture provides a `ThreeSum` program example.
- **Notable differences in Python**:
    - **No braces** (indents instead).
    - **No type declarations** (dynamic typing).
    - **Array creation** `a = *N`.
    - **I/O idioms** `stdio.readInt()`.
    - **for (iterable) idiom** `for i in range(N):`.
- Python code is executed by an **interpreter**, not a compiler.

### Compilation vs. Interpretation

- A **compiler** translates the entire program to (virtual) machine code.
    - Examples: `javac` (Java), `cc` (C).
- An **interpreter** simulates the operation of a (virtual) machine running your code.
    - Examples: `java` (Java), `python` (Python).

### Python Type Checking

- Python has **no compile-time type checking**.
    - Type errors are only checked at **run-time**.
- This makes it easier to write small programs but more difficult to debug large ones.
- **Typical nightmare scenario**: a small type error in a big program can cause a crash after hours of running.
- **Reasonable approaches**:
    - Use Python like a calculator.
    - Prototype in Python, then convert to Java for "production" use.

### Matlab

- You can also write MATLAB code, using it like Java.
- MATLAB is commonly used for **matrix processing**.
    - Example: Matrix multiplication `C = A*B`.
- **Big differences between Matlab and other languages**:
    - **Not free**.
    - Most programmers use only one data type (**matrix**).
- MATLAB is written in Java, and Java compilers are written in C.
- **Reasonable approaches**:
    - Use MATLAB as a "matrix calculator" if you own it.
    - Convert to Java/C/C++ for other tasks.

## 🧐 Why Java?

- Java is **widely used and available**, has been under continuous development for decades, embraces modern abstractions, and has automatic checks for program mistakes.
- It is used in many applications (Mars rover, cell phones, medical devices, supercomputing, etc.).
- Java has a full set of modern abstractions, modern libraries and systems and automatic checks for bugs.
- Other languages have drawbacks in these areas: C lacks objects, MATLAB has limited libraries, Python's abstractions may not be fully embraced, and C/C++ require manual memory management.

## 📚 Why Learn Another Programming Language?

- Offers something new.
- Need to interface with co-workers.
- Better than Java for the application at hand.
- Provides an intellectual challenge.
- Opportunity to learn something about computation.
- Introduces a new programming style.

## 🧮 Programming Styles

- **Procedural**: step-by-step instruction execution (usually compiled).
    - Examples: C, early Java.
- **Scripted**: step-by-step command execution (usually interpreted).
    - Examples: Python, Ruby.
- **Special-purpose**: optimized around certain data types.
    - Example: MATLAB for matrices.
- **Object-oriented**: focuses on objects that do things.
    - Examples: C++, Java.
- **Functional**: treats computation as evaluation of functions, avoids side effects.

## 💡 Object-Oriented Programming (OOP)

- A different philosophy of programming from procedural styles.
- **OOP**: software is a simulation of the real world.
- **Procedural**: tell the computer to do this, then that. (verbs oriented).
- **OOP**: identify things (nouns), which have properties (instance variables) and do things (methods).
- **Essential features of OOP**:
    - **Encapsulation**: hides information to make programs robust.
    - **Type checking**: avoids and finds errors.
    - **Libraries**: reuses code.
    - **Immutability**: guarantees stability of program data.
- OOP emerged due to good answers to the questions: is it easy to write, maintain, and is it correct/efficient.
- **OOP Pioneers**:
    - **Kristen Nygaard and O.J. Dahl** (Simula): invented OOP for simulation.
    - **Alan Kay** (Smalltalk): promoted OOP for widespread use.
    - **Barbara Liskov** (CLU): pioneered data abstraction.
- **Alan Kay's Vision:** Dynabook, a notebook-like device with OOP software.
- Key idea: "The best way to predict the future is to invent it".

## 🔍 Type Checking

- **Static (compile-time) type checking** (e.g., Java):
    - Variables have declared types.
    - Type errors are checked at compile time.
- **Dynamic (run-time) type checking** (e.g., Python):
    - Values have types, not variables.
    - Type errors are checked at run-time.
- **Debate**: Is static typing worth the trouble?
    - Compiled code more efficient? Type-checked code more reliable? Generics too difficult with static typing?
- **Dijkstra** argued program testing is inadequate to show the absence of bugs.
- **Python bloggers** say static type checking is redundant with automated testing.
- **Dave Walker** argues that static type checking is a complementary form of testing, scales well, and can guarantee the absence of certain classes of bugs.
- **Hungarian type system**: encodes type in first characters of a variable name (used in early Microsoft Word).

## ⚙️ Functional Programming

- Treats computation as evaluation of functions.
- Avoids side effects and mutable types.
- Has an on-demand execution model ("what" rather than "how").
- **Advantages**:
    - Functions are first-class entities (arguments, return values, data).
    - Often leads to more compact code.
    - Easier reasoning about correctness.
    - Supports concurrency (programming on multiple processors).
- **Examples**:
    - Python `square()` and `table()` functions show how functions can be passed as arguments.
    - The `map()` operation applies a function to every element of a list.
    - The `reduce()` operation combines elements of a list using a function.
- **MIT** used Scheme (a functional language) in its introductory CS course.
- **Modern applications**: communications systems, financial systems, Google MapReduce.

## 🤔 The Tower of Babel Revisited

- Is a single programming language capable of doing anything we imagine?.
- Is the proliferation of languages a basis for civilization in programming?.
- Programming languages are a rich and diverse field.
- Specialization is for insects!

## 🔑 Key Takeaways

- Many programming languages exist, each with its own strengths and weaknesses.
- **Java** is a good general-purpose language that embraces modern abstractions.
- **C/C++** require manual memory management but offer low-level control.
- **Python** is easy to use for small programs but can be problematic for large ones, due to lack of compile-time type checking.
- **MATLAB** is designed for matrix processing and not free.
- **Object-oriented programming** is a dominant paradigm that simulates real-world entities.
- **Functional programming** treats computations as function evaluations and facilitates concurrency.
- Type checking can happen at compile-time (static) or run-time (dynamic), each with pros and cons.
- Learning multiple programming languages can enhance your understanding of computation and programming.
