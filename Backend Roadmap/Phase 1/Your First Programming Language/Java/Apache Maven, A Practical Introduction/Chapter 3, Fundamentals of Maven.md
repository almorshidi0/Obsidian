This chapter dives into the fundamentals of Maven, covering project structure, the Project Object Model (POM), build lifecycles, dependencies, and plugins.

## 🎬 Introduction to Maven Fundamentals

*   This is a key section that explains how Maven works from the ground up.
*   You'll learn about the **Project Object Model (POM)**, build lifecycles, plugins, and dependencies.
*   Understanding **dependencies**, how they're declared and managed, is crucial. You'll also learn how Maven resolves dependencies.

## 🗂️ Maven Project Structure

*   Maven uses a standard project structure.
*   The **pom.xml** file is at the root of all Maven projects.
    *   It represents the **Project Object Model (POM)**, which defines the project's properties.
*   **GAV Coordinates**: The pom.xml contains the **Group ID**, **Artifact ID**, and **Version** (GAV) coordinates.
    *   These coordinates determine where the artifact lives in Maven repositories.
    *   The group ID is a namespace, similar to a Java package, for grouping projects.
    *   The artifact ID is the name of the artifact produced by the build.
    *   The version specifies the artifact's version.
*   **Source Directories**: There are two main directory trees:
    *   `src/main/java`: For production source code.
    *   `src/test/java`: For test source code (unit tests, integration tests, etc.).
    *   This separation of concerns prevents test code from being included in production artifacts.
*   **Example Classes**: Maven includes two example classes:
    *   `App.java`: A simple "Hello World" application.
    *   `AppTest.java`: A basic test class using JUnit.
        *   Maven includes an old version of JUnit by default (version 3.8.1).

## ⚙️ Performing Simple Build Tasks

*   Maven provides a standardized build process. You are customizing an existing standardized build, not writing a build file.
*   **Target Directory:** Maven creates a `target` directory for build artifacts.
    *   This directory is created during the build process.
*   **Build Command:** Use `mvn package` to create a JAR file of the project.
    *   The JAR file is placed in the `target` directory.
*  **Build Artifacts:** The generated jar file only includes compiled production code, not test code.
*   **Dependency Scopes:** Maven uses dependency scopes to differentiate between production and test code.
*   **Maven Actions:** Maven automates build steps, such as compiling, copying class files, and creating JARs.
*   **Build Steps**: When you execute `mvn package`, Maven executes several steps such as:
    *   Compiling source code using the compiler plugin.
    *   Testing source code using the surefire plugin.
    *   Building the JAR file.
*   **Other Commands**:
    *   `mvn clean`: Clears the project by deleting the `target` directory.
    *   `mvn test`: Runs the tests.
    *   `mvn compile`: Compiles the production source code.
    *   `mvn test-compile`: Compiles the test source code.
*   Maven plugins provide built-in functionality, eliminating the need for build scripts.

## ⚙️ Maven Invocation Modes

*   Maven can be invoked in two ways:
    *   **Phase:** `mvn <phase>` invokes a phase in the build lifecycle (e.g., `mvn compile`, `mvn package`, `mvn clean`).
    *   **Goal:** `mvn <plugin>:<goal>` invokes a specific goal of a plugin (e.g., `mvn archetype:generate`).
*   **Format of Commands**:
    *   **Phase**: `mvn <phase>`.
    *  **Goal**: `mvn <plugin>:<goal>`.

## 📝 The Project Object Model (POM)

*   **POM Overview:** The POM describes how Maven sees the project, including configurations, properties, and build customizations.
*   **Minimal POM:** A minimal POM contains the model version, group ID, artifact ID, version, and packaging type.
    *  The **model version** is usually `4.0.0` and doesn't change much between Maven versions.
    *  The **packaging type** can be `jar`, `war`, etc. which determines the type of artifact generated.
*   **GAV Coordinates:** The Group ID, Artifact ID, and Version (GAV) are essential properties.
    *   They specify the artifact's location in Maven repositories.
*  **Maven Repositories**:
    *   **External Repositories**: Public open-source repositories like Maven Central.
    *   **Internal Repositories**: Corporate repositories (e.g., Nexus, Artifactory).
    *   **Local Repo Cache**: A local repository on your system where dependencies are stored.
*   **Local Repo Cache Demo:**
    *   The local repo cache is located in `~/.m2/repository`.
    *   When you install an artifact, it is placed in a folder structure based on the GAV coordinates.
    *   The `install` command compiles the code, creates a JAR, and installs it in the local repository.
    *   The pom.xml file is also deployed alongside the jar.
    *   The GAV coordinates are used both for publishing artifacts and declaring dependencies.
*   **POM Structure:** The POM file contains:
    *   Basic project information (GAV coordinates, packaging type).
    *   **Dependencies section:** Specifies project dependencies.
    *   **Build section:** Includes build customizations and plugin configurations.
        *  The **plugins section** is where you configure and customize build plugins.

## 🦸 The Super POM and Effective POM

*   **Super POM:** All Maven projects inherit from a larger POM file called the Super POM.
    *   The Super POM is located in the Maven installation directory, inside `lib/maven-model-builder-<version>.jar/org/apache/maven/model/pom-4.0.0.xml`.
    *   It provides default settings, repositories, and plugin configurations.
    *  **Convention over configuration** - Maven uses a standard build lifecycle, structure, and properties.
    *   The Super POM defines the Maven Central Repository as the default.
    *   It also defines default source and resource directories, and the naming convention of the final artifact.
*   **Effective POM:** The Effective POM is the merged project object model of the Super POM and your project's pom.xml.
    *   You can view the Effective POM using `mvn help:effective-pom`.
    *   It shows the full set of properties, configuration and customizations applicable to the project.
    *   The Effective POM shows the settings from your `pom.xml`, as well as the defaults from the Super POM.

## ⚙️ Maven Build Lifecycles and Phases

*   **Standardized Build Lifecycle**: Maven offers a standardized build lifecycle with a sequence of phases.
*   **Three Lifecycles**: Maven has three built-in lifecycles:
    *   `clean`: For cleaning the build (pre-clean, clean, post-clean).
    *   `default`: For general builds.
    *   `site`: For generating project sites.
*   **Phases**: Each lifecycle consists of phases, which are steps in the build process.
*   **Lifecycle Execution:** When you run `mvn <phase>`, Maven executes all phases up to the specified phase.
*   **Plugin Goals:** Plugin goals are bound to phases in the build lifecycle.
*   **Plugin Bindings:** You can inspect plugin bindings in the Effective POM.
    *   Plugins are bound to specific phases.
*   **Sequential Execution**: Phases are executed sequentially.
*   **Example:**
    *  `mvn test-compile` will execute all phases up to the `test-compile` phase including the `compile` phase.
    *   Phases with bound plugin goals are executed in the build output.
*   **Built-in Bindings:** The documentation shows default bindings (e.g., compile phase executes the compile goal of the compiler plugin).
    *   The `package` phase varies based on the packaging type (e.g., war plugin for `war`, jar plugin for `jar`).
*   **Maven compile**: Executes all phases up to the compile phase, and also the resource plugin is run before.
*   **Maven test-compile**: Executes all phases up to the `test-compile` phase, and executes the resource plugin again.
*   Maven allows customization by binding different plugin goals at different phases.

## 📦 Resolving Dependencies

*   **Simple Dependency**: A simple dependency doesn't rely on other dependencies (e.g., Commons Lang).
    *  When a dependency is added to `pom.xml`, Maven downloads it and installs it in the local repo cache.
*   **Complex Dependency**: A complex dependency has other dependencies, called transitive dependencies (e.g., Spring MVC).
*   **Spring MVC Example**:
    *   Adding Spring Web as a dependency leads to the inclusion of multiple jar files in the WAR file.
    *   Maven inspects the pom file of the spring web dependency and downloads its dependencies.
*   **Transitive Dependencies:** Maven resolves dependencies recursively, downloading all transitive dependencies.
*   **Dependency Tree:** You can inspect the dependency tree using the dependency plugin.
    *   Use `mvn dependency:tree` to see the full graph of dependencies.
    *   The tree shows top-level dependencies, as well as their dependencies (transitive dependencies).
*   Maven uses the GAV coordinates in the pom files to resolve the dependencies.

## 🔎 Finding Dependencies in Maven Central

*   **Maven Central Repository:** You can use the search front end at [search.maven.org](http://search.maven.org) to look up dependencies.
*   **Basic Search:** Search using artifact ID, or other string, not necessarily the artifact ID.
*   **Advanced Search:** Use the advanced search to search using Group ID, Artifact ID, or version.
*   **Search by Class Name:** Search by fully qualified class name, replacing slashes with dots to find which artifact includes that class.
*   **Dependency Details:** Once you find the dependency, you can see:
    *   Dependency snippet for `pom.xml`.
    *   The `pom.xml` file.
    *   Download links for the jar, source, javadoc, etc.
*  **Dependency Information**: This section provides the dependency snippet to use in your project's `pom.xml` file.
*   **Download Artifacts:** You can download the JAR file or the source code of the dependency.

## 📁 The Maven Local Repo Cache

*   **Local Repository:** Maven caches downloaded dependencies in the local repository, located in `~/.m2/repository`.
*   **Cache Behavior:**
    *   Maven checks the local repository first.
    *   If the dependency is not found, it's downloaded from the remote repository (e.g., Maven Central) and cached locally.
*   **Benefits:**
    *   Faster builds since dependencies are cached locally.
    *   Enables offline builds.
*   **Folder Structure:** The local repo cache is organized by the GAV coordinates of the dependencies.
    *   Group ID folders, then Artifact ID folders, then Version folders, then the actual artifact (jar, pom, etc).
*   This layout is identical to that of external repositories.

## 📦 Population of the Local Repo Cache during a Build

*   **Demonstration:** Deleting the local repository forces Maven to download all dependencies again.
*   **Just-in-Time Download:** Maven downloads dependencies as needed.
*   **Archetype Plugin:** When you use `mvn archetype:generate`, Maven downloads the archetype plugin and its dependencies.
*   **Build Process:** During a build (e.g., `mvn install`), Maven downloads any missing plugins and dependencies.
*  **Plugin Dependencies:** Maven also downloads the dependencies of the plugins.
*   The local repository is populated with artifacts and their POM files.
*  **Rebuilding from Scratch**: You can delete your local maven repo cache if you encounter strange Maven behavior.

## 🧩 Maven Plugins

*   **Plugin Overview:** Maven uses plugins to provide build functionality.
*   **Plugin Examples**:
    *   Compiler plugin for compiling Java source code.
    *   Jar plugin for making jar files.
    *   War plugin for making war files.
    *   Surefire plugin for executing tests.
*   **Plugin Website:** The [maven.apache.org/plugins](http://maven.apache.org/plugins) website is a good resource for finding plugins.
*   **Plugin Configuration:** You can configure plugins in the `pom.xml` file.
*  **Plugin Goals**: Plugins have goals, which are like methods which are executed.
*   **Plugin Binding:** You can bind plugin goals to particular phases of the build lifecycle.
*   **Configuration Options**: You can configure and override the behavior of existing plugins.
    *  For example, you can configure the compiler plugin to use a specific Java source code level.

## ℹ️ The Maven Help Plugin

*   **Help Plugin:** The help plugin provides information about the Maven environment.
*  **Describe Goal:** The `help:describe` goal gives you information on plugins.
*   **Basic Usage:** `mvn help:describe -Dplugin=<plugin>` shows a top-level view of plugin goals.
*  **Detailed Plugin Information:** Add `-Ddetail` and a specific goal to get detailed information about a plugin and its configuration options, (e.g. `mvn help:describe -Dplugin=compiler -Ddetail=true -Dgoal=compile`).
*   **Configuration Options:** The help plugin shows the available configuration options.
*   **Plugin Configuration**: The configuration information can be added in a configuration block in the `pom.xml`.
*   **Plugin Naming:** When using `help:describe` with only one word (e.g. `compiler`), Maven assumes you are using a default plugin from the `org.apache.maven.plugins` group, and uses the naming convention `maven-<plugin>-plugin`.
    *   For third-party plugins, you have to use the GAV coordinates.

## 🌐 Creating a Web Application Project

*   **Maven Web App Archetype:** You can create a web app project using the Maven Web App archetype.
*   **Command:** `mvn archetype:generate -D filter=org.apache.maven.archetypes:` and select the webapp archetype.
*   **Packaging Type:** The packaging type is set to `war` by default.
*  **Final Name**: You can override the final artifact name in the build section of the pom.xml file.
*   **Source Directories:** The project contains:
    *   `src/main/resources`: For resources that will be placed in the `WEB-INF/classes` directory.
    *   `src/main/webapp`: Includes `index.jsp` and `WEB-INF/web.xml`.
    *   `src/main/java`: Can be created as a sibling of resources to include compiled Java files in the `WEB-INF/classes` directory.
*   **Building the WAR file**: `mvn package` creates a WAR file.
    *   The war file includes the JSP file at the root, the `web.xml` deployment descriptor in `WEB-INF`, and any files in the `classes` directory.
