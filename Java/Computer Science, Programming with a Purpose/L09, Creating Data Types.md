## 🔄 Overview of Creating Data Types

- This lecture focuses on **how to implement your own abstract data types (ADTs)**, building on the previous lecture's use of ADTs.
- **Object-oriented programming (OOP)** empowers you to bring your own abstractions to life by creating custom data types and manipulating their objects.
- Key to OOP: An object holds a data type value, and variable names refer to objects.
- An **abstract data type (ADT)** hides its representation from the client, allowing use without knowing the implementation details.
    - This is what makes the data type abstract.

## 🧱 Implementing a Data Type

To create a data type, you need to provide code that:

- **Defines the set of values (instance variables)**:
    - These declarations associate variable names with types and represent the data type's values.
- **Implements operations on those values (methods)**:
    - Methods are like static methods but can refer to instance variables.
- **Creates and initializes new objects (constructors)**:
    - Constructors have the same name as the type, no return type, and are invoked by `new` to return an object of the type.
- In Java, a data type implementation is known as a **class**.
- Every class has the basic structure of: instance variables, constructors, methods, and a test client.

## ⚡ Charge ADT (Point Charges)

- A point charge is an idealized model of a particle with an electric charge.
- **Values**: position (x, y) and electrical charge (q).
    - Position is represented by two `double` values: `rx`, `ry`.
    - Electrical charge is a `double` value: `q`.
- **API (Operations)**:
    - `Charge(double x0, double y0, double q0)`: Constructor to create a new charge.
    - `double potentialAt(double x, double y)`: Calculates the electric potential at (x, y) due to the charge.
    - `String toString()`: Returns a string representation of the charge.
- **Electric Potential**:
    - Electric potential is a measure of the effect of a point charge on its surroundings.
    - It increases proportionally to the charge value and decreases proportionally to the inverse of the distance from the charge.
    - Formula: Vc(x,y) = k * q / r, where k = 8.99 x 10^9 and r is the distance between (x, y) and (rx, ry).
    - The potential at a point is the sum of the potentials due to all individual charges.
- **Implementation**:
    - Instance variables: `private final double rx, ry, q;`.
        - `private` denies client access to make the data type abstract.
        - `final` disallows changes in value after initialization, making the data type immutable.
    - Constructor: Initializes the instance variables with provided values.
        - Client programs use `new` to invoke constructors.
    - Methods: Implement the API operations on instance variables.
        - Instance variable references in methods refer to the values for the object that invoked the method.
- **Test Client**:
    - Creates a `Charge` object and tests the `toString()` and `potentialAt()` methods.
- **Visualizing Potential:**
    - `toColor(double V)`: converts a potential value to an 8-bit integer for grayscale.
    - `readCharges()`: reads charge values from standard input and returns an array of charges.
    - A visualization program uses these methods to display the electric potential in the unit square.
    - Visualizations can be enhanced by using a discontinuous color map.

## 🐢 Turtle Graphics ADT

- A turtle is an idealized model of a plotting device.
- **Values**: position (x, y) and orientation (angle).
- **API (Operations)**:
    - `Turtle(double x0, double y0, double a0)`: Constructor to create a new turtle.
    - `void turnLeft(double delta)`: Rotates the turtle counterclockwise by `delta` degrees.
    - `void goForward(double step)`: Moves the turtle forward by `step`, drawing a line.
- **Implementation**:
    - Instance variables: `private double x, y, angle;`.
        - Instance variables are not `final` because turtle's position and angle change.
    - Constructor: Initializes the instance variables.
    - Methods:
        - `turnLeft()`: Adds `delta` to the turtle's `angle`.
        - `goForward()`: Calculates new `x` and `y` coordinates based on `angle` and draws a line using StdDraw.
- **Test Client**:
    - Creates a `Turtle` object and uses `goForward()` and `turnLeft()` to draw a triangle.
- **N-gon Client**:
    - Draws a regular n-gon by taking a command line argument, computing the angle of turn, and stepping forward.
    - A large value of n approximates a circle.
- **Spiral Client**:
    - Draws a logarithmic spiral by decaying the step size each iteration.
    - This geometric shape appears frequently in nature.
- **Pop Quiz**:
    - A common mistake in constructors is to **shadow** instance variables by redeclaring them, instead of using the implicit references.

## 🔢 Complex Number ADT

- A complex number is a number of the form a + bi, where a and b are real numbers and i is the square root of -1.
- **Values**: real part (re) and imaginary part (im).
- **API (Operations)**:
    - `Complex(double real, double imag)`: Constructor to create a new complex number.
    - `Complex plus(Complex b)`: Returns the sum of this number and b.
    - `Complex times(Complex b)`: Returns the product of this number and b.
    - `double abs()`: Returns the magnitude of the complex number.
    - `String toString()`: Returns a string representation.
- **Complex Number Operations:**
    - Addition: (x0+iy0) + (x1+iy1) = (x0+x1) + i(y0+y1).
    - Multiplication: (x0+iy0) * (x1+iy1) = (x0x1−y0y1) + i(y0x1+x0y1).
    - Magnitude: |x+iy| = √(x² + y²).
- **Implementation**:
    - Instance variables: `private final double re, im;`.
        - Instance variables are `final`, meaning the values are set when the complex number is created and do not change.
    - Constructor: Initializes the instance variables.
    - Methods: Implement the API operations by creating new `Complex` objects.
    - The `this` keyword is a reference to the object itself (the object that was used to invoke the method).
- **Test Client**:
    - Creates two `Complex` objects and tests `toString()`, and `times()` methods.

## 🌀 Mandelbrot Set

- The Mandelbrot set is a set of complex numbers with many fascinating properties.
- Complex numbers are represented as points in the plane. If a point is in the set, it's colored black; otherwise, it's white.
- **Definition:** A complex number `z0` is in the Mandelbrot set if the sequence `zt+1 = (zt)^2 + z0` does not diverge to infinity.
    - If the magnitude of `zt` goes to infinity, `z0` is not in the set.
- **Practical Issues:**
    - Cannot plot infinitely many points, so use a finite grid of points.
    - Cannot iterate infinitely many times, so approximate with a limit.
- **Approximations:**
    - Sample from an N-by-N grid of points.
    - If |zt| > 2 for any t, then z is not in the set.
    - If |z255| ≤ 2 then z is "likely" in the set.
- **Implementation:**
    - `mand(Complex z0)`: Returns `Color.WHITE` if z0 is not in the set and `Color.BLACK` if it is likely in the set.
    - The function iterates up to 255 times. If the magnitude exceeds 2 at any time, the method immediately returns white; otherwise the method returns black.
    - A client program reads parameters from the command line to plot the set.
    - The client scales complex numbers to screen coordinates.
- **Visualizations**:
    - Grayscale can be used to show the number of iterations it takes before the magnitude exceeds 2.
    - Zooming in reveals intricate details and patterns.
    - Different color palettes enhance visual representation.

## 🔑 Key Takeaways

- **Object-oriented programming (OOP)** allows creation of custom data types.
- OOP helps simulate the physical world and extend the Java language by adding our own abstractions.
- **Instance variables** define the data type's values and are associated with each object.
- **Constructors** create and initialize new objects.
- **Methods** define the data type's operations and can access instance variables.
- The use of `private` and `final` keywords enhance data abstraction and immutability.
- Test clients are crucial for verifying the implementation.
- The Mandelbrot set demonstrates the power of computation and algorithmic definitions in mathematics.
