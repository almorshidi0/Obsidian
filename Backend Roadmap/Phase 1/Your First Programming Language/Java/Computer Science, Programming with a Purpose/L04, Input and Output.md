## 🔄 Introduction to Input and Output

- This lecture focuses on how Java programs interact with the outside world using **input and output devices**.
- The goal is to write programs that can receive input, process it, and produce meaningful output.
- The lecture introduces abstractions for input and output, and how the operating system connects programs to actual devices.
- Abstractions simplify our view of the world by unifying diverse real-world artifacts. For example, "printing" is the idea of a program producing text as output.
- The lecture expands on previous text-based I/O by introducing graphics, sound, and image I/O.
- **Standard input and output**, along with **standard drawing** and **standard audio**, are key concepts in this lecture.

## ⌨️ Input Devices

- Various input devices include keyboards, storage, trackpads, the internet, cameras, and microphones.
- The program should be able to receive input from these diverse devices.

## 🖨️ Output Devices

- Output can be directed to displays, storage devices, networks, printers, and speakers.
- The program should be able to produce output on these different devices.

## 🔀 Abstraction

- An **abstraction** exists only as an idea, and simplifies our view of the world by unifying diverse real-world artifacts.
- The idea of "printing" is an abstraction for a program producing text as output.
- Good abstractions simplify our view of the world by unifying diverse real-world artifacts.

## 💻 Terminal

- A **terminal** is an abstraction for providing input and output to a program.
- The terminal window is used to interact with the program.
- The terminal window concept is an abstraction based on older VT-100 terminals.
- **Command-line input** provides strings to a program.
- Strings typed after the program name are available as `args`, `args`, etc. at runtime.
- System conversion methods convert these strings to other data types.
- **Standard output stream** is an abstraction for an infinite output sequence.
- Strings from `System.out.println()` are added to the standard output stream.
- By default, the OS connects the standard output stream to the terminal.

## 📥 Standard Input

- **Standard input stream** is an abstraction for an infinite input sequence.
- New input can be provided while the program is executing.
- There's no limit to the amount of input data.
- Conversion to primitive types is handled explicitly.
- The `StdIn` library implements abstractions invented for UNIX in the 1970s.
- The `StdIn` library is available for download and includes methods such as `isEmpty()`, `readInt()`, `readDouble()`, `readLong()`, `readBoolean()`, `readChar()`, `readString()`, and `readAll()`.
- **Interactive input** mixes input and output streams, prompting the user for input.
- The program reads a stream of numbers and computes their average using a `while` loop and the `StdIn.isEmpty()` method.
- End of stream is specified by typing `<Ctrl-d>` (or `<Ctrl-z>` on Windows).
- The size of the input stream is unlimited, allowing programs to handle large data sets.

## 📤 Standard Output

- The `StdOut` library provides a consistent set of I/O abstractions.
- It makes output independent of system, language, and locale.
- It includes methods such as `print()`, `println()`, and `printf()`.
- `StdOut.print()` puts a string on the output stream, `StdOut.println()` adds a newline, and `StdOut.printf()` allows formatted output.
- From this lecture forward, use `StdOut` instead of `System.out`.

## 🗂️ Redirection and Piping

- Data and results can be kept in files or connected through piping.
- **Redirection** keeps data in files.
    - `>` redirects standard output to a file, e.g., `% java RandomSeq 1000000 > data.txt`.
    - `<` redirects standard input from a file, e.g., `% java Average < data.txt`.
- **Piping** connects the standard output of one program to the standard input of another using `|`.
    - e.g., `% java RandomSeq 1000000 | java Average`.
    - Piping avoids saving data to a file and allows for processing unlimited amounts of data.
- The system collects data on standard output and provides it to standard input.

## 💾 Streaming Algorithms

- **Streaming algorithms** enable programs to handle much more data than computers can store.
- Redirection and piping enable programs to handle much more data than computers could store.
- The lesson is to avoid limits within programs whenever possible.

## 🖼️ Standard Drawing

- The `StdDraw` library adds the ability to create a drawing.
- It is a library developed for the course but is broadly useful.
- The library includes methods for drawing lines, points, text, circles, squares, polygons, and pictures.
- It also includes methods for setting the pen radius, color, and scaling.
- The `show()` method displays all drawings.
- The default canvas size is 512x512 pixels and the default coordinate system is the unit square (all x and y coordinates between 0 and 1).
- `StdDraw.setXscale(x0, x1)` and `StdDraw.setYscale(y0, y1)` methods set the drawing coordinates.
- **Data visualization** is achieved by plotting data from standard input using `StdDraw`.
    - `PlotFilter.java` reads points from standard input and draws them on a graph.
- **Function plotting** is done by sampling and connecting points of a function.
    - `PlotFunctionEx.java` plots a function by connecting successive points with lines.
- **Outline and filled shapes** are available in `StdDraw` using methods such as `circle()`, `square()`, and `polygon()`, along with `filledCircle()`, `filledSquare()`, and `filledPolygon()`.
- `StdDraw` also includes methods for drawing **text** and setting the **color**.
- **Double buffering** improves performance by drawing on an offscreen canvas and copying it to the screen only when `show()` is called.

## 🎬 Animation

- **Animation** is created by rapidly displaying static drawings.
    - Steps for animation: Clear the screen, move the object, draw the object, display and pause.
- The display time should be greater than the screen-clear time.
- **Bouncing ball** animation is achieved by updating the ball's position and velocity.
    - The `BouncingBall.java` program moves a ball and makes it bounce off the walls.
    - Changing the code to remove the screen clear from the loop reveals the entire path of the ball.
- The `StdDraw.picture()` method displays an image.
- `BouncingBallDeluxe.java` uses an image of a tennis ball and plays a sound when the ball hits the wall.
- **User interaction** is supported using methods like `mouseX()`, `mouseY()`, and `mousePressed()`.

## 🎶 Standard Audio

- `StdAudio` is a library to play and manipulate sound files.
- It allows playing, manipulating, and synthesizing sound.
- Digital sound is represented by sampling at regular intervals.
- `StdAudio.play()` plays an array of numbers representing sound.
- `PlayThatTune.java` plays notes from standard input using `StdAudio`.

## 🌀 Fractals

- **Fractals** can be generated by simple iterative computations.
- The **Sierpinski triangle** is generated by a random game with specific rules.
- Changing the rules of the random game can create other interesting patterns, like the **Barnsley fern**.
- Iterated function systems (IFS) are a way to generate these patterns.

## 🧪 Exercises and Creative Exercises

- Many exercises and creative exercises extend the use of input and output to solve problems or create visualizations and animations.
- These involve diverse tasks such as:
    - Reading and processing numbers and text from standard input.
    - Calculating statistics like mean and standard deviation.
    - Implementing filters that manipulate input.
    - Creating various graphics such as checkerboards, roses, and spirographs.
    - Drawing geometric shapes and patterns.
    - Creating animations of bouncing balls, clocks, and simple harmonic motion.
    - Simulating games and physical phenomena such as random walks, projectile motion, and elastic collisions.
    - Implementing ciphers and coding/decoding algorithms.

## 🔑 Key Concepts

- **Abstractions** simplify interactions with diverse input and output devices.
- **Standard input and output** provide flexible ways for programs to interact with the outside world.
- **Redirection and piping** enable programs to handle large amounts of data.
- **Standard drawing** and **standard audio** allow programs to generate visual and audio output.
- **Animation** is achieved by rapidly displaying static drawings.
