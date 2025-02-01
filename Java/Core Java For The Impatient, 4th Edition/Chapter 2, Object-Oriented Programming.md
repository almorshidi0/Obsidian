This chapter dives into the core of object-oriented programming (OOP) in Java.  It explains how to create and use objects, define classes, and organize code effectively. 

## Core Concepts 💡

### 🧱 Objects and Classes

*   **Objects** are the building blocks of OOP, each with its own state. They collaborate to carry out work. Think of them as real-world entities with behaviors and data.
*   **Classes** are blueprints for creating objects. They define the behavior and state of objects of the same type. In Java, every method is declared within a class, and most values are objects (except primitive types).
*   **Encapsulation**:  Hiding implementation details and exposing only necessary functionalities. This is a key principle of OOP.
*  **Sharing Work**: Functions allow work to be shared, and objects add the dimension of state.

### 🛠️ Methods

*   **Instance Methods** operate on a specific object instance.  They are invoked *on* an object and have access to the object's data using the `this` reference.
*   **Static Methods** belong to the class itself and not to any specific object. They are invoked using the class name. Static methods cannot access instance variables.
*   **Accessor Methods** retrieve information about the object's state without modifying it. They leave the object unchanged.
*   **Mutator Methods** modify the state of the object they are invoked on.

### 🗂️ Object References

*   In Java, variables hold **references** to objects, not the actual objects themselves.
*   Multiple variables can hold references to the same object. Mutating an object through one reference is visible through all its references.
*   **`null`**:  A special value indicating that a reference does not refer to any object.  Using `null` improperly can cause `NullPointerException` errors.

## Implementing Classes ⚙️

### 📍 Instance Variables

*   Used to describe an object's state and are declared inside the class.
*   Usually declared as `private`, restricting access to only methods of the same class. This allows you to control which parts of your program can modify the variables and to change internal representation.

### 📃 Method Headers

*   Specify the method's name, parameter types and names, and return type.
*   `public` methods can be accessed from anywhere. `private` methods are restricted to being used only in other methods of the same class.

### ⚙️ Method Bodies
* Contain the code that is executed when the method is called.
*   The `return` keyword is used to return a value from a method.

### 🎯 Instance Method Invocations

*   Methods operate on a specific object instance and use the `this` reference to access the object.
*   When an instance method is invoked, it receives a reference to the object on which it was invoked and the arguments of the method call.

### `this` Reference

*   A reference to the object on which the method is invoked.  It's used to distinguish between instance variables and local variables.

### 📞 Call by Value

*   Java uses "call by value" for all parameters, including object references.
    *   When an object is passed as a parameter, a copy of the reference is passed. The method can access and mutate the original object through this reference.
    *   Primitive type variables can not be updated by a method.
    *  Methods cannot change the object reference itself to something different.

### 🏗️ Object Construction

*   **Constructors** initialize objects when they are created using the `new` operator. They have the same name as the class and no return type.
*   **Overloading**: A class can have multiple constructors with different parameters.
*   **Calling Constructors**:  One constructor can call another using the `this` keyword as the first statement.
*   **Default Initialization**: Instance variables are automatically initialized to default values if not set in the constructor (0 for numbers, false for booleans, and null for objects).
*  **Initialization Blocks**: You can specify initial values for instance variables, or include initialization blocks in a class. They are executed before the constructor.
* **Final Instance Variables**: `final` instance variables must be initialized by the end of every constructor, and cannot be modified again.

### ⏺️ Records

*   A special kind of class whose state is immutable and publicly accessible.
*   Automatically generate constructor, accessor methods, `toString`, `equals`, and `hashCode` methods.
*  **Custom Constructors**:  Can be defined, but must call the canonical constructor.
* **Compact Constructor**: Can be used to validate or normalize parameters for the canonical constructor.

## Static Members ⚙️

### 🧮 Static Variables
*  There is only one such variable per class, not per object.
*   Often used for shared information (e.g., unique IDs).
*   **Static Constants**: Declared using `static final`, commonly used (e.g., `Math.PI`).
    * Useful for sharing a single instance of an object.

### 🧱 Static Initialization Blocks

*   Used for additional initialization work on static variables.
*   Executed when the class is first loaded.

### ⚙️ Static Methods

*   Do not operate on objects; invoked on a class.
*   Used for utility methods or factory methods that create objects.
*   Cannot access instance variables, but can access static variables.

### 🏭 Factory Methods

*   Static methods that return new instances of the class.
*   Useful when you need to return a specific subclass or a shared object.

## Packages 📦

### 🗂️ Package Declarations

*   Used to organize classes into logical groups.
*   Package names are dot-separated lists of identifiers. Use reverse domain names to guarantee uniqueness.
*  A `package` statement must be the first statement in a source file.
*   Class files must be placed in subdirectories that match their package names.
*  The default package is not recommended.

### 🗄️ The jar Command
* The `jar` utility packages class files into a single JAR file for distribution.

### 🛤️ Class Path

*   The class path tells the compiler and JVM where to find class files and JAR files. Use the `-cp` option to specify it. Wildcards can be used to include all JAR files in a directory.
* Setting the class path in the CLASSPATH environment variable is not recommended.

### 🔒 Package Access

*   Features without `public` or `private` modifiers have package access, allowing access within the same package.
*   Useful for internal utility classes or test classes.
*   Packages are open-ended; any class can be added to a package.

### 📥 Importing Classes

*   The `import` statement allows you to use classes without their fully qualified names.
*   `import` declarations are a convenience, not a necessity.
*   Wildcards can be used to import all classes from a package (e.g. `import java.util.*;` ).
*   Conflicts can occur if multiple packages have classes with the same name.

### 💫 Static Imports

*   Import static methods and variables using `import static`.

## Nested Classes  Nesting 🪺

### 🧱 Static Nested Classes

*   Declared using the `static` modifier. They are like regular classes with access control.
*   Only methods of the outer class can access private nested classes.

### 🧱 Inner Classes

*   Non-static nested classes that have a reference to the object of the enclosing class.
*  They can access instance variables of the outer class.
*   Inner classes exist as part of an object, while static nested classes do not.
*   Use `OuterClass.this` to access the outer class instance explicitly.
*  The syntax to create an inner class object is `outerObject.new InnerClass()`.

## Documentation Comments 📝

### 📑 Comment Insertion

*   Use `/** ... */` to create documentation comments.  Javadoc extracts information from these comments to generate HTML documentation.
* The first sentence should be a summary statement.
*   Use HTML modifiers and images from the `doc-files` subdirectory.

### 🏷️ Class, Method, and Variable Comments

*   Class comments document the class. Use `@author` and `@version` tags.
*   Method comments document method parameters (`@param`), return values (`@return`), and exceptions (`@throws`).
*   Variable comments document public variables (usually `static final` constants).
*   Use `@since` to indicate the version a feature was added and `@deprecated` for features that should no longer be used.

### 🔗 Links

*   Use `@see` to create hyperlinks in the “see also” section.  Can link to other classes, methods, or URLs.
*   Use `{@link ...}` to create hyperlinks within comments.

### 📦 Module, and Overview Comments

*   Package comments are placed in a `package-info.java` file.
*   Module comments are placed in `module-info.java` file.
*   An overview comment is placed in an `overview.html` file.

### ⚙️ Comment Extraction

*   Use the `javadoc` command to generate HTML documentation. You may want to use the -link and -linksource options.

## Key Takeaways 🔑

*   **OOP Fundamentals:** Understand the concepts of objects, classes, encapsulation, and references.
*   **Class Design:** Know how to implement classes with instance variables, methods, and constructors.
*   **Static vs. Instance:**  Distinguish between static and instance members.
*   **Packages and Organization:** Use packages to organize code effectively.
*   **Nested Classes:** Know when to use static nested classes and inner classes.
*   **Documentation:**  Use Javadoc comments to document your code.
