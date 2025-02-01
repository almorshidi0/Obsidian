## 🤔 The Challenge of Performance

- The challenge of ensuring programs run efficiently has been around since the earliest days of computing.
- Charles Babbage, in the 1800s, questioned how to achieve results in the shortest time with his mechanical "Analytical Engine".
- The modern version of this challenge is: Will my program be able to solve a large, practical problem?
- If not, how can I understand and improve its performance characteristics?
- **Key insight:** Use the scientific method to understand performance.

## 🎯 Why Study Program Performance?

- **To predict program behavior:** Will it finish? When will it finish?
- **To compare algorithms and implementations:** Will this change make my program faster? How can I make my program faster?
- **To develop a basis for understanding the problem and for designing new algorithms:** Enabling new technology and new research.

## 🧪 Empirical Analysis: Running Experiments

- **Find representative inputs**
    - Collect actual data, or write a program to generate representative inputs.
- **Run experiments**
    - Start with a moderate input size (N).
    - Measure and record running time.
    - Double the input size.
    - Repeat.
    - Tabulate and plot the results.
- **Measure running time** by recording the current time before and after the code being timed.
- **Data analysis**
    - Plot on a log-log scale.
    - If points are on a straight line, a power law holds—a curve of the form aNb fits.
    - The exponent _b_ is the slope of the line.
    - Solve for _a_ using the data.
- **Experimentation in CS is virtually free**, compared to other sciences.
- **Bottom line:** No excuse not to run experiments to understand costs.

## 🧮 Mathematical Models: Understanding Performance

- **Goal**: To write down an accurate formula for the running time of a program.
    - Determine the set of operations.
    - Find the cost of each operation.
    - Find the frequency of execution of each operation.
    - Total running time = sum of cost × frequency for all operations.
- **Warmup examples:** 1-sum, 2-sum
    - Demonstrate how to create a table of operations, costs, and frequencies
    - In 1-sum, the number of increments is variable based on the input, but the other frequencies can be determined by the code alone.
    - In 2-sum, the frequency of the operations increases, depending on the nested loops.
- **Tilde notation** (~): Used to simplify calculations by focusing on the fastest-growing term.
    - f(N) ~ g(N) means f(N)/g(N) approaches 1 as N approaches infinity.
    - Eliminates dependence on input by ignoring slower-growing terms and focusing on the dominant term.
- **Example**: For 3-sum, the mathematical model for the running time is ~ N3/2 nanoseconds. This matches the empirical hypothesis of 4.84 × 10-10 × N3.

## 🔬 Scientific Method Applied to Programs

- **Observe** the time a program takes to run.
- **Hypothesize** a model consistent with observations (e.g., a power law curve).
- **Predict** events using the hypothesis.
- **Verify** the predictions by making further observations.
- **Validate** by refining until hypothesis and observations agree.
- Mathematical models are easier to formulate in CS than in other sciences because programs are built from relatively few primitives.

## 👯 Doubling Method: A Practical Approach

- **Hypothesis:** Running time of a program is TN ~ aNb.
    - **Consequence:** As N increases, T2N/TN approaches 2b.
- **Steps:**
    - Start with a moderate input size.
    - Measure and record running time.
    - Double the size.
    - Repeat while you can afford it.
    - Verify that ratios of running times approach 2b.
    - Predict by extrapolation: multiply by 2b to estimate T2N and repeat.
    - **No need to calculate a (!)**
- **Order of growth**: If a function f(N) ~ ag(N), then g(N) is the order of growth of the function.
- **Order of growth** is a property of the algorithm, not the computer or system.
- When a program is executed on a computer that is X times faster, the program is expected to be X times faster.
- The order of growth of the running time of a program is typically Nb(logN)c.
- **Common orders of growth:** Constant, Logarithmic, Linear, Linearithmic, Quadratic, Cubic
    - Each classification has a factor by which the running time will increase if the input size doubles.
- If the math model gives the order of growth, use the doubling method to validate the 2b ratio.
- If not, use the doubling method and solve for b = lg(TN/TN/2) to estimate the order of growth to be Nb.

## 📈 Impact of Moore's Law

- **Moore's Law:** Computer power increases roughly by a factor of 2 every 2 years.
- If problem size doubles every 2 years, costs vary based on the algorithm's order of growth:
    - Linear and Linearithmic algorithms: Cost remains roughly the same.
    - Quadratic algorithms: Cost doubles every two years.
    - Cubic algorithms: Cost quadruples every two years.
- **Important Implication:** You can't afford to use a quadratic or worse algorithm to address increasing problem sizes.

## ⚠️ Caveats and Considerations

- It is not always easy to predict performance.
- **Challenges:**
    - Leading term may oscillate.
    - Other apps may be running on the computer.
    - Machine model might be too simple (e.g., parallel processors, cache).
    - Math model may need more terms.
    - Input model may be too simple.
- Doubling method is robust in the face of many of these challenges.

## 💡 Examples

- **Gambler's Ruin Simulation:** Running time is proportional to N2.
- **Mystery Program:** If the ratios of running times when doubling N approach 4, the order of growth is N2.
- **Coupon Collector:** Running time is proportional to N log N.
- **Memory Analysis**: It is important to analyze memory requirements, as programs can run out of memory before they run out of time.

## 🎯 Summary

- Use computational experiments, mathematical analysis, and the scientific method to understand if your program might be useful to solve a large problem.
- If the program is not fast enough, buy a new computer, learn a better algorithm, or invent a better algorithm.
- **Lesson:** Performance matters!
