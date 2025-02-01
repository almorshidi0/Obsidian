## 💡 Overview of Abstract Data Types (ADTs)

- A **data type** is a set of values and a set of operations on those values.
- Primitive types in Java (like `int`, `double`) have values that directly map to machine representations and operations that map to machine instructions.
- An **abstract data type (ADT)** is a data type where the representation is hidden from the client.
    - Clients use ADTs without needing to know the implementation details.
    - This is a core concept in **object-oriented programming (OOP)**.
- OOP involves creating your own data types and using them to manipulate objects.
- An object holds a data type value, and variables refer to objects.

## 🎨 Color ADT

- The Color ADT represents color values using the RGB color model.
    
    - A color is defined by three 8-bit integers (0-255) that represent the intensity of the red, green, and blue components.
- **Values:** Three 8-bit integers representing red, green, and blue intensities.
    
- **Operations (API):**
    
    - `Color(int r, int g, int b)`: Constructor to create a color object.
    - `getRed()`, `getGreen()`, `getBlue()`: Get the intensity of each color component.
    - `brighter()`, `darker()`: Create brighter or darker versions of the color.
    - `toString()`: Get a string representation of the color.
    - `equals(Color c)`: Check if two colors are the same.
- **Example Client: Albers Squares**
    
    - The `AlbersSquares` program takes six command-line arguments (RGB for two colors) and displays two squares with those colors.
    - It uses the `Color` constructor and methods like `setPenColor` and `filledSquare` to draw the squares.
- **Monochrome Luminance:**
    
    - The luminance of a color quantifies its effective brightness.
    - Calculated using the formula: `Y = 0.299r + 0.587g + 0.114b`.
    - Applications:
        - Choosing colors for displayed text.
        - Converting colors to grayscale.
- **Color Compatibility:**
    
    - The absolute value of the difference in luminance between two colors should be greater than 128 for readability.
    - The `compatible(Color a, Color b)` method checks this.
- **Grayscale Conversion:**
    
    - When R, G, and B values are the same, the color is on a grayscale (0 = black, 255 = white).
    - The `toGray(Color c)` method converts a color to grayscale by setting all three components to its luminance.
- **OOP Context**:
    
    - Java's representation of color is hidden, making it an ADT.

## 🖼️ Picture ADT

- A Picture is a 2D array of pixels, where each pixel has a color.
    - Values are 2D arrays of Colors.
- **Operations (API):**
    - `Picture(String filename)`: Create a picture from a file.
    - `Picture(int w, int h)`: Create a blank w-by-h picture.
    - `width()`: Get the width of the picture.
    - `height()`: Get the height of the picture.
    - `get(int col, int row)`: Get the color of the pixel at the given column and row.
    - `set(int col, int row, Color c)`: Set the color of the pixel at the given column and row.
    - `show()`: Display the image in a window.
    - `save(String filename)`: Save the picture to a file.
- **Example Client: Grayscale Filter**
    - The `Grayscale` program converts a color image to grayscale by applying the `Luminance.toGray()` method to each pixel.
- **Pop Quizzes:**
    - A code that sets each pixel to its current color has no effect (just shows the picture).
    - An attempt to turn an image upside down by directly setting pixel colors in the same picture fails because it overwrites pixels, creating a bug.
    - To correctly flip an image vertically, a new target picture is created and the pixels are set in reverse row order from the source picture.
- **Example Client: Scaling Filter**
    - The `Scale` program scales an image to a specified width and height.
    - It scales the column and row indices from the target image to the source image, and sets each target pixel to the corresponding source pixel's color.
- **Other Image Processing Effects**: Many other image processing effects like glass filter, edge detection, wave filter, RGB color separation, and swirl filter are possible.

## 🔤 String ADT

- A String is a sequence of Unicode characters.
- **Operations (API):**
    - `String(String s)`: Create a string with the same value.
    - `length()`: Get the length of the string.
    - `charAt(int i)`: Get the character at index i.
    - `substring(int i, int j)`: Get a substring from index i to j-1.
    - `contains(String sub)`: Check if the string contains a substring.
    - `startsWith(String pre)`: Check if the string starts with a prefix.
    - `endsWith()`: Check if the string ends with a suffix.
    - `indexOf()`: Search through string to find the first occurance of a given pattern.
    - `concat()`: Concatenate a string to the end of another string.
    - `replace()`: Replace all occurances of a given string with another string.
    - `split()`: Split a string into an array based on a delimiter.
    - `equals()`: Compare a string to another string by value, not reference.
- **Example Clients**:
    - Palindrome check.
    - Finding lines containing a specific string in standard input.
    - Searching for hyperlinks in a text file.
- **Genomics Example**:
    - Genomes are represented as strings over the A, C, T, G alphabet.
    - A gene is a substring made of codons (three nucleotides).
    - Genes are preceded by ATG (start codon) and succeeded by TAG, TAA, or TGA (stop codons).
    - The `Gene` program checks if a given DNA string is a potential gene.
    - A more complex algorithm scans left to right, identifying start and stop codons to find genes.
- **OOP Context**:
    - String memory representation may include a length and a memory address where the characters are stored.
    - String variables are references to objects.
    - `==` compares references, while `.equals()` compares character sequences.

## 🔑 Key Concepts

- **Abstraction**: Hiding implementation details and focusing on the API.
- **Object References**: Variables refer to objects, not the values themselves.
- **Constructors**: Create new objects using the `new` keyword.
- **Methods**: Apply operations to objects using the dot (`.`) operator.
- **Immutability**: String objects are immutable meaning that their value can't be modified after they are created.

## 📝 Summary

- Abstract data types (ADTs) allow you to create and use your own data types in your programs by defining a set of values and the operations on them.
- The representation of an ADT is hidden from the client, enabling flexibility and abstraction.
- Object-oriented programming (OOP) utilizes ADTs to manipulate objects that hold data type values.
- The `Color`, `Picture`, and `String` ADTs are examples of how you can work with real-world concepts using well-defined operations.
- You can apply the scientific method to study ADTs, analyze how well they meet requirements, and invent better ones.
