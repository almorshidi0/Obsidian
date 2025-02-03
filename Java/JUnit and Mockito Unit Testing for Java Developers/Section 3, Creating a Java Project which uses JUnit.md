## Introduction 🎬

- **Goal:** This section guides you through creating a Java project that uses JUnit, setting the stage for learning and applying the JUnit framework.
- **Methods:** It demonstrates two ways to set up a project with JUnit: via an IDE (IntelliJ) using Apache Maven, or via the command line with Gradle.
- **Project Structure:** The section explores the generated project structure, emphasizing the separation of production and test code.
- **Key Guidelines:** You'll learn essential coding conventions for writing test code, including dependency scopes and naming conventions.
- **Outcome:** You'll have a solid project setup, ready to explore and utilize the JUnit framework in subsequent sections.

## Creating a Java Project with JUnit using Maven ⚙️

- **IDE Choice:** The course uses IntelliJ IDEA for demonstration, though other IDEs like Eclipse or NetBeans are suitable.
- **Maven Quickstart Archetype:** The project is created using the Maven Quickstart archetype which sets up a basic Hello World project.
- **Project Creation Steps:**
    - Select "Create New Project" in IntelliJ and choose a "Maven" project.
    - Use the "Maven Quickstart" archetype which sets up a basic project.
    - Assign a simple **Group ID** and **Artifact ID** (e.g., "My App").
    - Choose a location for the project. The project will be created in that location.
    - Enable "Auto Import" to ensure dependencies are immediately reflected in IntelliJ's classpath.
- **Dependency Management:**
    - **`pom.xml` File:** Dependencies are added to the `pom.xml` file.
    - **Adding JUnit:** A JUnit dependency is added to the `pom.xml` file. The course uses version 4.12.
    - **Transitive Dependency:** JUnit includes the **Hamcrest library** as a transitive dependency, which JUnit needs to operate.
    - **External Libraries:** The JUnit and Hamcrest libraries appear under the "External Libraries" section.
- **Project Setup Confirmation:** After adding the dependencies, the project is set up to use JUnit.

## Exploring the Project Structure 📂

- **Source Folders:** The generated project contains a "source" folder with two subdirectories: "main" and "test".
    - `source/main/java`: Where **production code** resides.
    - `source/main/resources`: Holds **classpath resources** for production.
    - `source/test/java`: Where **test source code** is located.
- **Color Coding:** IntelliJ color-codes the folders: blue for production source code and green for test source code.
- **Separation of Source Trees:** Production and test source codes are kept separate.
    - This separation facilitates compiling and bundling different source sets as needed.
- **Dependency Scope:**
    - **Test Scope:** The JUnit dependency is declared as a "test scope" dependency.
        - This ensures that JUnit is only accessible to code within the `source/test/java` folder.
        - It prevents JUnit from being included in the production application.
        - Libraries used for testing, such as Mockito (introduced later), should also be "test scope" dependencies.
    - **Hamcrest Scope:** The Hamcrest dependency inherits the "test scope" of JUnit because it's a transitive dependency of JUnit.

## Basic Conventions for Creating Unit Tests 📝

- **Production Class Example**: A simple calculator class is created in the production source folder in a package called 'com.example'.
- **Package Structure:**
    - Test classes should reside in the same package as the corresponding production class, but within the test source directory.
    - This structure mirrors the production package structure.
    - A shortcut is provided to copy the package name of the production class when creating the test package.
- **Test Class Naming:**
    - Test classes should have the same name as the production class, but with a "Test" suffix.
        - For example, `Calculator` has a corresponding test class called `CalculatorTest`.
        - If there were a `DataService` class, its test would be called `DataServiceTest`.
- **Access Rights:** Placing the test class in the same package as the production class gives the test the same access rights.
    - This allows the test class to access members of the production class, even if they are not declared as public.
    - This is useful for setting up tests and accessing other classes within the same package.

## Key Takeaways ✅

- **Project Setup:** The course emphasizes setting up a project correctly with Maven and JUnit.
- **Dependency Scopes:** Understanding dependency scopes is crucial to avoid bundling test libraries with production code.
- **Naming Conventions:** Consistent naming conventions for test classes and package structures ensure clarity and maintainability.
- **Separation of Concerns:** The structure of the project ensures a clear separation between production and test code.
