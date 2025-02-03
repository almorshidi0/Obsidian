This episode introduces the concept of **algorithms** and explores different sorting algorithms.

## 🤔 What is an Algorithm?

- An algorithm is a set of specific steps used to complete a computation.
- Different algorithms can achieve the same result, but some are more efficient than others.
- Generally, fewer steps to compute mean a better algorithm, though memory usage can also be a factor.
- The term "algorithm" comes from Persian polymath **Muḥammad ibn Mūsā al-Khwārizmī**, a father of algebra.
- Crafting efficient algorithms led to the science of computation, which evolved into computer science.

## ⚙️ Sorting Algorithms: Organizing Data

- **Sorting** is a common algorithmic problem, and computers sort data all the time.
- Examples include arranging airfares, emails, or contacts.
- There are many different sorting algorithms, such as Bubble Sort and Spaghetti Sort.

### ➡️ Selection Sort

- A simple algorithm that involves scanning an array to find the smallest number.
- This number is swapped with the number in the top position, and the process is repeated, moving down the array.
- The pseudo-code for Selection Sort involves nested **FOR loops**.
- The complexity of Selection Sort is **N squared**.
    - If you want to sort N items, you have to loop N times, inside of which, you loop N times.
    - This means for an array of 8 items, the algorithm loops roughly 64 times.
    - If the array increases to 80 items, the running time increases to 6,400.
    - This relationship between input size and steps characterizes the complexity of the algorithm and is expressed using "big O notation".
    - N squared is not considered efficient.

### ➗ Merge Sort

- A more efficient sorting algorithm than Selection Sort.
- First, it checks if the size of the array is greater than 1. If it is, it splits the array in half.
- This splitting continues until you have arrays with only one item each.
- Then, the algorithm merges pairs of sorted arrays into larger sorted arrays.
- This process repeats until the entire array is sorted.
- The complexity of Merge Sort is **N times the Log of N**.
    - The N comes from the number of times we need to compare and merge items.
    - The Log N comes from the number of merge steps, like splitting an array of 8 into 4, then 2, then 1 (3 splits).
    - Doubling the size of the array only increases the number of split steps by 1.
    - Even with a large increase in the size of the array, the number of split steps remains relatively low.

## 🗺️ Graph Search Algorithms: Navigating Networks

- A **graph** is a network of nodes connected by lines, like a map with cities and roads.
- Each line can have a cost or weight associated with it.
- A **brute force** approach to finding the fastest route would involve trying every single path. This has a complexity of **N factorial**, which is inefficient.

### 🧭 Dijkstra's Algorithm

- A classic algorithm invented by Edsger Dijkstra for finding the shortest path in a graph.
- It starts at the node with the lowest cost, and then explores all paths to connecting nodes.
- The algorithm keeps a running cost from the start and updates paths if a lower cost is found.
- Dijkstra's original algorithm had a complexity of **N squared**.
- An improved version has a complexity of **N times the Log of N, plus the number of lines**.
- Services like Google Maps use algorithms like Dijkstra's to find the best routes.

## 🌐 Conclusion

- Algorithms are everywhere and essential to the modern world.
- Computer scientists leverage existing algorithms and write new ones when needed.

This episode provides a foundational understanding of algorithms, illustrating their importance in sorting data and navigating networks.