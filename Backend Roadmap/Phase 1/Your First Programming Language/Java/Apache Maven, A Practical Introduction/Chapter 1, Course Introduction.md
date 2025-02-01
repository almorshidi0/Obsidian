This chapter introduces the Apache Maven course and provides a foundation for understanding how to use Maven effectively.

## 🎬 Course Introduction
*   **Welcome to the Apache Maven Course!** 🎉 This course is designed to teach you how the Apache Maven build tool works, starting from the ground up.
*   **Java Build Tools:**  There are 3 main build tools in the Java world: Ant, Maven, and Gradle.
    *   Ant was the main build tool early in Java’s history, but it is now considered outdated.
    *  **Maven** is the most popular tool for building Java projects in the industry.
    *   Gradle is a newer build tool that is gaining traction.
*  **Why Maven?** 🤔 Maven is the most commonly used build tool for Java projects globally, making it essential to understand.
*   **Course Goal:** The course aims to provide both theoretical knowledge and hands-on experience with Maven. You'll learn by using the command line first, and then IDEs like Eclipse and IntelliJ later.
*  **Command Line Emphasis:** Learning the command line is the best way to understand how Maven works, even if you're not a command-line person. This approach will provide a solid foundation for using Maven plugins in IDEs.

## 🛠️ Course Structure
*   **Section 1: Course Introduction** (current section) - A high-level overview of Maven and generating a Java project from scratch.
*   **Section 2: Installation Basics** - How to install Maven on Windows, Linux, and Mac.
*   **Section 3: Fundamentals of Maven** - An in-depth look at how Maven works, not just superficial points. Includes demos to show Maven in action. It will cover all the major concepts you need to know to use it effectively.
*   **Section 4: Working with Maven in IDEs** - Using Maven in popular IDEs like IntelliJ and Eclipse.
*   **Bonus Resources:** Cheat sheets for quick reference.
*  **Focus:** The course is 100% focused on the essentials, with no fluff or filler, to help you become productive quickly.

## 💻 Setting Up the Command Line
*   **Command Line Defined:** The command line allows you to type commands at the operating system level.
*   **Accessing the Command Line:** The way to access the command line varies depending on the operating system.
    *   **Windows:** Open the "Run" dialog (Win + R), type `cmd`, and press Enter.
        *  Type `dir` and press enter to test if you get a directory listing
    *   **Linux:** Right-click on the desktop and select "New Terminal Session" or similar.
         *  Type `ls` and press enter to test if you get a directory listing
    *   **Mac:** Open "Terminal" in the "Utilities" folder within "Applications".
          *  Type `ls` and press enter to test if you get a directory listing

## 📝 Creating a Maven Project

*   **Maven Archetype Plugin:** Use the Maven archetype plugin and its generate goal to create a new Maven project.
*   **Archetypes:** Maven archetypes are templates for projects, consisting of files and folders, which form the basis of new projects.
*   **Filtering Archetypes:** You can filter the list of archetypes.
    *   Use the `-D` switch followed by `filter=group ID` to filter the archetypes.
    *   Example: `mvn archetype:generate -D filter=org.apache.maven.archetypes:`
    *   When referring to artifacts in Maven, you have three parts: **group ID**, **artifact ID**, and **version**, separated by colons.
*   **Quickstart Archetype:** The default archetype used by Maven is the **quickstart archetype**.
*   **Creating a Project:** After selecting the archetype, you need to define:
    *   **Group ID:** (e.g., `com.zention.training.demo`)
    *   **Artifact ID:** The name of the artifact (e.g., `my-app`)
    *   **Version:** (e.g., `1.0-SNAPSHOT`)
    *   **Package:** Accept default package
*   **Result:**  A new project is created with the specified artifact ID.
