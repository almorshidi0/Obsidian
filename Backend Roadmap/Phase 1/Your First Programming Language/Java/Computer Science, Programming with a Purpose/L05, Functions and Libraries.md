## 🧱 Basic Concepts

- This lecture introduces the concept of **modular programming** using functions and libraries.
- **Functions** are reusable blocks of code that perform specific tasks.
- **Libraries** are collections of functions, which are also called modules.
- The goal is to build large programs from small, manageable pieces of code.
- The idea of modular programming has been a "holy grail" for decades.

## 🧩 Modular Programming

- **Modular programming** organizes programs into independent modules that work together.
- It makes code easier to share, reuse, and build larger programs.
- For the purposes of this course, a **module** is a `.java` file.
- **Functions (static methods)** in Java take zero or more input arguments and return zero or one output value, and may cause side effects.
- Functions are more general than mathematical functions due to side effects, such as output to standard draw.

## 🧰 Functions and Libraries

- A **library** is a set of functions.
- Functions are used by scientists to calculate formulas and by programmers to build modular programs.
- Examples of built-in functions include `Math.random()`, `Math.abs()`, and `Integer.parseInt()`.
- I/O libraries like `StdIn.readInt()`, `StdDraw.line()`, and `StdAudio.play()` are also functions.
- **User-defined functions**, like `main()`, are also functions.
- **Java functions** are more general than mathematical functions because they can cause side effects.
- **Functions provide a new way to control the flow of execution**.

## 🔬 Anatomy of a Java Library

- A library is a set of functions.
- A function has a **return type**, a **method signature**, and **argument declarations**.
- A **method's signature** includes the name of the function and the types of its parameters.
- The `Newton.java` library consists of the `sqrt()` method and the `main()` method.
- A **return statement** in a method returns a value of the specified return type.

## 🎯 Scope

- The **scope of a variable** is the code that can refer to it by name.
- Variables should be declared to limit their scope.
- In a Java library, a variable's scope is the code following its declaration in the same block.
- Argument variables have a scope limited to the function's code block.
- A function's variables are local to that function.
- Variables with the same name in different scopes are different variables.

## 🚦 Flow of Control

- When a function is called, control transfers to the function's code.
- Argument variables are declared and initialized with the given values.
- The function code is executed.
- Control transfers back to the calling code, with the return value assigned in place of the function name. This is called **"pass by value"**.
- The operating system calls the `main()` method when a Java program is executed.
- The `main()` method processes command-line arguments and calls other functions.
- The flow of control can be traced through function calls.

## ✍️ Function Examples

- `FunctionExamples.java` provides examples of implementing mathematical functions.
- The **Gaussian (normal) distribution function** is defined by the formula `ϕ(x)= 1/(sqrt(2π)) * e^(-x^2/2)`.
- The **cumulative Gaussian distribution function** `Φ(z)` is the area under the curve of `ϕ(x)` to the left of the vertical line `x = z`.
- No closed-form expression exists for `Φ(z)`, so a Taylor series approximation is used.
- `Gaussian.java` implements both `ϕ(x)` and `Φ(z)` as static methods.
- `Coupon.java` separates individual components of the computation with functions.

## ⚙️ Passing Arguments and Returning Values

- **Pass by value:** parameter variables are initialized with the value of the arguments provided by the calling code.
- Parameter variables are used within the function body like local variables.
- Static methods can take arrays as arguments to operate on many values of the same type.
- Static methods that take array arguments may produce side effects by changing the array elements.
- Static methods can also return an array as a value.

## 🎵 Digital Audio

- Sound is the perception of the vibration of molecules.
- A musical tone is a steady periodic sound, and a pure tone is a sinusoidal waveform.
- The **frequency** of a sine wave determines the musical note.
- Concert A is 440 Hz, and the 12 notes in a Western scale are spaced logarithmically.
- Digital audio represents a wave by sampling it at regular intervals and saving the values in an array.
- The sampling rate is typically 44,100 samples per second for CD quality audio.
- The `StdAudio` library allows playing sound waves (arrays of double values) and converting to and from `.wav` files.
- `PlayThatNote.java` generates a tone at a given frequency and duration using a sine wave.
- `PlayThatTune.java` reads a list of tones and durations from standard input to play a tune.
- Chords can be produced by averaging waveforms.
- Harmonics can be added to a tone to produce a more realistic sound.

## 📊 Gaussian Distribution

- The **Gaussian distribution** is a mathematical model used for centuries.
- It is also known as the **bell curve**.
- The Gaussian probability density function (pdf) is given by `f(x) = (1 / (σ * sqrt(2π))) * e^(-((x - μ)^2) / (2 * σ^2))` where μ is the mean and σ is the standard deviation.
- The cumulative distribution function (cdf) gives the area under the curve to the left of a given point.
- The Gaussian PDF is not implemented in Java's Math library because it's easy for users to implement themselves.
- The CDF can be implemented using a **Taylor series**.
- A **best practice** is to test all code in `main()` and have it do something useful.
- Libraries of functions extend the Java system and make code reusable.

## 🎛️ Modular Programming

- **Modular programming** involves using **abstractions** to separate client code from implementation details.
- An **API (Application Programming Interface)** defines signatures and describes methods.
- A **client** is a module that calls a library's methods.
- The API is a contract between the client and implementation, enabling independent development.
- The `StdRandom` library implements methods for generating random numbers.
- The `StdStats` library implements methods for computing statistics on arrays.
- Small modules should separate and classify small tasks.
- Code the client before coding the implementation.
- Include a `main()` test client in each module.

## 🪙 Bernoulli Trials

- **Bernoulli trials** simulate coin flips.
- The `Bernoulli.java` program uses `StdRandom`, `Gaussian`, and `StdStats` libraries to simulate coin flips, calculate their frequencies, and compare against the theoretical Gaussian curve.
- Modular programming enables development of complex programs via simple, independent modules.
- Advantages include code that is easier to understand, debug, maintain, and reuse.

## 🔑 Key Concepts

- **Functions** and **libraries** enable modular programming.
- **Scope** limits the visibility of variables.
- **APIs** define the contract between clients and implementations.
- **Modular programming** promotes code reuse and maintainability.
- **Abstraction** simplifies the design and development process.
