This section provides a hands-on approach to understanding JUnit, focusing on practical application and core concepts. Here’s a breakdown:

## Getting Started 🎬

- The goal is to learn JUnit through simple examples, focusing on the framework itself rather than complex code.
- By taking "easy-to-walk steps," you can master the core concepts, which can later be applied to more complex projects.
- The approach is to explain JUnit features "just-in-time," in context as they are needed.

## Creating and Running Tests ✅

- To create a test method, use the **`@Test` annotation**. This marks a method as a test case.
- A basic test method is structured like this: `public void testAdd() {}`.
- JUnit uses the `org.junit.Test` annotation, which you need to import.
- After adding the `@Test` annotation, the IDE will recognize the method as a test and provide a "run" option.
- **Test Success** is indicated by green checkmarks ✅ in the IDE, meaning all test methods in the class have passed. The output will also confirm that tests have passed.

## Understanding Test Failures ❌

- **Test Failures** are indicated by red marks 🟥.
- If an exception is thrown during test execution and is not expected, the test fails.
- A full stack trace is provided to pinpoint the exact location and cause of the failure.

### Expected Exceptions ⛑️

- Use `expected = RuntimeException.class` within the `@Test` annotation to indicate that a test should expect a specific exception. If this exception is thrown the test will pass.
- This is useful for testing validation routines.
- **Note**: this mechanism is useful if you don't need to do any extra assertions within the catch block; otherwise a try/catch is necessary.

### Explicitly Failing Tests 💥

- Use `Assert.fail("message")` to explicitly fail a test, usually with a descriptive message.
- This can be used in a try-catch block to verify that an exception was thrown in the class being tested. If you end up in the catch block, that indicates that the expected exception was thrown and you can check the exception state within the catch block.
- If you do not end up in the catch block, you can explicitly fail the test.

## JUnit Assertions API 🤔

- JUnit provides an **`Assert` class** with various methods for making assertions.
- Common assertions include:
    - `assertNotNull(object)`: Checks if an object is not null.
    - `assertTrue(boolean)`: Checks if a boolean condition is true.
    - `assertArrayEquals(array1, array2)`: Checks if two arrays are equal.
    - `assertEquals(expected, actual)`: Checks if two objects are equal.
    - There are also corresponding `assertNotEquals` and `assertFalse` methods.
- **Important**: In `assertEquals`, the first argument is the expected value, and the second is the actual value.
- Experiment with `assert.` in your code to explore available methods.

## Structuring Tests: Arrange-Act-Assert (AAA) 📐

- Structure your tests into three sections: **Arrange, Act, and Assert**.
- **Arrange**: Set up the test environment including creating objects and setting up mocks.
- **Act**: Invoke the method that you want to test.
- **Assert**: Use JUnit's assertion methods to check the state after the method execution.
- AAA can also be thought of as Given, When, Then, popular in Behaviour Driven Development (BDD).
- Sticking to AAA provides a good template for writing tests.

## Execution of Assertions and Fail-Fast Mechanism 🏃‍♀️

- JUnit executes assertions sequentially within the test method.
- If an assertion fails, the test fails immediately, this is known as a **fail-fast mechanism**.
- The stack trace indicates which specific assertion caused the failure.
- This helps pinpoint the cause of the bug.
- Assertions are usually applied to data members that come back off of the class being tested.
- You can add static imports for JUnit assertions to make code more readable.

### Descriptive Messages in Assertions 💬

- Add a descriptive message as the first parameter to an assertion to provide context when a test fails. For example: `assertEquals("10 should always equal 10", expected, actual);`.

## Coding a Unit Test with AAA 👩‍💻

- Example test code follows the Arrange, Act, Assert pattern.
- Arrange: set up variables, instantiate objects:

```
 int a = 10;
 int b = 20;
```

- Act: invoke the method you are testing:
    
    ```
    int result = calculator.add(a, b);
    ```
    
- Assert: assert the output you expect against the actual output:
    
    ```
    assertEquals(30, result);
    ```
    
- By following this pattern you can write robust tests.

## Keeping Test Setup DRY with @Before 💧

- The **`@Before` annotation** allows you to define a setup method that is executed before each test method, keeping test code DRY (Don't Repeat Yourself).
- This method is used to set up the **test fixture** - the set of objects and states needed for the test.
- A `@Before` method is typically used to instantiate the class being tested.
- Using `@Before` eliminates setup code duplication.
- The test fixture setup in the `@Before` method is executed fresh for each test.
- The test class itself is also recreated for each test.

### Additional annotations ⚙️

- `@After`: tear down any state from the fixture.
- `@BeforeClass`: set up for all test methods at a class level.
- `@AfterClass`: tear down for all test methods at a class level.

## Conclusion ✅

This section provides a solid foundation for understanding JUnit and writing effective unit tests. By following the concepts and structure outlined, you'll be well-prepared to write robust tests for your projects. This knowledge serves as a prerequisite to using Mockito.
