## Introduction 🚀

- **Best Practices:** This section focuses on industry-standard best practices for writing unit tests.
- **Importance:** Adhering to these principles is crucial for writing high-quality, maintainable tests.
- **Benefits:** Good unit tests form a safety net that helps identify errors quickly and improves code robustness.
- **Goal:** To equip you with the foundational knowledge necessary to write effective tests.

## What is Unit Testing? 🤔

- **Definition:** Unit testing involves testing individual "units" of code.
- **Unit Varies:** The definition of a "unit" depends on the programming language or methodology.
- **Java Focus:** In Java, a unit typically refers to a **class**.
- **Purpose:** To ensure that classes perform as expected, handle various inputs without errors, and interact predictably.
- **Goal:** To produce high-quality, reliable, and bug-free production code.
- **Impact:** Reduces the chances of errors, resulting in a better user experience and more peaceful nights for developers.
- **Key Concept:** Unit tests are a way to iron out bugs so that the interactions between objects are predictable and robust.

## What is JUnit? 🧰

- **Framework:** JUnit is a framework for writing unit tests in Java.
- **Structured Approach:** It provides a structured way to conduct tests.
- **Java Framework Components:**
    - **Interfaces:** May need to be implemented.
    - **Classes:** May need to be extended (abstract classes), or used as helpers.
    - **Annotations:** Used to signify special aspects of classes, methods, or fields.
- **API (Application Programming Interface):** A collection of interfaces, classes, and annotations that allows interaction with the library or framework.
- **JUnit's API:** Provides well-defined callbacks and lifecycle methods for test code.
- **Integration:** Integrates with IDEs (IntelliJ, Eclipse) and build tools (Maven, Gradle).
- **Key Types in JUnit:**
    - Classes like `assert` and `JUnit test runner`.
    - Annotations like `@Test`, `@RunWith`, and `@Before`.
- **Functionality:**
    - Enables the writing of test cases via the `@Test` annotation.
    - Allows checking of values using assertions (e.g., `assert` class).
    - Provides test runners to execute tests and view results.

## Introducing a Simple Unit Test in JUnit 🧪

- **Starting Point:** Every test begins with identifying the unit to be tested (a class).
- **Example Class:** A simple class with a method that returns a greeting message is used as an example.
- **Test Class:** A separate class to house the test methods.
- **Test Methods:** Methods within the test class, often named using a convention (e.g. `test_greet`).
- **`@Test` Annotation:** Marks a method as a test case for JUnit to execute.
- **Assertions:** Used to verify if the output of the method matches the expected result.
    - **`assertNotNull`:** Checks if the result is not null.
    - **`assertEquals`:** Checks if the result is equal to the expected value.
- **Test Failure:** If an assertion is false, the test fails with an assertion error.

## Structure of a Unit Test 🧱

- **Logical Structure:** Unit test methods generally follow a logical structure.
- **Two Main Structures:**
    - **Arrange-Act-Assert (AAA):** Focuses on setting up the test, invoking the method, and checking results.
        - **Arrange:** Sets up the test context and prepares the test environment.
        - **Act:** Invokes the method under test.
        - **Assert:** Verifies the outcome using assertions.
    - **Given-When-Then:** Focuses on the behavior of the system, mainly used in Behavior Driven Testing.
        - **Given:** Sets up preconditions or the state of the system.
        - **When:** Performs the action being tested.
        - **Then:** Asserts the post conditions, the state of the system after the action.
- **Pre and Post Conditions:** A way of looking at things. Preconditions are what should be true before the test, and postconditions are what should be true after the test.
- **AAA vs. Given-When-Then:**
    - AAA is popular with developers, focusing on implementation details.
    - Given-When-Then is often used in business-focused tests such as integration and acceptance tests.
- **Consistency:** Choose one style and stick to it.
- **Clarity:** Comment the test code with the AAA or Given-When-Then phases to make it clear.

## Conventions for Writing Unit Tests ✍️

- **Test Class Naming:** Same name as the production class, but with a `Test` suffix (e.g., `Grita` becomes `GritaTest`).
- **Visibility:** Test classes are declared as public, not abstract or final.
- **Package:** Test classes should be placed in the same package as the production code class, but in the test source folder rather than the production source folder.
- **Reason for Same Package:** This gives test classes the same access rights as the production classes, so they can interact and set up tests appropriately.
- **Simplicity:** Keep tests simple and adhere to conventions to make them easier to write and maintain.

## Characteristics of Proper Unit Tests ✅

- **Isolation:** Unit tests should be isolated from external factors.
    - No database access, messaging systems, or network connections.
    - Reduces the number of moving parts, making it easier to identify errors.
    - Use mock objects to simulate collaborators to ensure this isolation.
- **Mock Objects:** Substitutes for real collaborators, allowing controlled behavior during tests.
    - Helps to test different scenarios, like exceptions.
- **Speed of Execution:** Tests should run as quickly as possible.
    - Enables frequent running of tests during development.
- **Consistency:** Test runs should be consistent, producing the same result each time.
    - Should not depend on time of day, location, or operating system.
- **Reliability:** Tests should be reliable and not depend on the order in which they are run or on other tests.
- **Regular Execution:** Run tests regularly to act as an early warning system and correct issues quickly.

## What are Assertions? 🤔

- **Definition:** Assertions are statements of fact or truths at a particular point during the test execution.
- **Purpose:**
    - Pass the test if the assertion is true.
    - Fail the test if the assertion is false, indicating an issue in the code.
- **Assertions in Plain Language:** First think about what should be true, then translate that into code using the assert API.
- **Belief vs. Truth:** Assertions are a belief that something is true, not necessarily a fact, and the unit test determines if the assertion evaluates to true or false.
- **Test Outcomes:** Tests pass only when all assertions in the test are true; one false assertion causes a test to fail.
- **Types of Assertions:**
    - **Preconditions:** Assertions that test the state of the world before executing the method being tested.
    - **Postconditions:** Assertions that test the state of the world after executing the method being tested.
- **Common Assertion Checks:**
    - Checking if something is `true` or `false`.
    - Checking if two things are `equal` or `not equal`.
    - Checking if two things are the `same` (identical references) or `not the same`.
- **JUnit's `Assert` Class:** Provides a foundation of assertion methods.
- **Hamcrest Library:** A more expressive assertion library (bundled with JUnit) that uses readable syntax based on "matchers" to create more complex assertions.
