This episode dives into the essential building blocks of programming languages, moving beyond the low-level details of machine code.

## Core Concepts 🧠

- **Statements:** Like sentences in spoken language, statements are individual instructions in a programming language.
    
    - Example: `a = 5` (assigning the value 5 to variable 'a')
- **Syntax:** The rules that govern how statements are structured. Every language, including programming languages, has syntax.
    
    - Just like "I want to eat" makes sense but "I want rain" doesn't
- **Variables:** Named storage locations for values. You can use any names, but it's best to use descriptive names, like `apples`, `pears`, `fruits`, for clarity.
    
    - Example: `level = 1`, `score = 0`, `bugs = 5`
- **Programs:** A list of instructions, executed sequentially, like following a recipe.
    

## Control Flow 🚦

- **Control Flow Statements:** Used to control the order in which statements are executed, instead of simply running top to bottom.
- **`if` Statements:** Execute a block of code only if a condition is true.
    - Think of them as a fork in the road where the path is determined by whether a condition is true or false.
    - Example: `if level is 1 then set score to 0`
- **`if-else` Statements:** Execute one block of code if a condition is true, and another if it's false.
    - If the level is not 1, a different set of instructions will be executed
- **`while` Loops:** Repeat a block of code as long as a condition is true.
    - Example: Increase the number of relays until the max is reached
- **`for` Loops**: Repeats a block of code a specific number of times. It's count controlled, unlike while loops.
    - Example: looping 10 times

## Functions 📦

- **Functions (also called methods or subroutines):** Named blocks of code that perform a specific task.
    
    - Help to compartmentalize code, hide complexity, and make code reusable.
- **Abstraction:** Packaging up complex code into functions allows programmers to use the functionality without needing to see the internal details.
    
    - Moving up a new level of abstraction to compartmentalize and hide complexity.
- **Example:** A function that calculates exponents.
    
    - Instead of specific variable names like relays and levels, use generic names like `base` and `x`.
    - Functions use a `return` statement to send the result back to where the function was called.
- **Calling Functions:** You can use a function by simply calling its name and providing the necessary input.
    
    - Example: `exponent(2, 44)` to calculate 2 to the 44th power
- **Functions Calling Functions** Functions can be nested, one function can call another function and so on.
    
    - By wrapping code in a function it hides all the complex processes that lead to the output

## Code Organization 🗂️

- **Modularity:** Breaking programs into functions allows for better organization, readability, and teamwork.
- **Smaller Functions:** Modern programming favors smaller functions (around 100 lines or less).
    - If a function gets too large, it should likely be broken down into smaller functions.
- **Libraries:** Collections of pre-written functions that provide common functionality, saving developers time and effort. These are written by experts and rigorously tested.
    - Libraries exist for networking, graphics, sound, and more.
    - In the real world programmers don't waste time writing things like exponents since libraries already provide those

## Key Takeaway 🎉

The power of abstraction and functions is the essence of modern programming. Functions help programmers to manage complexity in modern software by:

- hiding complexity
- promoting modularity
- making code reusable.
