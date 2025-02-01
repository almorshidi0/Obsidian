## 🤔 Why Programming?

- **Empowerment**: Programming lets you tell a computer exactly what you want it to do. Instead of being limited to pre-packaged solutions (apps), you can create custom solutions tailored to your specific needs.
- **Creative Outlet**: Programming is a natural, satisfying, and creative experience, similar to writing a sonnet or paragraph.
- **New Worlds**: It enables accomplishments not otherwise possible and opens up new avenues of intellectual exploration.
- **Ubiquity**: Computers are everywhere, and understanding how to program is essential for everyone.
- **Human-Computer Communication:** The goal of programming is to explain to a human what we want a computer to do.

> _"Specialization is for insects."_ - Robert A. Heinlein 🐜➡️🧑‍💻

## ⚙️ How to Tell a Computer What to Do

- **Natural Language:** Easy for humans but error-prone for computers 🗣️.
    - Example: _"Kids Make Nutritious Snacks"_ - actual newspaper headline showing how computers can misinterpret human language.
- **Machine Language:** Easy for computers but error-prone for humans 🤖.
    - Low-level code that directly tells the computer what to do.
    - Example: Adding two numbers requires specific codes.
- **High-Level Language:** A compromise, with some difficulty for both humans and computers 🔤.
    - An acceptable tradeoff, such as Java.

### 🎯 Our Choice: Java

- **Why Java?** Widely used, widely available, continuously developed since the early 1990s, embraces modern abstractions, and has automatic checks for errors.
- **Java Economy:** Used in Mars rovers, cell phones, web servers, medical devices, and supercomputing. 👨‍🚀📱🌐
- **No Perfect Language:** No language is perfect.
- **Focus**: Learn a minimal subset of Java and develop general programming skills applicable to other languages.

> _"There are only two kinds of programming languages: those people always [gripe] about and those nobody uses."_ - Bjarne Stroustrup. 🗣️

## 🧱 Java Vocabulary: Minimal Subset

- **Built-in Types:** `int`, `long`, `double`, `char`, `String`, `boolean`.
- **Flow Control:** `if`, `else`, `for`, `while`.
- **Operations**: `true`, `false`, `!`, `&&`, `||`.
- **String Operations:** `+`, `""`, `length()`, `charAt()`, `compareTo()`, `matches()`.
- **Numeric Operations:** `+`, `-`, `*`, `/`, `%`, `++`, `--`.
- **Punctuation**: `{ } ( ) , ;`.
- **Assignment**: `=`.
- **Arrays**: `a[]`, `length`, `new`.
- **Object-Oriented**: `static`, `class`, `public`, `private`, `new`, `final`, `toString()`, `main()`.
- **Math Methods:** `Math.sin()`, `Math.cos()`, etc..
- **System Methods:** `System.print()`, `System.println()`, `System.printf()`.
- **Type Conversion Methods:** `Integer.parseInt()`, `Double.parseDouble()`.
- **Comparisons**: `<`, `<=`, `>`, `>=`, `==`, `!=`.
- **Standard Methods**: `StdIn.read*()`, `StdOut.print*()`, `StdDraw.*()`, `StdAudio.*()`, `StdRandom.*()`.
- **Identifiers**: Names that you make up.

## 📝 Anatomy of a Java Program

- **Text File:** A Java program is stored in a text file with a `.java` extension.
- **Program Name:** The program name matches the filename (e.g., `HelloWorld.java` corresponds to a `HelloWorld` program).
- **`main()` method**: Every program has a `main()` method, which is where the execution of the program begins.
- **Statements:** The body of the `main()` method consists of a sequence of statements.
- **Example: `HelloWorld.java`**

```
public class HelloWorld {
   public static void main(String[] args) {
      System.out.println("Hello, World");
   }
}
```

- **Ignoring Style**: Fonts, color, comments, and extra space are not relevant in the Java language.

### 🐛 Common Errors

- **`Main method not public`**: Forgot the `public` keyword in the main method declaration.
- **`invalid method declaration; return type required`**: Forgot the `void` keyword in the main method declaration.

## 👨‍💻 Program Development Process

- **EDIT:** Create the program by typing it into a text editor ✍️.
- **COMPILE:** Translate the program into bytecode using the Java compiler (`javac`) ⚙️.
    - Result: `.class` file (e.g. `HelloWorld.class`).
    - Compiler checks for syntax errors.
- **RUN:** Execute the program using the Java runtime (`java`) ▶️.
    - Result: program output.
- **Feedback Loop:** If there are mistakes, go back to edit, recompile, and run again.

> Any creative process involves cyclic refinement/development

### 🧰 Program Development Environments

- **Virtual Terminals:** Work with any language, simple and concise.
    - Use multiple virtual terminals for editing, compiling, and running programs.
- **Integrated Development Environment (IDE):** Language-specific, has many helpful tools, often good for beginners.
    - Has buttons for compiling and running.

### 🕰️ A Very Short History of Program Development

- **Switches and Lights (circa 1970):** Input binary code and data using switches, read output with lights.
- **Punched Cards and Line Printers (mid-1970s):** Use punched cards for input, line printer for output.
- **Timesharing Terminals (late 1970s):** Use terminals for editing, reading output, and controlling the computer.
- **Virtual Terminals (1980s-present):** Use multiple virtual terminals on personal computers.
- **Integrated Development Environments (1980s-present):** Customized applications for program development.

## 📊 Built-In Data Types

- **Data Type Definition:** A set of values and a set of operations on those values.

### 📝 Common Data Types in Java

|Data Type|Values|Operations|Example|
|:--|:--|:--|:--|
|`char`|Characters ('A', '@', '1')|Compare|`char letter = 'A';`|
|`String`|Sequences of characters ("Hello", "CS")|Concatenate (+)|`String message = "Hello, World";`|
|`int`|Integers (17, 12345)|Add, subtract, multiply, divide, remainder|`int age = 30;`|
|`double`|Floating-point numbers (3.14, 6.022e23)|Add, subtract, multiply, divide|`double pi = 3.14159;`|
|`boolean`|Truth values (true, false)|And (`&&`), or (`|`), not (`!`)|

- **Variables:** A name that refers to a value.
- **Literals:** Programming-language representation of a value (e.g., `1234`, `"hello"`, `true`).
- **Declaration Statement:** Associates a variable with a type (e.g., `int a;`).
- **Assignment Statement:** Associates a value with a variable (e.g., `a = 1234;`).

### 🧮 String Data Type

- **Concatenation:** Use `+` to combine strings (e.g., `"Hi, " + "Bob"` results in `"Hi, Bob"`).
- **Whitespace:** Significant in strings and depends on context.
- **Use Case:** Primarily for input and output.

### 📏 Example: Ruler Program

```
public class Ruler {
    public static void main(String[] args) {
        String ruler1 = "1";
        String ruler2 = ruler1 + " 2 " + ruler1;
        String ruler3 = ruler2 + " 3 " + ruler2;
        String ruler4 = ruler3 + " 4 " + ruler3;
        System.out.println(ruler4);
    }
}
```

### ⌨️ Input and Output

- **Output:** `System.out.println()` prints a string to the terminal. Java automatically converts numbers to strings for output.
- **Input:** Command-line arguments are available as strings (e.g., `args`, `args`, ...).
    - Use `Integer.parseInt()` or `Double.parseDouble()` to convert strings to numbers.

### 🔢 Integer Data Type (`int`)

- **Values:** Integers between -2^31 and 2^31-1 .
- **Operations:** Add, subtract, multiply, divide, remainder (%).
- **Division:** Integer division drops the fractional part (e.g. `5 / 3` results in `1`).
- **Precedence:** `*`, `/` have precedence over `+`, `-`. Use parentheses to clarify order.
- **Left Associativity**: Operations of same precedence are done left to right.

### 🧮 Double Data Type

- **Values:** Floating-point numbers, like scientific notation.
- **Operations:** Add, subtract, multiply, divide.
- **Approximations:** Double values are often approximations.
- **Special values:** `Infinity`, `NaN` (Not a Number).
- **Math Library:** Includes many math functions

### Boolean Data Type

- **Values:** `true` or `false`.
- **Operations:** And (`&&`), or (`||`), not (`!`).
- **Truth Tables:** Define the outcomes of each operation.
- **Comparison Operators:** Produce a boolean result from comparing values (e.g., `==`, `!=`, `<`, `<=`, `>`, `>=`)

### 🔄 Type Conversion

- **Type Checking**: Types of variables must match the defined operations.
- **Automatic Conversion:** Convert number to string for `+`; make numeric types match if no loss of precision.
- **Explicit Conversion:** Use methods like `Math.round()`, `Integer.parseInt()`, and `Double.parseDouble()`.
- **Casts:** Explicitly convert a value from one type to another (e.g., `(int) 2.71828`).
- **Pay attention:** Always know the type of your data.

#### ⚠️ Type Conversion Caution

- **Potential Problems:** Can lead to counterintuitive results and loss of information.
- **Range limitations:** Ensure that the value is within the valid range for a given type or you will have unexpected results

### 🎲 Example: Random Integer

```
public class RandomInt {
    public static void main(String[] args) {
        int N = Integer.parseInt(args);
        double r = Math.random();
        int t = (int) (r * N);
        System.out.println(t);
    }
}
```

## 📝 Summary

- **Data Type**: A set of values and a set of operations on those values
- **Java Built-In Types**: `String`, `int`, `double`, and `boolean` are commonly used built-in data types in Java.
- **Java Rules:** In Java, you must declare the types of your variables, convert from one type to another when necessary, and resolve type errors.
- **Compiler is Your Friend**: Java compiler will help you identify and fix type errors.
