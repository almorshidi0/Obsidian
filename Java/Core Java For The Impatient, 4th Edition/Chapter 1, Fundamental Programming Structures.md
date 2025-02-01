This chapter provides a fast-paced introduction to Java for experienced programmers. It covers basic data types, control structures, and key aspects of the Java API.

## 🔑 Key Concepts

* **Methods in Java** are always declared within a **class**. Non-static methods operate on objects, while static methods do not. Program execution starts with the `static main` method.
* **Primitive Data Types:** Java has eight primitive types:
  * Four signed integers (`byte`, `short`, `int`, `long`).
  * Two floating-point types (`float`, `double`).
  * `char` for characters.
  * `boolean` for true/false values.
* **Operators and Control Structures:** Similar to C or JavaScript.
* **Switch Statements:** Java offers four forms of switch: expressions and statements, both with and without fall-through.
* **Math Class:** Provides common mathematical functions.
* **Strings:** String objects are sequences of Unicode characters, use text blocks for multiline string literals.
* **System.out & Scanner:** `System.out` displays output in the terminal, and `Scanner` reads input from the terminal.
* **Arrays and Collections:** Used to store elements of the same type.

## 🌎 1.1 Our First Program: "Hello, World!"

* **Java is object-oriented:** Programs manipulate objects, which are instances of classes.
* **Classes:** Define an object's state and behavior.
* **`main` Method:** The entry point of a Java program.
  * Declared as `static` because it doesn't operate on objects.
  * Declared as `void` as it does not return a value.
* **Visibility Modifiers:** `public` and `private` control access to classes and methods. `public` is most common.
* **Packages:** Classes are organized into packages, which helps avoid naming conflicts.
* **Comments:** Use `//` for single-line, `/* ... */` for multiline, and `/** ... */` for documentation comments.
* **Compilation and Execution:**
  * Use `javac` to compile `.java` files into byte code.
  * Use `java` to launch the virtual machine and execute the byte code.
  * Byte code is platform-independent ("write once, run anywhere").
* **JShell:** A REPL (read-evaluate-print loop) tool for experimenting with Java code without compiling.
  * Start JShell by typing `jshell` in a terminal.
  * JShell automatically prints the value of every expression.
  * Use tab completion to explore methods.
  * Use `/help` for more assistance, `/exit` to quit.
* **Preview features** such as omitting public static void main and the class itself (for very simple programs) are available in Java 21.

## 📞 1.1.3 Objects, Instances, and Method Calls

* **Objects** are instances of classes.
* **Instance Methods** operate on objects.
* Use dot notation (`object.methodName(arguments)`) to invoke a method.
* **String objects** have a `length()` method.
* **`new` operator**: Constructs objects.
* **Factory methods**: An alternative way of producing objects (e.g., `RandomGenerator.getDefault()`).

## 🧮 1.2 Primitive Types

### 1.2.1 Signed Integer Types
* Four types: `byte` (1 byte), `short` (2 bytes), `int` (4 bytes), and `long` (8 bytes).
* `int` is the most practical in most cases.
* `long` is used when you need a larger range.
* Ranges are consistent across different machines.
* Use `L` suffix for long literals (e.g., `4000000000L`).
* Hexadecimal literals start with `0x` (e.g., `0xCAFEBABE`).
* Binary literals start with `0b` (e.g., `0b1001`).
* Octal literals start with `0` (e.g., `011`) – avoid!
* Use underscores in number literals for readability (e.g., `1_000_000`).
* Signed integer values can be interpreted as unsigned with some care.

### 1.2.2 Floating-Point Types
* Two types: `float` (4 bytes) and `double` (8 bytes).
* `double` is the default, offering more precision.
* Use `F` suffix for float literals (e.g., `3.14F`), `D` suffix is optional for double literals (e.g., `3.14D`).
* Special values: `Double.POSITIVE_INFINITY`, `Double.NEGATIVE_INFINITY`, `Double.NaN`.
* Use `Double.isNaN(x)` to test for NaN, `Double.isInfinite` to test for ± ∞, and `Double.isFinite` to check if a number is finite and not NaN.
* Use `BigDecimal` for precise financial calculations (to avoid roundoff errors).

### 1.2.3 The `char` Type
* Represents UTF-16 code units.
* Character literals are enclosed in single quotes (e.g., `'J'`).
* Use `\u` prefix for hexadecimal code units (e.g., `\u004A` is the same as `'J'`).
* Special codes: `\n` (line feed), `\r` (carriage return), `\t` (tab), `\b` (backspace).

### 1.2.4 The `boolean` Type
* Has two values: `false` and `true`.
* Not a number type.

## 🏷️ 1.3 Variables

### 1.3.1 Variable Declarations
* Java is strongly typed, and each variable has a specific type.
* Use `var` keyword when the type of the declared variable is obvious.

### 1.3.2 Identifiers
* Must start with a letter, can consist of letters, digits, currency symbols and connectors like `_`.
* The `$` symbol is intended for automatically generated identifiers.
* Case-sensitive: `count` and `Count` are different identifiers.
* Cannot use spaces, symbols, or keywords as identifiers.
* Use camel case (e.g., `countOfInvalidInputs`).

### 1.3.3 Initialization
* Variables must be initialized before use, or you will get a compiler error.
* Declare variables as late as possible (just before first use).

### 1.3.4 Constants
* Use `final` keyword for values that cannot be changed (constants).
* Use uppercase letters for constant names (e.g., `DAYS_PER_WEEK`).
* Use `static` keyword for constants outside of methods to make them available to other methods.
* Initialization can be deferred if initialized once before first use.
* Use `enum` for a set of related constants.

## ➕➖➗✖️ 1.4 Arithmetic Operations

### 1.4.1 Assignment
* The `=` operator sets a variable to the value of an expression.
* Assignment is an operator with a value.
* Compound assignment operators combine an operation with an assignment (e.g., `amount -= fee`).

### 1.4.2 Basic Arithmetic
* `+`, `-`, `*`, `/` for addition, subtraction, multiplication, and division.
* Integer division (`/`) discards the remainder.
* Integer division by zero throws an exception; floating-point division by zero yields infinity or NaN.
* `%` is the modulus (remainder) operator.
* `Math.floorMod` handles negative operands correctly.
* `++` and `--` are increment and decrement operators.

### 1.4.3 Mathematical Methods
* `Math.pow(x, y)` for x<sup>y</sup>, `Math.sqrt(x)` for the square root of x.
* `Math.min` and `Math.max` for minimum and maximum of two values.
* The `Math` class also provides trigonometric, logarithmic functions, and constants like `Math.PI`, `Math.E`, and `Math.TAU`.
* Use methods like `Math.multiplyExact`, `addExact`, `subtractExact`, to handle overflow issues.
* Methods for unsigned operations are available in the `Integer` and `Long` classes.

### 1.4.4 Number Type Conversions
* Operands of different number types are automatically converted to a common type.
* Conversion happens in this order: double > float > long > int.
* Use cast operator `(type)` to convert to another type.
* Use `Math.round(x)` to round to the nearest integer (returns a `long`).
* Use `Math.toIntExact` to cause an exception when casting from `long` to `int` if the value does not fit.

### 1.4.5 Relational and Logical Operators
* `==` and `!=` for equality and inequality.
* `<`, `>`, `<=`, `>=` for comparisons.
* `&&` (and), `||` (or), `!` (not) for logical operations.
* Short-circuit evaluation is used to prevent errors.
* The conditional operator `? :` selects one of two values based on a condition.
* Bitwise operators `&` (and), `|` (or), `^` (xor) operate on bit patterns.
* Shift operators: `<<`, `>>`, `>>>`.
* When applied to boolean values, the `&` and `|` operators force evaluation of both operands before combining the result.

### 1.4.6 Big Numbers
* Use `BigInteger` for arbitrary-precision integers.
* Use `BigDecimal` for arbitrary-precision floating-point numbers.
* Use the `valueOf` method to turn a long into a `BigInteger`.
* Construct `BigInteger` objects from a string of digits.
* Use methods (`add`, `multiply`) to perform operations on big numbers.
* `BigDecimal` gives accurate results when dealing with floating-point operations that would otherwise be imprecise.

## 🧵 1.5 Strings

### 1.5.1 Concatenation
* Use the `+` operator to concatenate strings.
* When a string is concatenated with another value, the other value is converted to string first.
* Use `String.join` to combine multiple strings with a delimiter.
* Use `StringBuilder` for efficient concatenation of a large number of strings.

### 1.5.2 Substrings
* Use the `substring` method to extract substrings (e.g., `string.substring(start, end)`).
* Use the `split` method to extract substrings separated by a delimiter (e.g., `string.split(", ")`).

### 1.5.3 String Comparison
* Use `equals` method to compare strings, not `==` operator, to compare string contents.
* `String` variables can be `null`.
* Use `==` to check if a string is `null`.
* Use `equalsIgnoreCase` to compare strings ignoring case.
* Use `compareTo` to compare strings in dictionary order.
* Use `Collator` objects for language-specific sorting.

### 1.5.4 Converting Between Numbers and Strings
* Use `Integer.toString` to convert integers to strings.
* Use `Integer.parseInt` to convert strings to integers.
* Use `Double.toString` and `Double.parseDouble` for floating-point numbers.

### 1.5.5 The String API
* The `String` class has many useful methods, such as:
  * `startsWith`, `endsWith`, `contains`.
  * `indexOf`, `lastIndexOf`.
  * `replace`.
  * `toUpperCase`, `toLowerCase`.
  * `strip`.
* The `String` class is immutable (methods do not modify the original string).
* Methods often take `CharSequence` parameters (a common supertype for string-like classes).
* Use the online Java API documentation for details.

### 1.5.6 Code Points and Code Units
* Unicode uses 21 bits to represent all characters, and values are called code points.
* Java uses UTF-16, a variable-length encoding (code units) with 16-bit values. Some code points require two code units (surrogate pairs).
* A `char` is a code unit not a code point.
* Grapheme cluster is a sequence of code points that form a single symbol.
* Avoid processing individual code units with `charAt`.
* Use `indexOf` and `lastIndexOf` to work with substrings.
* `length` method returns the number of code units, not necessarily the number of characters.
* Use `split("\\b{g}")` to get an array of grapheme clusters.
* Strings may be internally represented as byte arrays.

### 1.5.7 Text Blocks
* Use triple quotes (`"""`) to declare multiline string literals.
* Line breaks after opening `"""` are not included.
* Use backslash (`\`) to suppress line breaks.
* No need to escape quotation marks within text blocks.
* Backslashes need to be escaped.
* Trailing whitespace is normalized (use `\s` to preserve it).
* Leading white space common to all lines is removed.

## ⌨️ 1.6 Input and Output

### 1.6.1 Reading Input
* Use `Scanner` class to read input from `System.in`.
* `nextLine` reads an entire line of input.
* `next` reads a single word (delimited by whitespace).
* `nextInt` reads an integer, `nextDouble` reads a floating-point number.
* Use `hasNextLine`, `hasNext`, `hasNextInt`, `hasNextDouble` to check for available input.
* `Scanner` is located in `java.util` package.
* Use `Console` class to read passwords (more secure).
* Redirect input/output using shell syntax (e.g., `< input.txt > output.txt`).

### 1.6.2 Formatted Output
* Use `print` for output without a new line.
* Use `printf` for formatted output.
* Use format specifiers (e.g., `%8.2f` for floating-point numbers, `%s` for strings, `%d` for integers).
* Use conversion characters and flags to control formatting (see Tables 1.5 and 1.6).
* Use `formatted` method to create a formatted string without printing it.

## 🚦 1.7 Control Flow

### 1.7.1 Branches
* Use `if` statement for conditional execution (single or multiple statements).
* Use `else` for alternative execution.
* Use `else if` for additional conditions.

### 1.7.2 Switches
* **Switch Expression:** Compares a selector against multiple cases, producing a value for each case, uses the `->` syntax.
* **Switch Statement:** Similar to the switch expression but does not yield a value, and has a `break` statement.
* Cases can be integers, string literals, or enumeration values.
* Cases can have multiple labels (comma-separated).
* Use `yield` to produce a value when doing additional work inside a brace-enclosed block.
* Use `throw new IllegalArgumentException()` to throw exceptions in default case.
* Use `case null` to handle null selector values.
* **Fall-through switch:** Execution falls through to the next case unless stopped by a `yield` (in expressions) or `break` statement (in statements). Use `:` instead of `->`.
* Enhanced switches (that have case null or fall through behavior) must be exhaustive and contain a `default` case.

### 1.7.3 Loops
* **`while` loop:** Executes as long as a condition is true.
* **`do/while` loop:** Executes at least once, then continues while a condition is true.
* **`for` loop:** Typically used when the number of iterations is fixed.
* Can rewrite a `for` loop as a `while` loop, but `for` keeps initialization, test, and updates in one place.
* Initialization, test, and update in `for` loop can take arbitrary forms.
* Multiple variables can be declared/updated in a `for` loop.

### 1.7.4 Breaking and Continuing
* Use `break` to exit a loop or switch immediately.
* Use `continue` to jump to the next iteration of a loop.
* **Labeled break:** Exits a labeled enclosing statement or loop.
* **Labeled continue:** Jumps to the next iteration of a labeled loop.

### 1.7.5 Local Variable Scope
* A local variable is declared in a method. Its scope is the block where it is declared.
* Parameter variables have a scope covering the entire method.
* Cannot have variables with the same name in overlapping scopes.

## 🗂️ 1.8 Arrays and Array Lists

### 1.8.1 Working with Arrays
* Arrays are used for collecting items of the same type.
* Declare arrays using `Type[] arrayName` syntax (e.g., `String[] names`).
* Initialize with `new Type[size]` (e.g., `new String`).
* Access elements with `array[index]` (e.g., `names`).
* Array length is accessed with `array.length`.
* Attempting to access an element that does not exist throws `ArrayIndexOutOfBoundsException`.
* `int numbers[]` is a less common syntax.

### 1.8.2 Array Construction
* When constructing with `new` operator, arrays are filled with default values: zeroes for numeric types, `false` for boolean, and null for objects.
* You can also list values in braces to initialize arrays (e.g., `int[] primes = { 2, 3, 5, 7, 11, 13 };`).
* A trailing comma is allowed in array initialization.
* Zero-length arrays are legal (e.g., `new int`, `new int[] {}`).

### 1.8.3 Array Lists
* `ArrayList` class in the `java.util` package manages an array internally and allows it to grow or shrink on demand.
* `ArrayList` is a generic class - you must specify the element type in angle brackets (e.g., `ArrayList<String>`).
* Declare and initialize `ArrayList` using `ArrayList<Type> arrayListName = new ArrayList<>();`.
* Add elements to the end with the `add` method (e.g., `friends.add("Peter")`).
* Use `remove(index)` to remove elements and `add(index, element)` to insert at a specific position.
* Use `get(index)` to access, `set(index, element)` to replace, and `size()` to get list size.
* Loop through elements with a traditional `for` loop with `size` and `get`.

### 1.8.4 Wrapper Classes for Primitive Types
* Use wrapper classes (`Integer`, `Byte`, `Short`, `Long`, `Character`, `Float`, `Double`, `Boolean`) with `ArrayList` since primitive types cannot be used as type parameters.
* Autoboxing and unboxing allow for seamless conversion between primitive types and their wrapper objects.
* `==` and `!=` operators compare object references, not contents of objects, when used with wrapper objects - use the `equals` method for value comparison.

### 1.8.5 The Enhanced for Loop
* Traverses the elements of an array or array list (e.g., `for (int n : numbers)`).
* Loop variable traverses elements of an array, not index values.

### 1.8.6 Copying Arrays and Array Lists
* Assigning array or `ArrayList` variables results in two variables referencing the same array or `ArrayList`, not a copy.
* Use `Arrays.copyOf` to create a copy of an array (e.g., `int[] copiedPrimes = Arrays.copyOf(primes, primes.length)`).
* Use a constructor like `var copiedFriends = new ArrayList<>(friends);` to copy `ArrayLists`.
* Use `String[] names = friends.toArray(new String);` to copy array list into an array.

### 1.8.7 Array Algorithms
* The `Arrays` class provides static methods for common array algorithms.
* Use `Arrays.fill` and `Collections.fill` to fill arrays and array lists.
* Use `Arrays.sort` and `Collections.sort` to sort arrays and array lists.
* `Arrays.parallelSort` distributes the sorting work over multiple cores for large arrays.
* Use `Arrays.toString` for debugging.
* `Collections.reverse` and `Collections.shuffle` are also available for array lists.

### 1.8.8 Command-Line Arguments
* The `main` method's `String[] args` parameter holds command-line arguments.
* The command, nor the class name are passed to the main method, only the arguments following them.

### 1.8.9 Multidimensional Arrays
* Implemented as arrays of arrays in Java.
* Use two bracket pairs to access elements (e.g., `square`).
* Row arrays can have different lengths.
* Traverse two-dimensional arrays with two nested loops.
* Use `Arrays.deepToString` to print multidimensional arrays.
* No two-dimensional array lists, but you can declare a variable of type `ArrayList<ArrayList<Type>>`.

## ⚙️ 1.9 Functional Decomposition

### 1.9.1 Declaring and Calling Static Methods
* Declare methods with return type (or `void`), method name, and parameter types.
* Use `return` statement to return the result.
* Declare methods with the `static` modifier when placing them in the same class as `main`.

### 1.9.2 Array Parameters and Return Values
* Methods can receive and modify arrays through references.
* Methods can return arrays.

### 1.9.3 Variable Arguments
* Methods can accept a variable number of arguments using `...` after the type (e.g., `double... values`).
* The variable argument is treated as an array inside the method.
* The variable parameter must be the last parameter.
