## 🗄️ Introduction to Arrays

- Arrays are a fundamental construct for processing large amounts of data.
- They are an **indexed sequence of values of the same type**.
- Arrays facilitate the **storage and manipulation** of data.
- They are considered a basic building block for programming.
- Arrays are the first **data structure** discussed, which is defined as an arrangement of data that enables efficient processing.
- Arrays allow efficient access to data elements using an index.
- They enable storage of large amounts of data of the same type.

## 💾 Why Use Arrays?

- Arrays are essential when dealing with a **huge amount of data** of the same type, where it would be tedious and error-prone to name each data item separately.
- Examples where arrays are useful:
    - 52 playing cards in a deck.
    - Many students in an online class.
    - Billions of pixels in a digital image.
    - Billions of nucleotides in a DNA strand.
    - Google queries per year.
    - Neurons in the brain.
    - Cells in the human body.
    - Particles in a mole.
- Arrays are stored in **contiguous memory locations**, which allows for efficient access and processing.

## ⚙️ Basic Concepts

- **Index**: The position of a value in an array.
    - Indices start at 0.
    - Given index `i`, accessing the value `a[i]` is extremely efficient.
- **Array Declaration**: Declares the type and name of the array.
    - Example: `double[] a;`
- **Array Creation**: Allocates memory for the array using the `new` keyword and specifies its length.
    - Example: `a = new double;`
- **Accessing Array Elements**: Use the array name with the index in square brackets.
    - Example: `a = 3.0;`
- **Array Length**: Accessed using `a.length`.
- **Default Initialization**: Array elements are initialized to zero for numeric types and false for boolean types by default.
- **Literal Initialization**: Initialize an array with literal values within curly braces.
    - Example: `double[] x = {0.92, 0.02, 0.02, 0.02, 0.02};`

## 📝 Array Operations

### 👯 Copying Arrays

- Assigning one array to another (e.g., `b = a`) makes them refer to the same array, not a copy.
- To create a new copy, you must create a new array with the same length and copy each value individually.
    
    ```
    double[] b = new double[a.length];
    for (int i = 0; i < a.length; i++)
        b[i] = a[i];
    ```
    

### 🖨️ Typical Array Processing Examples

- **Creating an Array with Random Values**
    
    ```
    double[] a = new double[N];
    for (int i = 0; i < N; i++)
        a[i] = Math.random();
    ```
    
- **Printing Array Values**
    
    ```
     for (int i = 0; i < N; i++)
        System.out.println(a[i]);
    ```
    
- **Computing the Average of Array Values**
    
    ```
    double sum = 0.0;
    for (int i = 0; i < N; i++)
        sum += a[i];
    double average = sum / N;
    ```
    
- **Finding the Maximum Value in an Array**
    
    ```
    double max = a;
    for (int i = 1; i < N; i++)
        if (a[i] > max) max = a[i];
    ```
    
- **Accessing Command Line Arguments**: The `args` array contains the command-line arguments passed to a Java program.
- **Precomputed Values**: Use arrays to save computed values for later use, saving computation time.
    
    ```
        double[] harmonic = new double[n];
        for (int i = 1; i < n; i++)
            harmonic[i] = harmonic[i-1] + 1.0/i;
    ```
    
- **Simplifying Repetitive Code**: Use arrays to simplify the code that produces repetitive outputs.

### 🐛 Common Array Bugs

- **Undeclared Variable**: Forgetting to declare the array type.
    - Example: `double[] a;` without `a = new double[N];`
- **Uninitialized Array**: Forgetting to create the array with the `new` keyword.
- **Array Index Out of Bounds**: Accessing an index outside the valid range (0 to length - 1).
    - Example: `a` for an array of length 10.

## 🃏 Example: Deck of Cards

- Arrays can be used to represent a deck of cards.
- Three arrays are defined:
    - `rank`: Stores the ranks of the cards (2, 3, ..., A).
    - `suit`: Stores the suits of the cards (♣, ♦, ♥, ♠).
    - `deck`: Stores the full deck of cards.
- **Nested Loops**: Used to fill the `deck` array with all the cards.
    
    ```
    String[] deck = new String;
    for (int j = 0; j < 4; j++)
        for (int i = 0; i < 13; i++)
            deck[i + 13*j] = rank[i] + suit[j];
    ```
    
- The order of the nested loops affects the order in which the deck is filled but not the final contents.
- The index calculation `i + 13*j` maps 2D indices to a single index in the array.
- You can change the order of suits and ranks in the deck by switching the order of the nested for loops and adjusting the index calculation accordingly.

### 🎲 Array Applications: Dealing Cards

- **Random Sequence of Cards**: Print a random sequence of N cards using `Math.random()` to select a random index.
    
    ```
    for (int i = 0; i < N; i++) {
        int r = (int) (Math.random() * 52);
        System.out.println(deck[r]);
    }
    ```
    
    - Note that this method samples with replacement (same card can appear multiple times).
- **Shuffling a Deck of Cards**: Use the Fisher-Yates (or Knuth) shuffle to shuffle the deck in place.
    
    ```
    for (int i = 0; i < 52; i++) {
        int r = i + (int) (Math.random() * (52-i));
        String t = deck[r];
        deck[r] = deck[i];
        deck[i] = t;
    }
    ```
    
    - For each index `i`, select a random index `r` between `i` and the end, then exchange the values at those indices.
    - This method shuffles the deck such that all permutations are equally likely.
    - The code exchanges `deck[i]` with `deck[r]`, a random card from deck[i] to deck[n-1].

## 🎫 The Coupon Collector Problem

- **Problem**: How many random coupons (or cards) do you need to collect before you have one of each type, assuming each type is equally likely?
- **Simulation**: Use a boolean array `found` to track which coupons have been collected.
    - `found[r]` is true if the coupon `r` has been collected.
- **Algorithm**: Generate random coupon indices until all coupons have been collected.
    
    ```
     boolean[] found = new boolean[M];
     while (distinct < M) {
        int r = (int) (Math.random() * M);
        cards++;
        if (!found[r]) {
            distinct++;
            found[r] = true;
        }
     }
    ```
    
- The expected number of coupons needed to acquire a full collection is approximately `M ln M + 0.57721M`.
    - Where M is the number of different types of coupons.
- This problem has applications to many different fields, such as playing cards, baseball cards and magic cards.
- This demonstrates how computer simulation can help validate mathematical analysis.

## 🧮 Two-Dimensional Arrays

- Two-dimensional arrays are doubly-indexed sequences of values of the same type.
- They can be thought of as a table of numbers organized in a rectangle.
- Examples: Matrices, grades for students, pixels in an image, geographic data.
- **Declaration**: `double[][] a;`.
- **Creation**: `a = new double;`.
- **Access**: `a[i][j]`.
    - The first index is the row and the second index is the column.
- **Default Initialization**: Similar to 1D arrays, elements are initialized to 0 for numeric types.
- **Literal Initialization**: Initialize an array with literal values within nested curly braces.
    
    ```
    double[][] p = {
         { .92, .02, .02, .02, .02 },
        { .02, .92, .32, .32, .32 },
        { .02, .02, .02, .92, .02 },
        { .92, .02, .02, .02, .02 },
        { .47, .02, .47, .02, .02 },
    };
    ```
    
- **Ragged Arrays**: There is no requirement for rows to be of the same length.
- **Multidimensional Arrays**: Java can support arrays with any number of dimensions.

### ➕ Two-Dimensional Array Operations

- **Matrix Addition**: Add corresponding elements of two matrices using nested `for` loops.
- **Matrix Multiplication**: Compute the dot product of the rows and columns.
    
    ```
    double[][] c = new double[N][N];
    for (int i = 0; i < N; i++)
        for (int j = 0; j < N; j++)
            for (int k = 0; k < N; k++)
                c[i][j] += a[i][k] * b[k][j];
    ```
    
    - Requires a triple nested for loop.
    - Matrix multiplication of two N-by-N matrices requires N³ multiplications.

## 🐕 Example: Self-Avoiding Random Walk

- **Problem**: Simulate a random walk on a grid, where each step is a random direction, but you cannot revisit any previously visited grid location.
    - Does the walker escape the grid or reach a dead end?
- **Implementation**: Use a 2D boolean array to track visited positions.
    - `a[x][y]` is true if the position (x, y) has been visited.
- **Algorithm**: Start in the middle, choose a random direction, and update the position until the edge is reached or a dead end is encountered.
    - A dead end occurs if all neighbors have been visited.
- **Simulation**: Run the simulation many times and record the percentage of times a dead end is reached.
- **Results**: As the grid size increases, the probability of reaching a dead end increases.
    - For large N, the probability of a dead end is close to 1.
- This problem has applications to modeling polymers, solvents, magnetic materials, and other physical phenomena.
- The probability of reaching a dead end is unknown mathematically, demonstrating how simulation is sometimes the only effective way to study scientific phenomena.

## 🔑 Key Concepts

- **Arrays** provide a way to store and manipulate collections of data of the same type.
- Arrays use **indices** to access individual elements.
- Arrays are stored in **contiguous memory locations**.
- **Two-dimensional arrays** are useful for representing matrices and tables.
- **Simulation** can validate mathematical analysis and is sometimes the only method for studying a scientific phenomenon.
