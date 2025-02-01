This chapter focuses on installing Maven on different operating systems and checking your installation.

## 💻 Installation Basics: Introduction

*   **Importance of Installation:** While not the most exciting topic, installing Maven correctly is crucial before you can start using it.
*   **Zip Install Method:** The most common method involves downloading a zip file from the Maven website, unzipping it, and configuring environment variables. This works on **Windows, Linux, and Mac**.
*   **Installation Methods Covered:** The chapter covers:
    *   Traditional zip install for **Windows and Linux**
    *   **SDKMAN** for Mac

## 🔍 Checking for Existing Installation

*   **Java Requirement:** Maven runs on Java, making it platform-agnostic, capable of running on **Linux, Windows, Mac, or Unix**.
*  **Check Java Version**: Type `java -version` in the command line. You need at least **JDK 1.7**.
*   **Maven Command:** The `mvn` command is the command-line interface for Maven.
*   **Check Maven Version:** Use `mvn --version` to check if Maven is installed.
    *   This command displays:
        *   Maven version
        *   Maven home directory
        *   JDK version
        *   Java home directory
        *   Platform settings
*   If the version information message is displayed, Maven is installed.

## ⚙️ Installing Maven on Windows

*   **Check Java:** First, verify that Java is installed using `java -version` in the command prompt.
    *   You can open the command prompt via the start menu or using a shortcut.
*   **Download Maven:** Go to [maven.apache.org](http://maven.apache.org) and navigate to the downloads section.
*   **System Requirements:** Ensure you have the **JDK** installed as a prerequisite.
*   **Binary Distribution:** Download the binary `.zip` distribution. The source distribution is only needed if you want to develop Maven itself or write plugins.
*   **Installation Directory:** Create a `C:/Java` directory and copy the downloaded `.zip` into this folder.
    * This keeps all Java tools in one place.
*   **Unpack the Archive:** Use `java -xvf apache-maven-3.x.x-bin.zip` to unpack the archive.
    *   You need Java Home set and Java Home bin on the system path to use the Java command
    *   Alternatively, use a Windows decompression tool.
*   **Delete the .zip:** Remove the zip file after unpacking.
*   **Set Environment Variables:**
    *   Access System Properties, then Advanced System Settings and click the Environment Variables button.
    *   Set a new system variable with variable name `M2_HOME` and the value as the path to the unzipped Maven folder.
    *   Edit the `Path` variable, append `;%M2_HOME%\bin` to the end of its value.
*   **Verify Installation:** Open a new command prompt and type `mvn --version`. The version message confirms a successful installation.

## 🐧 Installing Maven on Linux

*   **Ubuntu 16.04 LTS** is used in the demo, but the process is similar for other Linux distributions.
*   **Traditional Installation:** Download the `.zip` from the Maven website, extract it, set the `M2_HOME` environment variable, and add the bin directory to the system path.
*   **Download Maven:** Go to [maven.apache.org](http://maven.apache.org) and navigate to the download section. Download the binary distribution.
*   **Installation Directory:** Install Java tools in `/opt/Java`.
    *  Create the `/opt/Java` directory if it doesn't exist using `sudo mkdir /opt/Java`.
*    **Unpack the Archive:** Extract the archive into `/opt/Java` using the command `sudo tar -xvf apache-maven-3.x.x-bin.tar.gz`
*   **Verify Executable Flag:** The Maven scripts should already have the executable flag set.
*   **Set Environment Variables:** Add the following to your `.profile` (or `.bashrc`):
    *   `export M2_HOME=/opt/Java/apache-maven-3.x.x`
    *   `export PATH=$PATH:$M2_HOME/bin`
*   **Log Out and Back In:** Log out and back in for the changes to take effect.
*    **Verify Installation**: Type `mvn --version` in the terminal. The version message confirms successful installation.

## 🍎 Installing Maven on Mac with SDKMAN

*   **SDKMAN:** A tool that manages various Java-related tools (e.g., Gradle, Maven, Groovy). It works well on Mac and Linux.
*   **Installation:**
    *   Go to [sdkman.io](http://sdkman.io).
    *   Copy the installation command from the website and execute it in the terminal.
    *   This command downloads and sets up SDKMAN.
    *   SDKMAN setup is added to `.bash_profile` or similar.
*   **Interacting with SDKMAN:** Type `sdk` to interact with the tool.
*  **List Available Packages**: Use `sdk list` to view available packages.
*   **Search for Maven:** Use `sdk list maven` to find Maven.
*   **Install Maven:** Use `sdk install maven` to install the latest version.
*   **Verify Installation:** Use `mvn --version` to check the installed version.
*   **List Installed Versions:** `sdk list maven` lists installed versions and the version in use.
*   **Install Specific Version:** Install a specific version using `sdk install maven <version>`.
*   **Use Specific Version:** Switch to a specific version using `sdk use maven <version>`.
*   **SDKMAN Directory:** SDKMAN installs packages in `.sdkman` in your home directory.
    *   Packages are located in `candidates` folder.

## 📁 Maven Installation Directory Tour

*   **Find Maven Home:** Use `mvn --version` to find the Maven home directory.
*   **Bin Directory:**
    *   Contains `mvn` (shell script for Linux/Mac) and `mvn.cmd` (for Windows).
    *   `mvnDebug` can be used to run Maven with debug options.
*   **Conf Directory:** Contains `settings.xml`, the default Maven settings file.
    *   You can customize settings, including the local repository, proxies, and plugin groups.
    *   The default local repository is located at `.m2/repository` in the user's home directory.
